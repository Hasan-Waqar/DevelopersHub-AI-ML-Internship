# Task 2: Predict Future Stock Prices (Short-Term)

This project focuses on a time-series regression problem: predicting short-term stock price movements.

### Objective
To use historical stock data for Apple Inc. (AAPL) to build a machine learning model that predicts the next day's closing price.

### Dataset
-   **Name:** Apple Inc. (AAPL) Historical Stock Data
-   **Source:** Fetched via the `yfinance` Python library.

### Key Steps
1.  **Data Fetching:** Downloaded several years of daily stock data using the `yfinance` API.
2.  **Feature Engineering:** Created the target variable (`Target`) by shifting the `Close` price column by one day. This frames the problem as predicting tomorrow's close using today's information.
3.  **Data Splitting:** Split the data chronologically into training (80%) and testing (20%) sets to simulate real-world performance.
4.  **Model Training:** A `RandomForestRegressor` was trained on the features: `Open`, `High`, `Low`, `Close`, and `Volume`.
5.  **Evaluation & Visualization:** The model's predictions were plotted against the actual prices, and its performance was measured by R-squared and RMSE.

### Conclusion
The model achieved a very high R-squared score (>0.98), visually tracking the actual price trend with high fidelity. This success is largely attributed to the high auto-correlation of daily stock prices. The conclusion notes that while this is a great academic exercise, such a simple model should not be used for real financial trading as it lacks external market factors.
