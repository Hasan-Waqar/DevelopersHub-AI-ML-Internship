# Task 6: House Price Prediction

This project focuses on solving a classic regression problem: predicting the sale price of houses.

### Objective
To build an effective regression model using various property features from the King County House Sales dataset.

### Dataset
-   **Name:** King County House Sales Dataset
-   **Source:** Kaggle.

### Key Steps
1.  **Feature Selection:** Relevant numerical features like `sqft_living`, `grade`, `bedrooms`, and geographical data (`lat`, `long`) were selected for modeling.
2.  **Preprocessing:** The data was cleaned by dropping non-predictive columns (`id`, `date`). `StandardScaler` was applied to all features to standardize their scale.
3.  **Model Training:** A powerful `GradientBoostingRegressor` ensemble model was trained on the preprocessed data.
4.  **Evaluation:** The model's performance was measured using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.
5.  **Visualization:** A scatter plot of Actual vs. Predicted prices was created to visually assess the model's accuracy. A feature importance plot was also generated.

### Conclusion
The trained model demonstrated strong predictive performance, with the scatter plot showing a tight, diagonal cluster of points that confirmed its accuracy across the price spectrum. The feature importance analysis correctly identified `sqft_living`, `grade`, and `lat` as the most influential predictors, aligning with real-world real estate knowledge.
