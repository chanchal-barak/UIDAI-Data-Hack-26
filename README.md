# Jan-Sanket: Decoding Societal Signals for Smarter Governance

> **UIDAI Hackathon 2026 Submission**,
> *Theme: Unlocking Societal Trends*

![Project Status](https://img.shields.io/badge/Status-Prototype_Complete-success?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-Python_%7C_Pandas_%7C_GeoPandas-blue?style=for-the-badge)
![Impact](https://img.shields.io/badge/Focus-Social_Welfare_%26_Compliance-orange?style=for-the-badge)

## Overview
**Jan-Sanket** is a tool designed to identify invisible societal trends using aggregated Aadhaar administrative data. 

Instead of treating 'aadhar enrolment logs' as static records, we interpret them as high-fidelity signals of human behavior. Our solution detects **"Invisible Migrant's Motion"** and **"Biometric Compliance Gaps,"** enabling the government to shift from reactive service delivery to proactive resource allocation.

---

## Metrics

We developed two indices to normalize district-level data and identify anomalies:

### 1. Migration Intensity Index (MII)
Identifies districts serving as likely destinations for migrant workers.
* **Logic:** Districts with low natural growth (low child enrolment) but high adult demographic activity (address updates) indicate inward migration.
* **Formula:**
  $$MII = \frac{\text{Adult Demographic Updates (18+)}}{\text{Child Enrolment (0-5)}}$$
* **Utility:** Supports targeted planning for welfare portability schemes.

### 2. Bio-Update Lag (BUL)
Identifies districts with lower compliance rates for mandatory biometric updates among children.
* **Logic:** Compares the volume of mandatory biometric updates (ages 5-17) against the baseline child enrolment (ages 0-5) of the district.
* **Formula:**
  $$BUL = \frac{\text{Biometric Updates (5-17)}}{\text{Child Enrolment (0-5)}}$$
* **Utility:** Highlights areas requiring focused intervention to prevent service disruption for minors.

---

## Visual Insights
*(Placeholders - Upload your actual screenshots to your repo and link them here)*

| **Migration Analysis** | **Compliance Analysis** |
|:---:|:---:|
| ![Migration Map](path/to/migration_map.png) | ![Compliance Chart](path/to/compliance_chart.png) |
| *Heatmap showing migration intensity across districts.* | *Comparison of enrolment versus update compliance.* |

---

## Technology Stack
* **Core Analysis:** Python (Pandas, NumPy)
* **Visualization:** Matplotlib, Seaborn
* **Geospatial:** GeoPandas (for District-level mapping)
* **Reporting:** LaTeX (Automated PDF generation)

---

## Repository Bird's Eye View
```text
repo/
├── data/                  # Hidden to reduce repo size
├── src/                   # Source code for analysis
│   ├── data_loader.py     # Cleaning & Merging logic
│   ├── metrics.py         # MII and BUL calculations
│   └── visualize.py       # Plot generation
├── report/                # LaTeX Report Source
│   ├── main.tex           # Root LaTeX file
│   └── sections/          # Chapters (Methodology, Findings)
└── README.md              # Project Documentation