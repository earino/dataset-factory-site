# Dataset Factory

<!-- dataset-factory:links -->
**Dataset Factory · v2026.10**

[Dataset website](https://earino.github.io/ec-merger-phase2-opening/versions/v2026.10/) · [GitHub release](https://github.com/earino/ec-merger-phase2-opening/releases/tag/v2026.10) · [Hugging Face](https://huggingface.co/datasets/earino/ec-merger-phase2-opening/tree/v2026.10) · [Catalogue](https://earino.github.io/dataset-factory-site/)

Artifact: e96929efbbc4fcb84d2986a7e32f83f9c5fec5395124439fb3404faff2e9e662

### Suitability and evaluation requirements

Retained for retrospective model-development research. Every shipped feature is a same-row case attribute fixed at notification (an administrative record), and eligibility reads only notification-time fields, but the register publishes a single current snapshot with no historical vintages, so training-label timing and full-row historical availability are unverified and no operational or point-in-time forecasting claim is supported.

**Supported uses:** Retrospective train/validation model-development experiments under the documented timing, vintage and selection limitations; Final evaluation only under a protocol that isolates the labeled holdout from agent development and prevents any later row influencing an earlier prediction

**Not supported:** Claims of verified real-time, operational or point-in-time forecasting validity; Treating development/validation (eval-split) scores as untouched final-test results; Presenting current-vintage register values (notably the NACE Rev 2 sector coding) as the values an analyst at notification time would have seen

**Evaluation access:** isolated rows. The labeled eval split is development/validation data. Keep the final holdout outside agent development; prevent later rows from influencing earlier predictions.

**Historical availability:** partial. **Training-label timing:** unverified. **Vintage:** current snapshot. **Selection:** prediction time.

**Cross-row audit:** bounded no recovery. Gate 1.5.0 executed its two declared probes on the full artifact on the worker across all three splits (unique case_number donor; repeat case_title with a 365-day offset): 0 rows covered, 0 mismatches, 0 ambiguous on both probes and all splits. Rows are unique notified cases and every feature is a same-row attribute, so no outcome-bearing cross-row exposure is constructed; the probes are a bounded mechanism, not a proof, and no broader attack search was run.

Structural qualification and baseline scores do not certify operational forecasting validity.

- The register retains no historical vintages (bulk feed since 2025-03-18; S3 objects expire after 30 days), so a reverse-history probe is not performable: this is retrospective research over the pinned 2026-10-27 snapshot, never a certified historical forecasting setup.
- Feature availability is fixture-verified at three cross-era points (M.877 1997, M.4731 2007 with its OJ prior notice, M.10188 2021) but not verified row-by-row against notification-era vintages; the sector taxonomy labels are current-vintage NACE Rev 2 applied across all eras.
- Training-label timing is unverified: labels are the register's current values, observed as of the fetch snapshot, with no availability ledger.
- Positives cluster by enforcement era and sector acquisition waves beyond the day-level event key; per-notification-year positive counts (1-22, median about 8) are reported beside every score.
- Prevalence falls across splits (train 4.01%, eval 2.60%, holdout 1.58%): the eval and holdout windows are prevalence-shifted relative to training, an out-of-distribution property reported, not hidden.
- Pending cases with neither an opener nor a terminal decision at fetch (33, overwhelmingly live 2020s filings) are censored and counted per split and year; their labels are unobserved, not negative, and censoring never decides another row's membership.
- The ever-adopted label keeps M.10188 positive despite its 2024-09-06 post-ECJ withdrawal of the opener; M.3333 stays positive on its 2007-03-01 opener with the 2004 pre-notification opener excluded by rule.
- The stock runner baseline trails the required sector-division comparator on the identical eval rows (0.6973 vs 0.7679; paired difference -0.0706, 95% CI [-0.1558, +0.0168], inconclusive with the observed gap negative). Headroom above that prior is NOT demonstrated by the packaged evidence; both numbers must be quoted together.

**Corrections to the historical documentation:**

- 2026-10-27/28 descriptor correction per the independent pre-flip audit (PUBLISH WITH CONDITIONS): meta.json and quality.json regenerated (retrospective-use honesty, metadata contradiction fixes, recipes shipped, repeated-transaction dependence disclosed); superseded artifact e5a98dfc9c05d0b0..., CSVs byte-identical; re-qualified as e96929ef by worker job ecm-requal-002 before any public visibility

Review: 2026-10-28; applies to v2026.10 / `e96929efbbc4fcb84d2986a7e32f83f9c5fec5395124439fb3404faff2e9e662`. Frozen data and tags are unchanged.
<!-- /dataset-factory:links -->

Website sources and release records are managed by the dataset publication pipeline.
