# Clustering and Statistical Analysis of San Diego Parking Citations

## Overview
Analysis of 475,638 San Diego parking citations (2024) to identify distinct street-level enforcement typologies using K-means clustering and statistical inference.

**→ All analysis, code, and findings are in [`03-FinalProject.ipynb`](03-FinalProject.ipynb)**

---

## Authors
- Toby Zhang — Data curation, Software, Inference
- Rohan Marda — Data curation, Software, Modeling
- Luke Huang — Writing, Analysis, Visualization
- Tyler Wong — Writing, Analysis, Visualization

---

## Quick Start

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib scikit-learn scipy requests tqdm
```

### 2. Clone the repo and open the notebook
```bash
git clone <repo-url>
cd Group073_FA25
jupyter notebook 03-FinalProject.ipynb
```

### 3. Run all cells top to bottom
- The first cell will automatically download the raw data to `data/00-raw/`
- Processed data will be saved to `data/02-processed/`
- **Do not skip the first setup cell** — it downloads the raw data files required for the rest of the notebook

---

## Dataset
- **Source:** [City of San Diego Open Data Portal](https://data.sandiego.gov/datasets/parking-citations/)
- **Size:** 475,638 citations, 8 variables
- **Period:** January–December 2024

---

## Key Results
| Test | Result |
|------|--------|
| Optimal clusters (k) | **2** (via silhouette score) |
| Chi-square (violation types vs cluster) | p < 0.001 — significant |
| ANOVA (fine amounts across clusters) | p < 0.001 — significant |
| Cohen's d (effect size) | 0.219 — medium effect |

- **Cluster 0** — Typical streets: broad mix of violations, higher avg fine ($62.17)
- **Cluster 1** — Hotspot streets (e.g. Mission Blvd, 4th Ave): dominated by meter/loading zone violations, lower avg fine ($52.31)

---

## Project Video
https://drive.google.com/file/d/1cS1ebV9NzwmMCXe1jqe1JWw6uRpWBT9w/view?usp=drive_link
