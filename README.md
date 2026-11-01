# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.10**

[Dataset website](https://earino.github.io/ipo-trademark-registration-outcome/versions/v2026.10/) · [GitHub release](https://github.com/earino/ipo-trademark-registration-outcome/releases/tag/v2026.10) · [Hugging Face](https://huggingface.co/datasets/earino/ipo-trademark-registration-outcome/tree/v2026.10) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: 2c1dade2913d0a8b643c89e628095a18e03223a6167beb9363316389486a544d

### Suitability and evaluation requirements

Retained for retrospective model-development research. Each row is one distinct trade mark application whose features are its own filing-time attributes as recorded in the single frozen 2018-02-13 IPO snapshot; the prediction instant is the filing event (event_time) and no point-in-time or operational claim is made. The publisher serves exactly one frozen vintage and no historical vintages, so training-label timing and full-row historical availability are unverified and none is claimed. Measured finding carried beside every figure: the stock runner baseline (eval AUC 0.6224, Brier 0.1318) exceeds every measured simple reference on the identical 97,274 eval rows - mark-type rate 0.5650 (+0.0574, CI95 [0.0533, 0.0605]), nice-class rate 0.5421 (+0.0803, [0.0748, 0.0862]), calendar-month rate 0.4972 (+0.1252, [0.1174, 0.1315]) - all paired row-level intervals excluding zero, with the advantage holding in both eval filing years at flat prevalence: demonstrated headroom over these references under this protocol, with its scope recorded (row-level intervals only - no dependence cluster is measurable from the shipped columns; one model configuration, no re-tuning; two filing years of eval coverage). Persistence is not applicable (every scored row is a new application).

**Supported uses:** Retrospective research and method comparison on the pinned 2018-02-13 snapshot, predicting row-wise from the shipped filing-time columns; Agent evaluation with the labeled eval split as development/validation data and the holdout kept outside agent development until a design is frozen; Study of filing-cohort prevalence and of which filing-time attributes carry registration-outcome signal

**Not supported:** Operational or live filing-time screening claims: no historical operational-availability evidence exists and none is claimed; Point-in-time historical reconstruction: the publisher serves one frozen snapshot; a later re-fetch is a different vintage, not what was knowable earlier; Quoting the model AUC (0.6224) without the reference comparison (mark-type 0.5650, nice-class 0.5421, calendar 0.4972, with the paired intervals) beside it; Treating the snapshot-vintage owner fields (country/region/postcode area) or class columns as as-of-filing facts: ownership can be assigned after filing and classes can be narrowed

**Evaluation access:** isolated rows. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** unverified. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** prediction time.

**Cross-row audit:** untested. No cross-row exposure is declared and none is structurally available in the shipped columns: every feature is a filing-time attribute of the application itself (mark text, class booleans, category, type, series, owner fields, filing date), no history or aggregate feature crosses rows, tm_number is unique per row, and the label source columns are excluded from every shipped CSV. The panel-style reverse-history probes declared for panel-shaped candidates therefore do not apply; no donor-join audit has been run against this artifact. The isolation contract is the row-per-application grain itself; the shipped illustrative runner passes the whole eval feature table to the predictor, which does not create an exposure here but is also not an enforcement mechanism.

Structural qualification and baseline scores do not certify operational forecasting validity.

- Single frozen vintage (2018-02-13 snapshot, sha256-pinned); the publisher revises in place and retains no historical vintages, so no historical operational-availability claim is possible
- Training-label timing and full-row historical availability are unverified; the task is retrospective research only
- Owner and class columns are snapshot-vintage: assignment can move ownership after filing and classes can be narrowed post-filing - a uniform-vintage limitation declared in quality.json, never an as-of claim
- Censoring is outcome-observability conditioning recorded as a limitation: marks unresolved at the snapshot (21/172/809 per split) are excluded and counted, never labelled negative
- The headroom finding's scope: row-level intervals only (no dependence cluster measurable from the shipped columns), one model configuration with no re-tuning, and two filing years of eval coverage; beating the measured rate references does not enumerate all simple rules and does not prove a causal signal
- The holdout was never evaluated; no holdout figure exists and its first use must follow a frozen design

Review: 2026-10-30; applies to v2026.10 / `2c1dade2913d0a8b643c89e628095a18e03223a6167beb9363316389486a544d`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
