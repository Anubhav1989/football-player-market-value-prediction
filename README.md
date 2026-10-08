# Football Player Market Value Prediction

Machine learning project for **CSE570: Machine Learning with Python** (LPU).

## Problem Statement
Football clubs spend large sums on transfers, so an accurate estimate of a
player's market value helps them avoid overpaying. This project builds a
regression model to predict a player's market value (in EUR) from profile
attributes (age, position, height, foot, league) and on-pitch performance
(goals, assists, minutes, cards), and identifies which factors drive value most.

## Dataset
- **Source:** Football Data from Transfermarkt (David Cariboo), Kaggle:
  https://www.kaggle.com/datasets/davidcariboo/player-scores
- **Licence:** CC0: Public Domain
- **Tables used:** players.csv (profiles and market value), appearances.csv
  (one row per player per game)
- **Size:** about 50,000 players and about 1.89 million appearance records
- **Data currency:** the dataset is current to July 2026 (updates are paused),
  so market values reflect mid-2026.
- **Note:** appearances.csv (about 198 MB) is not stored in this repo. Download
  it from the Kaggle link above and place it in the data/ folder.

## Approach
1. Data cleaning and visualization
2. EDA and statistical analysis
3. Feature engineering and preprocessing pipeline
4. Model development: [models to be added]
5. Evaluation and hyperparameter tuning
6. Saving the final model

## Results
[to be added]

## Author
Anubhav - M.Tech Data Science and Analytics, LPU
GitHub: https://github.com/Anubhav1989