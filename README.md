# Supplementary Materials for *Point-Cloud Stockpile Inventory: A Review of Survey Workflows, Volumetry, and Change Detection*

This repository contains the supplementary review materials accompanying the manuscript:

> **Point-Cloud Stockpile Inventory: A Review of Survey Workflows, Volumetry, and Change Detection**

The review examines stockpile inventory as an integrated three-dimensional measurement workflow, linking acquisition geometry, point-cloud registration, pile and base-surface reconstruction, volumetric estimation, multitemporal change detection, uncertainty, and validation. Particular attention is given to mobile laser scanning and emerging robotic mapping systems.

The repository is intended to make the literature search, screening, evidence mapping, appraisal, and benchmarking framework transparent and reproducible.

---

## Repository Structure

| Directory                                                            | Contents                                                                                                                                  |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| [`S1_search_and_PRISMA/`](./S1_search_and_PRISMA/)                   | Search strategies, search records, deduplication information, and materials supporting the PRISMA-style identification and retrieval flow |
| [`S2_screening_and_adjudication/`](./S2_screening_and_adjudication/) | Record-level screening materials, reviewer decisions, agreement assessment, and adjudication information                                  |
| [`S3_evidence_map/`](./S3_evidence_map/)                             | Structured evidence map used to classify direct stockpile evidence, transferable methodological evidence, reviews, and data resources     |
| [`S4_evidence_appraisal/`](./S4_evidence_appraisal/)                 | Claim-specific evidence-appraisal framework, validation-maturity criteria, and study-level appraisal materials                            |
| [`S5_reporting_checklist/`](./S5_reporting_checklist/)               | Recommended reporting items for comparable benchmarking of repeated stockpile point-cloud surveys                                         |

---

## Review Design

The study was conducted as a **critical scoping review with a structured evidence map**.

The literature was organized into two principal evidence layers:

1. **Direct stockpile evidence**
   Studies in which three-dimensional observations were used directly to estimate stockpile volume, inventory, or material change.

2. **Transferable methodological evidence**
   Studies from adjacent areas such as SLAM, point-cloud registration, terrain modeling, change detection, calibration, and robotic mapping that address components of the stockpile acquisition-to-inventory workflow.

Transferable studies were interpreted only for the endpoints demonstrated in the original work and were not treated as direct evidence of stockpile volumetric accuracy.

---

## Search and Screening Summary

The final search update was completed on **September 1, 2026**, covering records published through **August 31, 2026**.

The review workflow identified:

* **797** source records before final deduplication
* **472** unique records entering screening
* **262** reports sought for retrieval
* **113** full reports assessed for eligibility
* **103** full reports retained in the structured evidence map

The 103 retained full reports comprised:

* **44** direct empirical stockpile or bulk-material studies
* **54** transferable-method studies
* **2** specialist reviews
* **3** data resources

The primary empirical synthesis therefore contained **98 full empirical reports**.

An additional **7 direct records** available only through formal abstracts or publisher previews were retained for narrowly defined qualitative interpretation and were excluded from numerical performance synthesis.

---

## Independent Screening

The same 472-record candidate set was independently screened by two reviewers.

The second reviewer did not have access to the first reviewer's record-level classifications during screening.

Agreement across the complete multicategory screening taxonomy was:

* **416/472 records**
* **88.1% exact agreement**
* **Cohen's \(\kappa = 0.837\)**

Records with discrepant classifications were reassessed against the prespecified eligibility criteria before final synthesis membership was assigned.

Detailed screening and adjudication materials are provided in [`S2_screening_and_adjudication/`](./S2_screening_and_adjudication/).

---

## Evidence Appraisal

Direct and transferable empirical studies were appraised across six domains:

1. independence and characterization of the reference system;
2. realism of the scene and pile geometry;
3. sample size, repetition, and remount or revisit design;
4. completeness of the acquisition-to-volume or acquisition-to-change workflow;
5. treatment of uncertainty, missing support, and failure cases; and
6. availability of data, parameters, or implementation detail.

The domains were assessed separately rather than combined into a single additive quality score.

Numerical claims were additionally classified according to their reference basis, including:

* known or independently quantified volume;
* independent high-grade surface or survey reference;
* intermethod agreement;
* internal geometric residual; and
* unverified operational quantity.

This distinction is important because similar percentage errors can represent substantially different forms of evidence.

The appraisal framework and study-level materials are available in [`S4_evidence_appraisal/`](./S4_evidence_appraisal/).

---

## Validation-Maturity Framework

The review uses five descriptive validation-maturity levels:

| Level  | Definition                                                                                                |
| ------ | --------------------------------------------------------------------------------------------------------- |
| **R1** | Algorithm demonstration without an independent reference                                                  |
| **R2** | Controlled experiment with known geometry or transformation                                               |
| **R3** | Field comparison against an independent reference                                                         |
| **R4** | Repeated operational validation across dates and operating conditions                                     |
| **R5** | Operational deployment with uncertainty-bearing results, exception handling, and inventory reconciliation |

Validation maturity is treated separately from evidential strength. A mature operational workflow does not necessarily provide an independent estimate of absolute volumetric error.

---

## Major Analytical Distinctions

The review distinguishes several quantities that are often combined in stockpile-mapping studies.

### Volume accuracy versus agreement

Agreement between UAV, TLS, MLS, or other surveying methods is not equivalent to absolute accuracy unless an independently characterized reference is available.

### Registration quality versus volumetric accuracy

A low registration residual describes geometric alignment with respect to the selected constraints. It does not by itself establish an unbiased stockpile-volume estimate.

### Observed versus modeled geometry

Occluded or inaccessible surfaces may be reconstructed through interpolation or other completion methods. The review therefore distinguishes directly observed geometry from model-derived geometry.

### Inventory change versus spatial change

For repeated surveys, the inventory-level change is defined from independently accepted single-epoch volumes,

$$
\Delta V_{\mathrm{pile}} = V_2 - V_1,
$$

whereas spatial change analysis identifies local material increase or decrease over valid common support.

The review further distinguishes:

* **observed geometric change**;
* **credible local change**; and
* **inventory-attributed change**.

A reconciliation residual is used to compare the independently estimated inventory change with spatially integrated local changes.

---

## Benchmarking Framework

The manuscript proposes a five-stage validation progression for mobile and autonomous stockpile-mapping systems:

1. **Component verification**
2. **Controlled stockpile reconstruction**
3. **Repeated unchanged acquisition**
4. **Controlled material change**
5. **Operational validation**

These stages are cumulative rather than interchangeable. Controlled reference experiments remain necessary even when a system has already been demonstrated in operational environments.

The associated reporting recommendations are provided in [`S5_reporting_checklist/`](./S5_reporting_checklist/).

---

## Scope and Limitations

The direct evidence base is strongest for UAV photogrammetry and terrestrial laser scanning. Evidence for handheld SLAM, mobile laser scanning, and especially autonomous ground-robot stockpile volumetry is smaller and more heterogeneous.

Accordingly, adjacent-domain evidence is used to examine mechanisms such as:

* trajectory estimation and SLAM;
* sensor calibration;
* multisession registration;
* geometric observability;
* terrain and base-surface modeling;
* point-cloud change detection;
* autonomous exploration and inspection; and
* uncertainty propagation.

Performance reported for these adjacent-domain tasks should not be interpreted as direct stockpile-volume performance.

The review did not statistically pool reported percentage errors because the studies differ substantially in target quantity, reference system, pile geometry, scale, acquisition conditions, and validation endpoint.

---

## Reproducibility

The supplementary materials are provided to support inspection of the review process, including:

* search and identification;
* deduplication;
* eligibility decisions;
* independent screening;
* adjudication;
* evidence classification;
* quantitative-result interpretation;
* evidence appraisal; and
* benchmark-reporting recommendations.

Where possible, record identifiers, DOI information, classifications, and methodological annotations are retained to allow individual review decisions to be traced.

Full-text copies of copyrighted publications are not redistributed through this repository.
