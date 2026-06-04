# Keum and Warey 2026 Summary

## Citation

Seunghwan Keum and Alok Warey, "Bracketing Inference with Uncertainty
Quantification: A Reliability Pipeline for Neural Aerodynamic Surrogates."
Research Square preprint, posted May 28, 2026.

https://www.researchsquare.com/article/rs-9775673/v1
DOI: https://doi.org/10.21203/rs.3.rs-9775673/v1

Local source: `sources/to_review/keum_and_warey_preprint.pdf`

---

## What the Paper Is About

Keum and Warey study neural surrogates for automotive computational fluid dynamics
(CFD). These are machine-learning models that approximate expensive CFD simulations
for vehicle aerodynamics.

The practical promise is speed: instead of running a full CFD simulation for every
new design variant, a trained neural model can predict pressure fields, aerodynamic
forces, drag, lift, and related quantities.

The central problem is reliability.

Their key deployment observation is:

> a trained neural surrogate will never refuse to predict.

Given any new vehicle geometry, even one far outside the model's training
distribution, the surrogate produces a plausible-looking aerodynamic field. That is
dangerous in engineering because a wrong-but-confident prediction can directly affect
design decisions.

The paper argues that, as benchmark accuracy saturates, the barrier to industrial
deployment shifts from raw predictive performance to trustworthiness: knowing when
the model is inside or outside its domain of competence.

---

## Proposed Reliability Pipeline

The authors propose a two-stage uncertainty quantification pipeline that brackets
inference:

1. Pre-inference out-of-distribution detection.
2. Post-inference confidence diagnostics.

The point is not that their specific methods are uniquely correct. Their contribution
is the practical workflow: do not let the surrogate silently extrapolate, and do not
present predictions without uncertainty information.

---

## Stage 1: Pre-Inference OOD Detection

Before trusting the surrogate, the pipeline checks whether the new geometry lies
within the model's learned domain of competence.

The authors use **Mahalanobis distance** in the model's learned geometry-feature
space.

The geometry is passed through the model's geometry encoder, producing a learned
feature vector. The Mahalanobis distance measures how far that feature vector lies
from the training distribution.

If the distance is high, the geometry is flagged as out-of-distribution and should
not be trusted. In a production workflow, it should be sent to full CFD rather than
accepted from the neural surrogate.

Important details:

- Features are extracted from the geometry encoder, not the downstream physics
  prediction branches.
- The model uses a 512-dimensional feature space.
- Because the number of CFD samples is limited, covariance estimation requires
  Ledoit-Wolf shrinkage.
- The authors emphasize that Mahalanobis distance becomes unstable when the number
  of samples is much smaller than the feature dimension.

---

## Stage 2: Post-Inference Confidence Diagnostics

If the geometry passes the OOD screen, the pipeline can run uncertainty estimation
after inference.

The authors use **Monte Carlo Dropout**:

- keep dropout active at inference time;
- run the model multiple times;
- treat variation across predictions as an uncertainty signal.

This produces spatial uncertainty maps over the vehicle surface, showing where the
model is least confident.

The advantage is interpretability: engineers can see which regions of the predicted
flow field are unreliable, such as front fascia, wheel arches, underbody separation
zones, or other geometrically sensitive regions.

The disadvantage is cost and calibration. MC Dropout requires repeated forward passes,
which is expensive for large transformer-based surrogate models. More importantly,
the resulting confidence intervals are badly miscalibrated.

---

## Dataset and Model

The study uses a proprietary General Motors dataset:

- 511 CFD simulations;
- 5 vehicle types;
- roughly 100 design variants per vehicle type;
- vehicle types include midsize SUV, small crossover, and multiple large SUVs.

The model is a transformer-based neural surrogate:

> AB-UPT: Anchored-Branched Universal Physics Transformer.

The architecture separates geometry encoding, surface prediction, and volume
prediction into interacting branches. The configuration used in the study has:

- latent dimension 512;
- 8 attention heads;
- 6 geometry encoder blocks;
- 12 mode-specific encoder blocks per branch;
- approximately 87 million parameters;
- training on 8 NVIDIA H100 GPUs.

---

## Main Findings

### 1. Mahalanobis Distance Works Well as an OOD Screen

When the model is trained on four vehicle types and evaluated on the fifth unseen
vehicle type, Mahalanobis distance cleanly separates the unseen vehicle type from
the in-distribution vehicles.

In their 4-vehicle experiment:

- training `DM` p95: 10.45;
- training max: 12.60;
- all in-distribution vehicles fall below roughly 14;
- OOD vehicle minimum: 26.32.

A threshold around `DM > 15` would achieve perfect separation in this dataset.

Mahalanobis distance also correlates with prediction error: samples farther from the
training distribution tend to have larger force prediction errors.

### 2. Progressive Training Diversity Reduces OOD Distance

As more vehicle types are added to the training set, the Mahalanobis distributions
tighten and previously OOD geometries move into the learned distribution.

This is a useful sanity check: the metric is not just detecting arbitrary differences;
it reflects whether the model has actually seen comparable geometry classes during
training.

### 3. MC Dropout Is Spatially Informative but Badly Calibrated

MC Dropout provides useful spatial uncertainty maps. Regions with elevated dropout
variance often coincide with regions of high true prediction error.

But the confidence intervals are far too narrow.

For nominal 95% confidence intervals, observed coverage is:

- drag force `Fx`: 47.7%;
- side force `Fy`: 3.5%;
- lift force `Fz`: 8.6%.

This means the model is systematically overconfident.

MC Dropout often knows **where** the prediction is risky, but not **how wrong** it is.

### 4. OOD Geometries Make Overconfidence Worse

When MC Dropout is applied to OOD geometries, the standard deviation increases, so
it does provide an indirect OOD signal.

However, actual prediction error increases much faster than the uncertainty estimate.
In one example:

- ID mean MC standard deviation: 6.43 N;
- OOD mean MC standard deviation: 8.60 N;
- OOD actual error increases by roughly 670%.

So the model becomes confidently wrong on OOD data.

### 5. Sample Size Matters for Mahalanobis Distance

The method depends on estimating a covariance matrix in feature space. If the number
of training samples `N` is much smaller than the feature dimension `d`, the estimate
breaks down.

In a LoRA fine-tuning example with:

- `N = 20`;
- `d = 512`;

the Mahalanobis scores become pathological. The authors recommend monitoring the
`N/d` ratio and using mitigations such as dimensionality reduction or shared reference
statistics from a larger pretrained model.

---

## Practical Recommendation

The authors recommend a two-stage deployment workflow:

1. **Mandatory pre-inference gate**:
   Use Mahalanobis distance to detect whether a geometry is outside the model's
   training distribution. If it is OOD, do not trust the surrogate; run full CFD.

2. **Optional post-inference diagnostic**:
   For geometries that pass the OOD screen, use MC Dropout only when the prediction
   is high-stakes and spatial uncertainty information is useful.

Their conclusion is that uncertainty quantification is not an optional add-on for
industrial SciML. It is part of the deployment pipeline.

---

## Relevance to the Talk

This paper is not about LLMs or theoretical physics. It does not belong in the main
evidence chain with Hsu, Pan et al., Lu et al., Robin, Co-Scientist, or Castelvecchi.

Its relevance is indirect but useful.

It is an engineering-world version of the same reliability problem:

> AI systems do not naturally know when they are outside their competence.

In the talk's terms:

- Hsu shows that LLMs can produce serious but fallible frontier-physics reasoning.
- Keum and Warey show that neural SciML surrogates can produce plausible but
  unreliable CFD predictions.
- In both cases, raw model output must be wrapped in a reliability workflow.

The common structure is:

> model capability + reliability wrapper + expert judgment.

This aligns with the talk's expert-bottleneck thesis. In Keum and Warey, the expert
bottleneck appears as engineering deployment discipline: OOD screening, uncertainty
diagnostics, and the decision to send suspicious cases back to full CFD.

---

## Possible Use in the Talk

Best placement: optional support in section 4 or section 5.

Suggested line:

> A recent GM SciML paper makes the deployment version of the same point: a neural
> surrogate never refuses to predict. The reliability problem is not just accuracy;
> it is knowing when the model should not be trusted.

This can support the argument that AI reliability in scientific domains is not solved
by better benchmark performance alone. Deployment requires systems that can identify
domain mismatch and quantify uncertainty.

Do not overuse it. It is applied engineering SciML, not evidence for AI contributing
to theoretical physics. Its value is as a cross-domain confirmation that scientific AI
deployment is converging on reliability-gated workflows.

---

## One-Line Version

> Keum and Warey show the engineering analogue of the expert-bottleneck problem:
> neural surrogates can make fast, plausible scientific predictions, but deployment
> requires a reliability gate because the model never refuses to answer.
