# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.09**

[Dataset website](https://earino.github.io/austin-911-response/versions/v2026.09/) · [GitHub release](https://github.com/earino/austin-911-response/releases/tag/v2026.09) · [Hugging Face](https://huggingface.co/datasets/earino/austin-911-response/tree/v2026.09) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: e4598317e406984fa590aacc5e7aff675867578c51ae1a84ebf6279bc42c3328

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. No answer recovery was found in the bounded audit; historical forecasting validity remains unverified.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** bounded no recovery. Bounded attack search, 15 active minutes per repository, frozen plan; not a security proof Holdout recovery was not tested by this audit.

Structural qualification and baseline scores do not certify operational forecasting validity.

- The bounded leakage audit's strongest lookup (identical full feature vector matched to unanimous train labels) covered 75,300/285,665 eval rows with 25,154 mismatches, AUC 0.6386: context memorization, not answer reconstruction - but a bounded search is not an absence proof.
- Historical feature/label availability at the declared prediction instant is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame to predict_proba; prediction-time isolation is instructed but not mechanically enforced.
- The response-time outcome clock begins when the call was answered, before the dispatch prediction instant; this is not a forecast of a fresh full 20-minute interval.

Review: 2026-10-24; applies to v2026.09 / `e4598317e406984fa590aacc5e7aff675867578c51ae1a84ebf6279bc42c3328`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
