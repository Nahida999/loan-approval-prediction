# Loan Approval Prediction Using Machine Learning

## Overview

This project uses supervised machine learning to predict loan approval outcomes based on applicant information. The project follows a complete machine-learning workflow, including dataset inspection, exploratory data analysis (EDA), data cleaning, preprocessing, model training, evaluation, and comparison.

Three classification algorithms are implemented and compared:

- Logistic Regression
- Decision Tree
- Random Forest

The purpose of the project is to analyse applicant data, prepare the dataset for machine learning, train multiple classification models, and compare their performance using standard evaluation metrics.

---

## Project Workflow

The project follows the following machine-learning workflow:

1. Dataset Inspection
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Data Preprocessing
5. Feature and Target Preparation
6. Train-Test Split
7. Feature Scaling
8. Model Training
9. Model Evaluation
10. Model Comparison

---

## Dataset

The dataset contains information about previous loan applicants and their loan approval outcomes.

The data includes applicant-related features such as:

- Age
- Gender
- Income
- Outgoings
- Postcode
- Loan approval status

Before developing the machine-learning models, the dataset was inspected, analysed, cleaned, and transformed to make it suitable for classification.

---

## Dataset Inspection

Before preprocessing and model development, the dataset was explored to understand its structure and identify potential data-quality issues.

The initial inspection included:

- Examining the number of rows and columns
- Reviewing the column names
- Checking data types
- Inspecting general dataset information
- Generating descriptive statistics for numerical features
- Identifying missing values
- Detecting duplicate records
- Examining the number of approved and rejected loan applications
- Checking unique values in categorical features
- Identifying potentially invalid categorical values

This initial inspection helped identify issues that needed to be addressed during the data-cleaning stage.

---

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to better understand the characteristics and distribution of the applicant data and identify relationships between different variables.

The analysis included:

- Loan approval distribution
- Applicant age distribution
- Gender distribution
- Outgoings distribution
- Loan approval by gender
- Correlation analysis between numerical features

Visualisations were created using Matplotlib and Seaborn to make patterns and distributions within the dataset easier to understand.

---

## Data Cleaning

Several data-quality issues were addressed before preparing the dataset for machine-learning models.

The cleaning process included:

- Removing duplicate records
- Removing the ID column because it was not useful for prediction
- Removing an invalid gender value
- Converting Income values into numerical format
- Identifying and handling missing values
- Replacing missing Age values using the median
- Replacing missing Income values using the median
- Replacing missing Outgoings values using the median
- Replacing missing Gender values using the mode
- Replacing missing Postcode values using the mode
- Replacing missing Approved values using the mode
- Removing unrealistic Outgoings values above 100,000
- Resetting the DataFrame index after cleaning
- Rechecking the dataset for missing values
- Checking the final dataset shape after cleaning

These steps helped improve the consistency and quality of the data before model development.

---

## Data Preprocessing

After cleaning, the dataset was transformed into a format suitable for machine-learning algorithms.

The preprocessing steps included:

- Removing the Postcode feature
- Encoding categorical Gender values using LabelEncoder
- Encoding the Approved target variable
- Separating the independent features (`X`) from the target variable (`y`)
- Splitting the dataset into training and testing sets
- Using an 80/20 train-test split
- Using a fixed random state for reproducibility
- Standardising numerical features using StandardScaler

Feature scaling was used to ensure that numerical features were represented on a comparable scale where required by the machine-learning models.

---

## Machine Learning Models

Three supervised machine-learning classification algorithms were implemented and compared.

### 1. Logistic Regression

Logistic Regression was trained to predict whether a loan application would be approved or rejected.

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Classification Report

### 2. Decision Tree

A Decision Tree classifier was trained using the processed applicant data.

Its performance was evaluated using the same metrics to allow comparison with the other classification algorithms.

### 3. Random Forest

A Random Forest classifier was trained and evaluated as an ensemble-based classification approach.

Its performance was compared with Logistic Regression and Decision Tree using the same evaluation metrics.

---

## Model Evaluation

Each machine-learning model was evaluated using several classification metrics rather than relying only on accuracy.

The evaluation metrics included:

- **Accuracy** – measures the overall proportion of correctly classified applications.
- **Precision** – measures how many applications predicted as positive were correctly classified.
- **Recall** – measures how many actual positive cases were correctly identified.
- **F1 Score** – provides a balance between precision and recall.
- **Confusion Matrix** – shows the numbers of correct and incorrect classifications across the classes.
- **Classification Report** – provides detailed precision, recall, and F1-score information for the classification results.

Using multiple evaluation metrics provides a more complete understanding of model performance.

---

## Model Performance

The three models produced the following results:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 64.86% | 67.41% | 77.14% | 71.95% |
| Decision Tree | 59.67% | 66.17% | 63.36% | 64.73% |
| Random Forest | 65.66% | 68.81% | 75.38% | 71.95% |

The results demonstrate differences in performance between the three classification algorithms.

Random Forest achieved the highest accuracy and precision among the tested models, while Logistic Regression achieved the highest recall. Logistic Regression and Random Forest produced very similar F1 scores.

The comparison demonstrates why multiple evaluation metrics are useful when assessing classification models.

---

## Technologies and Libraries Used

The project was developed using:

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Key Skills Demonstrated

This project demonstrates practical experience in:

- Python programming
- Data analysis
- Exploratory Data Analysis (EDA)
- Data visualisation
- Data cleaning
- Missing-value handling
- Data preprocessing
- Categorical encoding
- Feature preparation
- Feature scaling
- Train-test splitting
- Supervised machine learning
- Classification
- Logistic Regression
- Decision Trees
- Random Forest
- Model evaluation
- Confusion matrix analysis
- Performance metric comparison
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

```text
loan-approval-prediction/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── previousApplicants.csv
│
└── notebooks/
    └── loan-approval-prediction.ipynb
```

The Jupyter Notebook contains the complete analysis, preprocessing, model development, visualisations, and evaluation outputs.

The visualisations are stored directly within the notebook output, so a separate images folder is not required.

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Navigate to the project directory

```bash
cd loan-approval-prediction
```

### 3. Install the required dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

Open:

```text
notebooks/loan_approval_prediction.ipynb
```

using Jupyter Notebook, JupyterLab, or Visual Studio Code with the Jupyter extension installed.

### 5. Run the notebook

Run the notebook cells in order to reproduce the data analysis, preprocessing, model training, visualisations, and evaluation results.

---

## Repository Files

### `README.md`

Provides an overview of the project, methodology, machine-learning models, results, technologies, and instructions for running the project.

### `requirements.txt`

Contains the Python libraries required to run the project.

### `.gitignore`

Prevents unnecessary local Python, Jupyter, virtual-environment, and editor files from being committed to the repository.

### `data/previousApplicants.csv`

Contains the dataset used for the loan approval analysis.

### `notebooks/loan_approval_prediction.ipynb`

Contains the complete implementation, including:

- Dataset inspection
- Exploratory Data Analysis
- Data cleaning
- Data preprocessing
- Visualisations
- Feature preparation
- Model training
- Model evaluation
- Model comparison

---

## Author

**Nahida Sultana**

MSc Computer Science  
University of Chester