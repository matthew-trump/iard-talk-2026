# Codex Verification Report

Date: 2026-05-31

Scope: reviewed the talk draft, local source files, and current web metadata for the main factual claims. This was a research/editorial verification pass, not a line edit.

## Bottom Line

The project is substantially coherent and most quantitative claims checked out against the provided sources. The main issue is not arithmetic or citation drift; it is that the Hsu anchor case is presented as a settled physics result even though there is now a direct 2026 arXiv comment challenging the paper's central claim.

The talk can still use Hsu as the anchor example of an AI-originated research workflow, but it should separate that from the stronger claim that Hsu's no-go result is established physics.

## High-Priority Findings

1. Hsu result is actively disputed.

   The draft repeatedly presents Hsu's PLB paper as a successful, settled QFT result. However, Lajos Diosi posted "Comment on 'Relativistic covariance and nonlinear quantum mechanics: Tomonaga-Schwinger analysis'" on 2026-02-06, claiming that Hsu's central claim is wrong and that the TS equation remains covariant despite the nonlinear modification.

   Recommended fix: add a brief caveat in section 2 and soften claims like "What Hsu shows is..." to "Hsu argues..." or "the PLB paper claims..." unless you are prepared to adjudicate Diosi's objection. This actually strengthens the talk's AI-risk thesis: the anchor case may itself illustrate why AI-assisted frontier theory needs post-publication scrutiny.

2. "Established" language is too strong in `talk_project/NOTES.md`.

   `talk_project/NOTES.md` says the Hsu paper "established that state-dependent nonlinear modifications to quantum mechanics fundamentally violate relativistic covariance." Given the Diosi comment, that should be changed to "argued" or "claimed."

3. Missing Wang reference summary.

   `talk_project/reference_summaries/03_pan_et_al_2025.md` points to `09_wang_et_al_2024.md`, but no such file exists under `talk_project/reference_summaries`. The source PDF does exist at `sources/to_review/wang_et_al_2024.pdf`.

4. Section 5.6 is intentionally unfinished.

   The first-person section is still a skeleton. The plan already notes this, but it is a real delivery blocker because the surrounding argument depends on the speaker's personal experience doing QFT/LLM work.

5. Minor naming/date cleanup.

   The local filename `hsu_2025_physical_review_letters_b.pdf` and `THESIS.md` phrase "Phys Rev Letters B" are incorrect/confusing. The journal is `Physics Letters B`, volume 872, article 140053, issue dated January 2026, DOI dated 2025.

## Claims Checked Out

- Hsu PLB metadata: `Physics Letters B` 872, article 140053; DOI `10.1016/j.physletb.2025.140053`; available online 2025-11-24; issue volume dated 2026.
- Hsu acknowledgement: GPT-5, Gemini 2.5 Pro, and Qwen-Max are acknowledged for checking results, LaTeX formatting, and related-work exploration.
- Hsu methodology paper: the quoted GPT-5 Tomonaga-Schwinger suggestion, "novel research direction" assessment, Generate-Verify prompt, Reeh-Schlieder failure, and "brilliant but unreliable human genius" quote are present in the local PDF.
- Pan et al. 2025: 87.5/100 average, 13/15 final HF Hamiltonians, above-95 rigor, 6456 cond-mat HF abstracts, one-shot extraction jump from 44 +/- 8 to 80 +/- 6, and September 2021 cutoff discussion are supported.
- Wang et al.: 40 GPT-4 physics problems, 62.5% well-specified vs. 8.3% under-specified, Fisher exact test p < 0.001, and physical-world-modeling failure mode are supported.
- Castelvecchi 2026 Nature feature: Liam Price/Erdos #1196, May 19 2026, Nature 653:664-665, proof length 3-4 pages, Google internal models targeting 10 pages, 100 pages not yet within capability, Fields Medal prediction, and "AI slop" concern are supported.
- Ghareeb et al. Robin: 551 papers in 30 minutes, ~540 human hours, $10.76 run estimate, ripasudil 1.89-fold RPE phagocytosis result, KL001 claim, ABCA1 upregulation, Deep Research comparison, and 44.5 +/- 6.37% hallucinated references for o4-mini ablation are supported.
- Gottweis et al. Co-Scientist: multi-agent Gemini system, test-time compute scaling, AML/KIRA6/binimetinib claims, cf-PICI two-days claim, expert-in-the-loop design, and homogenization/reproducibility cautions are supported.
- Nature editorial: "feature, not a bug," efficiency-vs-insight distinction, Perutz framing, and "Does science need humanity?" inversion are supported.

## Recommended Draft Changes

- In section 2, add a short caveat after the physics summary:

  "A February 2026 arXiv comment by Lajos Diosi disputes Hsu's central covariance claim. I am not going to adjudicate that technical dispute here. For this talk, the load-bearing point is the documented workflow: a peer-reviewed PLB paper whose research direction Hsu says originated in GPT-5, followed by human and model verification."

- Replace "What Hsu shows..." with "Hsu argues..." in the technical summary unless you include the dispute.
- In sections 1 and 5, avoid using Hsu as uncomplicated evidence that AI produced a correct result. Use it as evidence that AI produced a publishable and technically serious research direction.
- Add `talk_project/reference_summaries/09_wang_et_al_2024.md` or remove the dangling reference from the Pan summary.
- Fill section 5.6 before rehearsal. If it remains skeletal, cut it rather than improvise.

## External Sources Used

- Hsu PLB: https://www.sciencedirect.com/science/article/pii/S0370269325008111
- Hsu arXiv: https://arxiv.org/abs/2511.15935
- Diosi comment: https://arxiv.org/abs/2602.06845
- Pan et al.: https://www.nature.com/articles/s42005-025-01956-y
- Wang et al.: https://arxiv.org/abs/2310.08773
- Castelvecchi Nature feature: https://www.nature.com/articles/d41586-026-01553-1
- Ghareeb et al. Robin: https://www.nature.com/articles/s41586-026-10652-y
- Gottweis et al. Co-Scientist: https://www.nature.com/articles/s41586-026-10644-y
- Lu et al. physics agents: https://arxiv.org/abs/2506.06214
- Apple "Illusion of Thinking": https://machinelearning.apple.com/research/illusion-of-thinking
