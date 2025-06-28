# DevelopersHub Corporation - AI/ML Engineering Internship Tasks

Welcome to the repository for my completed tasks for the AI/ML Engineering Internship at DevelopersHub Corporation. This collection showcases a range of projects, from fundamental data analysis and classical machine learning to modern large language model (LLM) implementation.

Each task is contained within its own folder, complete with the source notebook and a dedicated `README.md` file detailing the specific objectives, methods, and outcomes of that project.

---

## Completed Tasks Summary

### [Task 1: Exploring and Visualizing the Iris Dataset](./Task-1-Iris-EDA/)

-   **Objective:** A foundational exercise in loading, inspecting, and visualizing a dataset to understand its structure, distributions, and feature relationships.
-   **Skills Demonstrated:** Data loading (Pandas), descriptive statistics, and data visualization (Matplotlib, Seaborn).
-   **Outcome:** Successfully analyzed the Iris dataset, identifying key correlations and the clear separability of the `setosa` species through visual plots.

### [Task 2: Predict Future Stock Prices (Short-Term)](./Task-2-Stock-Prediction/)

-   **Objective:** To build a time-series regression model to predict the next day's closing stock price for a selected ticker (AAPL).
-   **Skills Demonstrated:** API data fetching (`yfinance`), time-series feature engineering, regression modeling (`RandomForestRegressor`), and model evaluation.
-   **Outcome:** Developed a model with a high R-squared score (>0.98), accurately tracking the next-day price movements. The analysis also acknowledged the limitations of such a simplified model for real-world trading.

### [Task 3: Heart Disease Prediction](./Task-3-Heart-Disease/)

-   **Objective:** To build and optimize a robust binary classification model to predict the presence of heart disease from patient data.
-   **Skills Demonstrated:** Advanced data cleaning for a messy, real-world dataset, one-hot encoding, model selection (baseline vs. advanced), hyperparameter tuning (`GridSearchCV`), and in-depth evaluation (Accuracy, Confusion Matrix, ROC-AUC).
-   **Outcome:** After a rigorous data cleaning and model optimization process, the final tuned Random Forest model achieved **85% accuracy** and an **AUC of 0.91**, showcasing a strong ability to distinguish between patient outcomes.

### [Task 4: General Health Query Chatbot](./Task-4-Health-Chatbot/)

-   **Objective:** To create a conversational AI that can answer general health questions safely and effectively using a Large Language Model (LLM).
-   **Skills Demonstrated:** Prompt engineering, implementing safety filters, working with LLMs via the `transformers` library, and 4-bit quantization for efficient model deployment.
-   **Outcome:** The final chatbot successfully provided informative answers while strictly adhering to a critical safety protocol: never giving direct medical advice and always including a disclaimer. This highlighted the importance of responsible AI development.

### [Task 6: House Price Prediction](./Task-6-House-Price-Prediction/)

-   **Objective:** To develop a regression model capable of predicting house prices based on various property features.
-   **Skills Demonstrated:** Preprocessing of mixed data types (numerical and categorical), building a `scikit-learn` pipeline, and training a powerful ensemble model (`GradientBoostingRegressor`).
-   **Outcome:** A predictive model was successfully built and evaluated using a real-world dataset (King County). Feature importance analysis identified `sqft_living`, `grade`, and `lat` (latitude) as the most influential factors, aligning with real-world intuition.

---

This portfolio represents my ability to tackle diverse problems in the AI/ML space and my commitment to producing clean, well-documented, and effective solutions.
