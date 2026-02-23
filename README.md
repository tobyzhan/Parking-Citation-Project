# Clustering and Statistical Analysis of San Diego Parking Citations
**COGS 108 Final Project — Group 073, FA25**

## Overview
This project analyzes **475,638 parking citations** issued across San Diego in 2024 to identify distinct street-level enforcement patterns using K-means clustering and statistical inference.

**Key findings:**
- San Diego parking enforcement is highly concentrated — a small number of streets (hotspots like Mission Blvd, 4th Ave, Island Ave) generate a disproportionate share of citations and revenue (~$26.8M total in 2024)
- K-means clustering with engineered features (day-of-week, seasonal, and violation-type distributions) identified **2 meaningful street clusters**: typical low-activity streets vs. high-intensity enforcement hotspots
- Chi-square test (p < 0.001) confirmed clusters differ significantly in violation-type mix
- ANOVA (p < 0.001) confirmed clusters differ significantly in average fine amounts

## Authors
| Name | Role |
|------|------|
| Toby Zhang | Data curation, Software, Inference |
| Rohan Marda | Data curation, Software, Modeling |
| Luke Huang | Writing, Analysis, Visualization |
| Tyler Wong | Writing, Analysis, Visualization |

## Repository Structure
```
.
├── 00-ProjectProposal.ipynb     # Initial proposal
├── 01-DataCheckpoint.ipynb      # Data loading & cleaning
├── 02-EDACheckpoint.ipynb       # Exploratory data analysis
├── 03-FinalProject.ipynb        # Full analysis (main notebook)
├── modules/
│   └── get_data.py              # Data download helper
├── data/
│   ├── 00-raw/                  # Raw CSVs (downloaded, not edited)
│   └── 02-processed/            # Cleaned citations.csv
└── results/                     # Output figures
```

## Quickstart
1. **Install dependencies**
   ```sh
   pip install pandas numpy matplotlib scikit-learn scipy requests tqdm
   ```
2. **Run notebooks in order** — start with [03-FinalProject.ipynb](03-FinalProject.ipynb) for the full analysis. The first cell will automatically download raw data to `data/00-raw/`.

## Project Video
https://drive.google.com/file/d/1cS1ebV9NzwmMCXe1jqe1JWw6uRpWBT9w
