# MLB Salary Prediction with Regularized Regression

## Project Overview
This project predicts MLB player salary using season-level batting statistics from the Lahman baseball database. The goal was to evaluate whether player performance metrics such as games played, runs, batting average, and OPS could help explain variation in salary.

Originally completed as a group course project. This repository is organized as a portfolio version by Lana Robison to highlight the modeling workflow, feature engineering, regularized regression approach, and interpretation of model limitations.

## Tools Used
- R
- tidymodels
- tidyverse
- Lahman
- glmnet
- ggplot2

## Data
The analysis used the Lahman R package, specifically batting and salary data. Player-season records were created by joining batting statistics with salary information, removing missing values, and aggregating season-level player performance.

No raw external data file is required because the data comes from the Lahman package.

## Methods
- Joined MLB batting and salary data by player and season
- Removed missing salary records
- Aggregated player-season batting statistics
- Engineered baseball performance metrics including BA, OBP, SLG, and OPS
- Conducted exploratory analysis of salary relationships with batting metrics
- Split data into training and testing sets
- Built a tidymodels workflow using a glmnet regularized regression model
- Tuned penalty and mixture hyperparameters using cross-validation
- Evaluated model performance using RMSE, MAE, R-squared, and MAPE

## Key Results
The final model achieved a test R-squared of approximately 10.4%, indicating that the selected batting statistics explained a limited portion of salary variation. Games played and runs emerged as important predictors of salary.

The model showed that batting statistics alone do not fully explain MLB salary, which is reasonable because salary also depends on contract timing, service time, defensive value, position, age, injuries, free agency status, and market factors.

## Limitations
The model had limited predictive strength. Future improvements could include:
- Removing players with very low at-bat totals
- Adding pitching, fielding, position, and age variables
- Accounting for free agency and contract structure
- Modeling salaries separately by position
- Applying log transformation to salary
- Testing alternative models such as random forest or gradient boosting

## Repository Structure
- `analysis/`: Quarto source file or cleaned R analysis file
- `docs/`: modeling notes and project documentation
- `report/`: rendered project report PDF
- `outputs/`: selected model result summaries

## Portfolio Relevance
This project demonstrates feature engineering, regularized regression, cross-validation, model evaluation, and honest interpretation of limited model performance.
