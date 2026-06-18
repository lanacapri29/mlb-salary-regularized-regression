# Modeling Notes

## Objective
Predict MLB player salary using season-level batting statistics.

## Data Source
The project used the Lahman R package. Batting and salary data were joined by `playerID` and `yearID`.

## Feature Engineering
The analysis created several baseball performance metrics:
- Batting average (BA)
- On-base percentage (OBP)
- Slugging percentage (SLG)
- On-base plus slugging (OPS)

## Model
A regularized linear regression model was fit using `glmnet` through the tidymodels framework. The model tuned:
- `penalty`
- `mixture`

This allowed the model to test Elastic Net-style regularization.

## Evaluation
The model was evaluated using:
- RMSE
- MAE
- R-squared
- MAPE

The final model achieved a test R-squared of approximately 10.4%.

## Interpretation
Games played and runs were identified as important predictors of salary. However, the model explained only a limited amount of salary variation, suggesting that batting statistics alone are not enough to predict MLB salary accurately.

## Future Improvements
Potential improvements include:
- Filtering out players with fewer than 50 at-bats
- Adding position, age, fielding, and pitching variables
- Log-transforming salary
- Modeling salary by position group
- Incorporating contract and service-time variables
