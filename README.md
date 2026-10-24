# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.09**

[Dataset website](https://earino.github.io/noaa-tide-flooding/versions/v2026.09/) · [GitHub release](https://github.com/earino/noaa-tide-flooding/releases/tag/v2026.09) · [Hugging Face](https://huggingface.co/datasets/earino/noaa-tide-flooding/tree/v2026.09) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: fb49f932c7b4ea5ab532c20f7dce59a7d733de925d1e172054ff1d38abe1eeed

### Suitability and evaluation requirements

Retained for retrospective model-development research with documented timing limitations. Later evaluation rows expose earlier outcomes; predictions require restricted access.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing and selection limitations; Final evaluation only under a protocol that isolates holdout data from development and prevents later rows influencing earlier predictions

**Not supported:** Claims of verified real-time or operational forecasting validity; Treating development/validation scores as untouched final-test results; Forecasting scores from unrestricted cross-row access to this artifact

**Evaluation access:** chronological. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** assumed. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** unverified.

**Cross-row audit:** recovery demonstrated. Both split designs (temporal, station-disjoint) tested; temporal 88,915/89,038 covered AUC 0.99929 with 423 binary mismatches; station-disjoint 29,889/29,930 AUC 0.99922 with 191; a D+2 margin_ft variant still ranks ~0.9993, so deleting the obvious column is not a fix Holdout recovery was not tested by this audit.

Structural qualification and baseline scores do not certify operational forecasting validity.

- Near-perfect future-outcome ranking in both split designs (see cross_row_audit scope).
- Dictionary/build day-definition conflict: release/noaa-tide-flooding/code/build.py assigns the official minFlag to date+1 while DATA_DICTIONARY.md describes the target-day value.
- One calendar week straddles train/eval in each design (244 temporal, 82 station-disjoint eval rows).
- Historical feature/label availability is assumed from current snapshots, not verified against release vintages.
- The current scorer passes the complete feature frame; isolation is not mechanically enforced.

**Corrections to the historical documentation:**

- For row date D, observed_max_ft is the measurement on D; margin_ft and trailing summaries use observations preceding D (through D-1 when consecutive). The label is NOAA’s official minor-flood flag for D+1. It is not the same-day flag and is not defined by simply thresholding observed_max_ft. Historical verification/publication timing remains unverified.
- The original dictionary says carry columns are dropped. The bundled template excludes only target and id_columns; observed_max_ft and threshold_ft are therefore available to that baseline. This does not by itself expose its own D+1 label, but the documentation must not claim those columns were excluded.

Review: 2026-10-24; applies to v2026.09 / `fb49f932c7b4ea5ab532c20f7dce59a7d733de925d1e172054ff1d38abe1eeed`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
