# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.10**

[Dataset website](https://earino.github.io/tsb-railway-occurrence-casualty/versions/v2026.10/) · [GitHub release](https://github.com/earino/tsb-railway-occurrence-casualty/releases/tag/v2026.10) · [Hugging Face](https://huggingface.co/datasets/earino/tsb-railway-occurrence-casualty/tree/v2026.10) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: e75a59bb1116e39b980c9fa2f5ea7c2b984fa6ccce4b3286f194de69d2b32309

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. No answer recovery was found in the bounded audit; historical forecasting validity remains unverified.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** bounded no recovery. Bounded attack search, 15 active minutes per repository, frozen plan; not a security proof Holdout recovery was not tested by this audit.

Structural qualification and baseline scores do not certify operational forecasting validity.

- The bounded leakage audit found no recovery path (0 covered by any tested join); a bounded search is not a proof. One calendar week straddles train/eval (5 eval rows).
- Historical feature/label availability at the declared prediction instant is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame to predict_proba; prediction-time isolation is instructed but not mechanically enforced.
- Features come from a finalized occurrence register; excluding outcome taxonomy does not prove each retained contextual field was available at occurrence onset.

Review: 2026-10-24; applies to v2026.10 / `e75a59bb1116e39b980c9fa2f5ea7c2b984fa6ccce4b3286f194de69d2b32309`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
