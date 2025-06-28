# Task 1: Exploring and Visualizing the Iris Dataset

This project serves as a fundamental introduction to Exploratory Data Analysis (EDA).

### Objective
To load, inspect, and visualize the classic Iris dataset to understand data trends, distributions, and the relationships between its features.

### Dataset
-   **Name:** Iris Dataset
-   **Source:** Loaded directly via the Seaborn library.

### Key Steps
1.  **Data Loading:** The dataset was loaded into a Pandas DataFrame.
2.  **Initial Inspection:** Used `.shape`, `.columns`, and `.head()` to get a basic understanding of the data's structure.
3.  **Summary Statistics:** Employed `.info()` and `.describe()` to check for missing values and view statistical summaries of the numerical features.
4.  **Visualization:**
    -   A **Pair Plot** was used to visualize pair-wise relationships and distributions, colored by species.
    -   **Histograms** were plotted to show the distribution of each individual feature.
    -   **Box Plots** were created to identify the spread and potential outliers for each feature across the different species.

### Conclusion
The analysis successfully identified strong correlations, particularly between petal length and width, and demonstrated that the `setosa` species is linearly separable from the other two. The dataset was confirmed to be clean with no missing values, making it an excellent candidate for classification models.
