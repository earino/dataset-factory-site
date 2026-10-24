# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.09**

[Dataset website](https://earino.github.io/chicago-doah-adjudication/versions/v2026.09/) · [GitHub release](https://github.com/earino/chicago-doah-adjudication/releases/tag/v2026.09) · [Hugging Face](https://huggingface.co/datasets/earino/chicago-doah-adjudication/tree/v2026.09) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: b71586bf28fa56ebbfaede26c4494d68b166545ac504b2ebd8a52c7f272627ef

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. No answer recovery was found in the bounded audit; historical forecasting validity remains unverified.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** bounded no recovery. Bounded attack search, 15 active minutes per repository, frozen plan; not a security proof Holdout recovery was not tested by this audit.

Structural qualification and baseline scores do not certify operational forecasting validity.

- The bounded leakage audit found no meaningful recovery (57/3,436 covered, 4 mismatches, AUC 0.4732); absence of a discovered shortcut is not evidence none exists.
- Historical feature/label availability at the declared prediction instant is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame to predict_proba; prediction-time isolation is instructed but not mechanically enforced.
- Charge counts are aggregated from the current final case records. The build does not verify that all charges existed at docketing or that training dispositions were known before later prediction windows.

Review: 2026-10-24; applies to v2026.09 / `b71586bf28fa56ebbfaede26c4494d68b166545ac504b2ebd8a52c7f272627ef`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
