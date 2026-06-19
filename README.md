# Machine Learning Assignment 2: Applying ML Algorithms

## Project Overview
This project applies supervised and unsupervised machine learning algorithms to the Customer Personality Analysis dataset.  
The goal is to build regression, classification, and clustering models, then compare their performance using suitable evaluation metrics.

## Dataset
Dataset: Customer Personality Analysis  
File used in the notebook:

```text
data/marketing_campaign.csv
```

The dataset contains customer information such as income, spending habits, family size, purchase history, and campaign response.

## Notebook Contents
The notebook is organized into the following sections:

1. **Data Preprocessing**
   - Load and inspect the dataset
   - Check and handle missing values
   - Fill missing `Income` values using median imputation
   - Create new features:
     - `Age`
     - `TotalSpending`
     - `TotalChildren`
   - Remove unrealistic ages and zero-income rows
   - Encode categorical variables

2. **Regression**
   - Target variable: `TotalSpending`
   - Models used:
     - Linear Regression
     - Ridge Regression
     - Decision Tree Regressor
   - Evaluation metrics:
     - MSE
     - RMSE
     - R² Score

3. **Classification**
   - Target variable: `Response`
   - Models used:
     - Logistic Regression
     - K-Nearest Neighbors
     - Random Forest Classifier
   - Class imbalance was handled using SMOTE.
   - Evaluation metrics:
     - Accuracy
     - Precision
     - Recall
     - F1 Score
     - Balanced Accuracy
     - Confusion Matrix

4. **Clustering**
   - Features used:
     - `Income`
     - `TotalSpending`
     - `Age`
     - `TotalChildren`
   - StandardScaler was applied.
   - Elbow Method was used to choose the number of clusters.
   - K-Means was applied with `k = 4`.
   - PCA was used to visualize clusters in 2D.
   - Cluster profiling was created using the mean values of the selected features.

## How to Run the Project
1. Clone this repository or download it as a ZIP file.
2. Make sure the dataset is placed inside the `data` folder:

```text
data/marketing_campaign.csv
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook ML_Assignment2.ipynb
```

5. Run the notebook cells from top to bottom.

## Files in This Repository
```text
ML_Assignment2.ipynb
README.md
requirements.txt
data/marketing_campaign.csv
```

## Main Findings
- Regression models were compared to predict total customer spending.
- Classification models were compared to predict customer campaign response.
- Clustering was used to segment customers into groups based on income, spending, age, and children count.
- K-Means with 4 clusters provided a reasonable segmentation based on the Elbow Method.

## Author
Hasan Azir SH.
1320221651
