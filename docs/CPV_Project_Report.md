# Continued Process Verification Analytics Project

## Executive Summary

This project demonstrates a synthetic pharmaceutical Continued Process Verification (CPV) analytics workflow designed to detect emerging process shifts using historical-reference standardization, statistical process control rules, and change-point analysis.

Two analytical versions were developed:

- V1: baseline CPV monitoring and dashboarding
- V2: advanced statistical monitoring using Nelson rules and change-point detection

The synthetic case shows a coordinated process transition around B019-B020.

Strong shifts were observed in API PSD, compression force, tablet hardness, disintegration time, and dissolution, while tablet thickness and tablet weight remained comparatively stable.

The analysis is intended to demonstrate statistical monitoring methodology and does not establish causal relationships.

## 1. Project Objective

The objective was to build a reproducible CPV analytics workflow capable of:

- establishing historical process behavior
- monitoring new batches against that reference
- identifying unusual statistical behavior
- detecting sustained process shifts
- providing interpretable batch-level alerts
- supporting focused process investigation

## 2. Dataset

The project uses a synthetic pharmaceutical manufacturing dataset containing 24 batches.

- B001-B018: historical reference period
- B019-B024: monitoring period

Variables include:

- API PSD D90
- Compression force
- Tablet hardness
- Tablet thickness
- Tablet weight
- Disintegration time
- Dissolution at 30 minutes

No confidential manufacturing data are used.

## 3. V1 — Baseline CPV Monitoring

V1 established the initial CPV monitoring workflow.

The baseline version focused on:

- data preparation
- historical process behavior
- standardized comparison of process variables
- dashboard visualization
- identification of emerging process variation

V1 provided the foundation for the more advanced V2 monitoring system.

## 4. Why V2 Was Developed

A process may show non-random behavior even before a simple control-limit check fully describes the pattern.

V2 was therefore developed to add:

- Nelson SPC run-rule detection
- automated batch-level SPC signals
- change-point detection
- quantitative assessment of mean shifts
- SSE-reduction analysis
- integrated statistical summary reporting

## 5. Historical-Reference Standardization

The 18 historical batches were used to calculate the reference mean and standard deviation for each monitored variable.

Each observation was standardized using:

Z = (Batch Result - Historical Mean) / Historical Standard Deviation

Monitoring batches were evaluated against this fixed historical reference.

## 6. Nelson SPC Rule Monitoring

Eight Nelson rules were implemented.

These rules detect patterns including:

- extreme excursions beyond ±3 sigma
- sustained shifts above or below the centerline
- increasing or decreasing trends
- alternating behavior
- clustering beyond ±1 or ±2 sigma
- unusually low variation
- mixture-like behavior

The rules were applied to monitoring batches without allowing the monitoring period to redefine the historical baseline.

## 7. Automated SPC Alerts

For each batch and variable, the dashboard identifies which Nelson rules are triggered.

A batch-level SPC signal count summarizes the number of variable-rule combinations triggered.

This signal count is intended as a monitoring indicator and should not be interpreted as a validated risk or severity score.

## 8. Change-Point Analysis

A single major mean change point was estimated for each monitored variable.

Candidate split points were evaluated by comparing the combined within-segment sum of squared errors.

The split producing the lowest total SSE was selected as the candidate process transition.

## 9. SSE-Reduction Assessment

The strength of the detected change point was evaluated by comparing:

- SSE from a single-mean model
- SSE from a two-segment change-point model

A high SSE reduction indicates that separating the process into pre-change and post-change regimes provides a substantially better description of the data.

## 10. Key V2 Findings

The strongest coordinated transition occurred around B019-B020.

### B019

Large shifts were detected in:

- API PSD
- Compression force
- Tablet hardness

These variables showed strong statistical departures from the historical reference.

### B020

Disintegration and dissolution showed their strongest detected regime changes around B020.

The overall pattern was:

API PSD increase  
→ compression force increase  
→ tablet hardness increase  
→ disintegration time increase  
→ dissolution decrease

Tablet thickness and tablet weight remained comparatively stable.

## 11. Meaningful-Change Screening

For this synthetic demonstration, a change was classified as meaningful when:

- absolute mean shift was at least 1 historical standard deviation
- SSE reduction was at least 50%

These thresholds were selected for demonstration purposes only.

They are not universal regulatory or industry acceptance criteria.

## 12. Interpretation

The temporal alignment of API PSD, compression force, hardness, disintegration, and dissolution supports focused process investigation.

However, the analysis does not prove causality.

A scientifically appropriate interpretation is:

The coordinated statistical shifts support investigation of material and process variables as potential contributors to the observed product-performance changes.

## 13. V1 vs V2

### V1 demonstrated

- baseline CPV monitoring
- historical process comparison
- dashboard-based process visibility

### V2 demonstrated

- automated SPC run-rule detection
- batch-level statistical alerts
- trend and pattern recognition
- change-point detection
- quantification of process-regime shifts
- integrated statistical interpretation

## 14. Limitations

This is a synthetic analytical case study.

A production CPV program would additionally require:

- validated data sources
- measurement-system assessment
- process-specific control limits
- scientifically justified alert thresholds
- investigation procedures
- quality-system governance
- change control
- subject-matter-expert review

## 15. Conclusion

The project demonstrates how CPV analytics can move beyond simple specification checking toward proactive identification of statistical process changes.

The combined use of historical-reference standardization, SPC run rules, and change-point analysis provides a structured framework for identifying when a process begins to behave differently and which variables should receive further investigation.
