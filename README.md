# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.10**

[Dataset website](https://earino.github.io/abs-visitor-arrivals-direction/versions/v2026.10/) · [GitHub release](https://github.com/earino/abs-visitor-arrivals-direction/releases/tag/v2026.10) · [Hugging Face](https://huggingface.co/datasets/earino/abs-visitor-arrivals-direction/tree/v2026.10) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: afb46c6b29e6c4aa7668afcbd8f14c3f02ad56066bb7fbd5af263802740ad442

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. Later evaluation rows expose earlier outcomes; predictions require restricted access.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results; Forecasting scores from unrestricted cross-row access to this artifact

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** recovery demonstrated. Independent operator-commissioned audit; predictions frozen before labels were opened; holdouts sealed; two AUC implementations in exact agreement

Structural qualification and baseline scores do not certify operational forecasting validity.

- eval join (country, T) -> (country, T+1): the next row's val_m and val_m12 are the two operands of T's label
- The labelled holdout is presumed to carry the same self-answering structure by construction; it was never opened by the audit and must be treated as compromisable by the same join class.
- Historical feature/label availability at the declared instant is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame to predict_proba; prediction-time isolation is instructed but not mechanically enforced, so any framework score on these files is gameable.

**Corrections to the historical documentation:**

- Public site page, Hub card and repository README must state the restricted suitability once rendered; no frozen package bytes change.

Review: 2026-10-24; applies to v2026.10 / `afb46c6b29e6c4aa7668afcbd8f14c3f02ad56066bb7fbd5af263802740ad442`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
