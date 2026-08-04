# Slay the Spire — Modeling Card-Selection Decisions

## Overview
This project explores whether card-selection decisions in Slay the Spire (a roguelike deckbuilding game) can be modeled as a sequential decision process. Using community-shared run-log data, the goal is to:
1. Predict which card a player is likely to pick, given the game state at that decision point.
2. (Planned extension) Evaluate how much a given pick affects the player's downstream chances of winning.

This is a personal portfolio project built to develop and demonstrate end-to-end data science skills: data engineering from messy nested data, rigirous machine learning methodology, and interpretable modeling.

## Data
Source: a community-shared dataset of 77M+ Slay the Spire runs, originally posted on Reddit and hosted on Google Drive by the game's internal metrics maintainer.

- Original post (context, file naming convention, licensing notes): [Reddit post](https://www.reddit.com/r/slaythespire/comments/jt5y1w/77_million_runs_an_sts_metrics_dump/)
- Data download: [Google Drive folder](https://drive.google.com/drive/folders/1c7MwTdLxnPgvmPbBEfNWa45YAUU53H0l?usp=sharing)

Raw data is not included in this repository (see `.gitignore`) due to size. To reproduce this project, download one or more `.json.gz` files from the Drive folder above and place them in `data/raw/`.

## 
The first pipeline pass is scoped to a single character (Ironclad), since card pools differ substantially by character. The same pipeline is intended to be repeated for the other three characters afterward.

## Project structure
​```
data/raw/          # raw downloaded files (gitignored)
data/processed/    # cleaned tables generated from raw data
notebooks/         # analysis notebooks, one per project phase
src/               # reusable functions
requirements.txt   # Python dependencies
​```

## Setup
```bash
python -m venv venv
venv\Scripts\activate      # Windows
pip install -r requirements.txt
```

## Progress
- [x] Milestone 0: Project setup, data acquisition, initial data 
      inspection (`notebooks/00_data_inspection.ipynb`)
- [ ] Phase 1: Dataset construction
- [ ] Phase 2: Exploratory data analysis
- [ ] Phase 3: Baseline predictive model
- [ ] Phase 4: Model improvement and interpretation