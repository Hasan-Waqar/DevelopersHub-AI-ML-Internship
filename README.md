# DevelopersHub Corporation - AI/ML Engineering Internship Project Portfolio

## Introduction

This repository documents the projects completed during my AI/ML Engineering Internship at DevelopersHub Corporation. The tasks cover a diverse range of machine learning concepts, from fundamental data analysis and classical regression/classification to modern applications of Large Language Models (LLMs) through prompt engineering.

Each project is self-contained in its respective folder, including the source Jupyter Notebook. This report provides a consolidated summary of the objectives, methodologies, key findings, and challenges encountered for each task.

---

## Table of Contents
1.  [Task 1: Exploring and Visualizing the Iris Dataset](#task-1-exploring-and-visualizing-the-iris-dataset)
2.  [Task 2: Stock Price Prediction (Short-Term)](./#task-2-stock-price-prediction-short-term)
3.  [Task 3: Heart Disease Prediction](./#task-3-heart-disease-prediction)
4.  [Task 4: General Health Query Chatbot](./#task-4-general-health-query-chatbot)
5.  [Task 6: House Price Prediction](./#task-6-house-price-prediction)

---

## Task 1: Exploring and Visualizing the Iris Dataset

-   **Objective:** To perform a foundational Exploratory Data Analysis (EDA) on the classic Iris dataset to understand its structure and identify key feature relationships.
-   **Methodology:**
    -   Loaded the dataset using the `seaborn` library.
    -   Used `pandas` for initial inspection (`.info()`, `.describe()`).
    -   Created visualizations using `matplotlib` and `seaborn`, including pair plots, histograms, and box plots to analyze distributions and correlations.
-   **Key Findings:**
    -   The dataset was found to be clean with no missing values.
    -   A strong positive correlation exists between `petal_length` and `petal_width`.
    -   The `setosa` species is linearly separable from `versicolor` and `virginica`, making the dataset highly suitable for classification tasks.
-   **Challenges:** This was a straightforward introductory task with no significant challenges.

---

## Task 2: Stock Price Prediction (Short-Term)

-   **Objective:** To build a time-series regression model to predict the next day's closing price for Apple Inc. (AAPL) stock.
-   **Methodology:**
    -   Fetched historical daily stock data using the `yfinance` API.
    -   Engineered the target variable by shifting the `Close` price to create a supervised learning problem.
    -   Split the data chronologically to prevent look-ahead bias.
    -   Trained a `RandomForestRegressor` model using `Open`, `High`, `Low`, `Close`, and `Volume` as features.
    -   Evaluated the model using R-squared and visualized the predictions against actual prices.
-   **Key Findings:**
    -   The model achieved an exceptionally high R-squared score (>0.98), indicating it could track the next-day price with high accuracy.
    -   This high performance is primarily due to the strong auto-correlation of daily stock prices (i.e., tomorrow's price is very close to today's).
    -   The final analysis concludes that while successful as an exercise, this simple model is not suitable for real-world trading due to its lack of external market indicators and sentiment analysis.

---

## Task 3: Heart Disease Prediction

-   **Objective:** To develop and optimize a robust binary classification model to predict the presence of heart disease.
-   **Methodology:**
    -   Used the Heart Disease UCI dataset from Kaggle, which presented significant data quality issues.
    -   Conducted an intensive data cleaning process, handling non-standard missing values (`?`), imputing data, and correctly separating categorical and numerical features.
    -   A `RandomForestClassifier` was chosen after a baseline Logistic Regression model performed poorly.
    -   Optimized the model using `GridSearchCV` to find the best hyperparameters.
    -   Evaluated the final model on accuracy, precision, recall, F1-score, and ROC-AUC.
-   **Key Findings:**
    -   The initial model was heavily biased, predicting only the majority class.
    -   After switching to a Random Forest and performing hyperparameter tuning, the final model's performance improved dramatically, achieving **85% accuracy** and an **AUC of 0.91**.
    -   The final model was well-balanced and demonstrated a strong ability to correctly identify both positive and negative cases.
-   **Challenges:**
    -   The primary challenge was the data cleaning phase. The dataset contained empty columns and non-standard missing values, which caused initial models to fail entirely. This required a careful, evidence-based debugging process to create a working data pipeline.

---

## Task 4: General Health Query Chatbot

-   **Objective:** To build a conversational AI using a Large Language Model (LLM) that can answer general health questions in a safe and helpful manner.
-   **Methodology:**
    -   Utilized an open-source, instruction-tuned LLM (`Mistral-7B-Instruct-v0.2` or `Zephyr-7B-Beta`) via the Hugging Face `transformers` library.
    -   Applied **prompt engineering** to define the chatbot's persona and enforce safety rules.
    -   A critical **safety filter** was implemented in the prompt, instructing the model to never provide direct medical advice and to always include a disclaimer recommending consultation with a healthcare professional.
    -   Used 4-bit quantization to efficiently run the large model on a free Google Colab GPU.
-   **Key Findings:**
    -   The prompt-engineered chatbot successfully provided informative and contextually relevant answers.
    -   The safety filter was highly effective, as the chatbot correctly refused to give direct medical advice and consistently appended the required disclaimer.
-   **Challenges:**
    -   The setup process involved handling gated model access on Hugging Face and resolving environment-specific library conflicts (`bitsandbytes`), which are common hurdles in practical LLM application.

---

## Task 6: House Price Prediction

-   **Objective:** To create a regression model to predict house prices based on property features from the King County House Sales dataset.
-   **Methodology:**
    -   Preprocessed the data by dropping non-predictive columns and defining the feature set (`X`) and target (`y`).
    -   Since the features were all numerical, `StandardScaler` was applied to standardize their scales.
    -   Trained a `GradientBoostingRegressor`, a powerful ensemble model well-suited for tabular data.
    -   Evaluated the model using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
    -   Visualized the results with a scatter plot of actual vs. predicted prices and a feature importance plot.
-   **Key Findings:**
    -   The model performed very well, with the visualization showing a strong, linear relationship between predicted and actual prices.
    -   Feature importance analysis correctly identified `sqft_living`, `grade` (construction quality), and `lat` (latitude) as the most significant predictors of price, confirming that size, quality, and location are key drivers in the real estate market.
-   **Challenges:**
    -   An initial attempt with a randomly generated dataset resulted in a poor, underfitting model. The challenge was recognizing that the issue was with the **data quality**, not the model itself. Switching to a high-quality, real-world dataset (King County) immediately produced a successful outcome.
 

---

## Internship Summary and Key Takeaways

This portfolio of projects demonstrates a comprehensive journey through key areas of modern AI and Machine Learning. The tasks progressed from fundamental data analysis to complex model optimization and the practical application of Large Language Models.

**Key skills and concepts covered include:**
-   **Data Science Fundamentals:** Exploratory Data Analysis, data cleaning, feature engineering, and visualization.
-   **Classical Machine Learning:** Building and evaluating both regression (Tasks 2 & 6) and classification (Task 3) models.
-   **Advanced Modeling Techniques:** Implementing powerful ensemble models like Random Forest and Gradient Boosting, and systematically optimizing them with hyperparameter tuning (`GridSearchCV`).
-   **Generative AI & LLMs:** Applying prompt engineering to control the behavior of a pre-trained LLM and implementing critical safety filters for a real-world application (Task 4).
-   **Problem-Solving and Debugging:** Successfully navigating and resolving complex, real-world challenges related to poor data quality and difficult software environments.

The successful completion of these tasks has provided a robust, hands-on foundation in the end-to-end machine learning lifecycle. I am confident in my ability to approach new AI/ML problems with a structured, analytical, and results-oriented mindset.
