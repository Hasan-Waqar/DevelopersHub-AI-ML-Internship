# Task 3: Heart Disease Prediction

This project tackles a real-world binary classification problem in the critical domain of healthcare.

### Objective
To build, evaluate, and optimize a machine learning model to predict the presence of heart disease based on patient health attributes.

### Dataset
-   **Name:** Heart Disease UCI Dataset
-   **Source:** Kaggle.

### Key Steps
1.  **Intensive Data Cleaning:** The project started with a messy dataset that required a rigorous, iterative process to handle non-standard missing values (`?`), impute data, and correctly identify categorical vs. numerical features.
2.  **Preprocessing:** A `scikit-learn` Pipeline was used to apply `StandardScaler` to numerical features and `OneHotEncoder` to categorical features, ensuring a robust and leak-proof workflow.
3.  **Model Selection:** A baseline Logistic Regression model was initially trained, which performed poorly. A more powerful `RandomForestClassifier` was then chosen for optimization.
4.  **Hyperparameter Tuning:** `GridSearchCV` was employed to systematically search for the best hyperparameters for the Random Forest model, significantly boosting its performance.
5.  **In-depth Evaluation:** The final model was evaluated using Accuracy, a Classification Report, a Confusion Matrix, and the ROC-AUC score.

### Conclusion
The final tuned model achieved an impressive **85% accuracy** and an **AUC of 0.91**. This demonstrated a strong and well-balanced ability to predict heart disease, showcasing a complete and professional end-to-end machine learning workflow.
