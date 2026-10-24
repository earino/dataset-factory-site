# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.10**

[Dataset website](https://earino.github.io/my-pricecatcher-weekly-increase/versions/v2026.10/) · [GitHub release](https://github.com/earino/my-pricecatcher-weekly-increase/releases/tag/v2026.10) · [Hugging Face](https://huggingface.co/datasets/earino/my-pricecatcher-weekly-increase/tree/v2026.10) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: 06c5cd6f8a74aef9d1fab048ab88f86e311385e68c0d25416b7ac5c0281a23cf

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. Later evaluation rows expose earlier outcomes; predictions require restricted access.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results; Forecasting scores from unrestricted cross-row access to this artifact

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** recovery demonstrated. Independent operator-commissioned audit; predictions frozen before labels were opened; holdouts sealed; two AUC implementations in exact agreement

Structural qualification and baseline scores do not certify operational forecasting validity.

- join (premise, item, T) -> (same pair, T+7 days): the next row's prices are the operands of T's label
- The labelled holdout is presumed to carry the same self-answering structure by construction; it was never opened by the audit and must be treated as compromisable by the same join class.
- Historical feature/label availability at the declared instant is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame to predict_proba; prediction-time isolation is instructed but not mechanically enforced, so any framework score on these files is gameable.
- Observing same-day rows in one current bulk file does not verify historical weekly completeness or revision timing. Missing next-week outcomes restrict the scored population.

**Corrections to the historical documentation:**

- Public site page, Hub card and repository README must state the restricted suitability once rendered; no frozen package bytes change.

Review: 2026-10-24; applies to v2026.10 / `06c5cd6f8a74aef9d1fab048ab88f86e311385e68c0d25416b7ac5c0281a23cf`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
