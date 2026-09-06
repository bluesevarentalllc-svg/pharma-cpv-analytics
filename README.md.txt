# Pharmaceutical Continued Process Verification (CPV) Analytics Project

## Overview

This project demonstrates a synthetic pharmaceutical Continued Process Verification (CPV) workflow using historical-reference standardization, SPC run-rule detection, and change-point analysis.

The project is organized into two versions:

- **V1** — baseline CPV monitoring and dashboarding
- **V2** — advanced statistical monitoring using Nelson rules, automated SPC alerts, and change-point analysis

## Dataset

The analysis uses a synthetic pharmaceutical manufacturing dataset containing:

- API PSD D90
- Compression force
- Tablet hardness
- Tablet thickness
- Tablet weight
- Disintegration time
- Dissolution at 30 minutes

The dataset is synthetic and does not contain confidential manufacturing data.

## V1

V1 establishes the baseline CPV workflow using historical process behavior and dashboard-level statistical monitoring.

## V2

V2 extends the baseline workflow with:

1. Historical-reference Z-scores
2. Nelson SPC run-rule detection
3. Automated batch-level SPC signal counts
4. Detailed SPC alert tables
5. Change-point detection
6. Mean-shift estimation
7. SSE-reduction assessment
8. Meaningful-change screening
9. Integrated CPV dashboard visualization

## Key V2 Finding

The synthetic case shows a coordinated process transition around B019-B020.

Strong changes were detected in:

- API PSD
- Compression force
- Tablet hardness
- Disintegration time
- Dissolution

Tablet thickness and tablet weight remained comparatively stable.

The results identify statistical associations and process-transition patterns. They do not establish causality.

## Project Structure

```text
CPV Analytics Project/
├── README.md
├── data/
├── notebooks/
├── dashboards/
└── outputs/