# House Price Predictor
 
Regression models to predict California house prices, comparing
Linear Regression with Random Forest using scikit-learn.
 
## Dataset
California Housing sample dataset (included with Google Colab,
~17,000 rows, derived from the 1990 US Census).
Target: `median_house_value`.
 
## What I did
1. Explored the data (no missing values)
2. Split into 80% train / 20% test (random_state=42 for reproducibility)
3. Trained Linear Regression as a baseline
4. Trained Random Forest and compared both on the same test set
 
## Results
| Model | MSE | R² | RMSE |
|---|---|---|---|
| Linear Regression | 4.63e9 | 0.664 | ~$68,000 |
| Random Forest | 2.44e9 | 0.823 | ~$49,400 |
 
Random Forest reduced the typical prediction error by about 27%.
 
## Key learnings
- A baseline model is useful to measure improvement against
- Both models must be evaluated on the same test split
- Non-linear models capture location-based price patterns better
- Results vary slightly with a different random seed
 
## Limitations
- Data is from 1990, so prices do not reflect today's market
- No hyperparameter tuning or cross-validation yet
 
## Tools
Python, pandas, scikit-learn, Google Colab
 
## How to run
Open the notebook in Google Colab and run all cells.
The dataset is already available at /content/sample_data/.
