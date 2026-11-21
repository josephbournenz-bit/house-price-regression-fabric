# House Price Prediction with Multiple Linear Regression (Microsoft Fabric)

Group project from the Mission Ready Data Analysis Accelerator. The notebook predicts house prices from property features using a multiple linear regression (MLR) model, then compares it with a random forest regressor.

## My contribution
I took the data exploration and visualisation part of this group project: summary statistics, the Square Feet vs Price scatter plot, the price distribution histogram, the correlation heatmap, and the written insights for each chart. The modelling steps were completed together with my teammates.

## Dataset
500 houses with 7 features and a target (Price), supplied by the course:

| Column | Meaning |
|---|---|
| Square_Feet | Total area of the house |
| Num_Bedrooms / Num_Bathrooms / Num_Floors | Room and floor counts |
| Garage_Size | Size of the garage |
| Location_Score | Desirability of the location |
| Distance_to_Center | Distance to the city centre (km) |
| Price | Sale price (target) |

## Approach
1. Loaded the data into a pandas DataFrame and checked types and missing values (none found).
2. Explored it with summary statistics, a scatter plot, a histogram and a correlation heatmap.
3. Split the data 80/20 into training and test sets and trained an MLR model.
4. Trained a random forest (200 trees) and compared both models using RMSE.

## Results
| Model | RMSE on test set |
|---|---|
| Multiple linear regression | $63,952 |
| Random forest | $72,013 |

## Key findings
- Square_Feet and Num_Bedrooms have the strongest correlation with Price (about 0.56 each). Most other features are weakly correlated.
- Prices are roughly bell-shaped, ranging from about $277k to $961k, with no extreme outliers.
- MLR performed better than the random forest on this test set, suggesting the relationships in this data are largely linear.
- Both models tend to under-predict expensive homes and over-predict cheaper ones, pulling predictions toward the average.

## Tools
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Microsoft Fabric notebooks.

## Running the notebook
The data is loaded from course-provided cloud storage. The connection string has been removed from this repository. To rerun it, supply your own connection string through the AZURE_STORAGE_CONNECTION_STRING environment variable.
# house-price-regression-fabric
