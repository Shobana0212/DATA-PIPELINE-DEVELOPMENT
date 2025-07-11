
## 🏢 Internship Details

- **Company**: CODTECH IT SOLUTIONS  
- **Intern Name**: Shobana Balusamy
- **Intern ID**: CITS0D117  
- **Domain**: Data Science
- **Duration**: 4 Weeks  
- **Mentor**: Neela Santosh  

# 📊 ETL Pipeline using Pandas and Scikit-Learn

This project demonstrates a full **ETL (Extract, Transform, Load)** pipeline using Python. It is designed to show how raw data can be cleaned, transformed, and prepared for machine learning in a reproducible, automated, and scalable way.

---

## 📌 Objective

The objective of this project was to create an automated pipeline that performs:
- Data Extraction from a CSV file
- Data Preprocessing including handling of missing values and feature encoding
- Feature Scaling and Transformation
- Splitting into training and testing sets
- Saving the clean output for future model training

This project was built as a practical exercise to understand the essentials of data preparation using industry-standard tools such as **Pandas** and **Scikit-learn**.

---

## 🧰 Tools and Technologies Used

### 1. Software & Platform
- **Python 3.10+**
- **Jupyter Notebook** (via **Anaconda Distribution**)
- **Anaconda Navigator** – for environment and notebook management
- **JupyterLab / Jupyter Notebook Interface** – to write and run Python code interactively

### 2. Python Libraries
- `pandas`: For loading and manipulating datasets
- `scikit-learn`: For data preprocessing, transformation, and train-test splitting
- `numpy`: (used internally by scikit-learn)
- `SimpleImputer`: To handle missing values
- `OneHotEncoder`: To convert categorical data into numerical form
- `StandardScaler`: For scaling numeric features
- `ColumnTransformer` and `Pipeline`: To apply preprocessing steps efficiently

---

## 📁 Project Structure

```
etl_pipeline/
├── extended_sample_data.csv        # Original dataset
├── etl_pipeline.ipynb              # Main notebook performing ETL
├── X_train.csv                     # Transformed features for training
├── X_test.csv                      # Transformed features for testing
├── y_train.csv                     # Target variable for training
├── y_test.csv                      # Target variable for testing
└── README.md                       # Project description and instructions
```

---

## 🔄 Workflow Overview

### 1. Extract

The dataset `extended_sample_data.csv` was loaded using Pandas from the local directory. This dataset contains a mix of numeric and categorical data with some missing values.

```python
df = pd.read_csv("extended_sample_data.csv")
```

### 2. Transform

Data transformation included the following:

- **Handling missing values**:
  - Numeric: Imputed with the mean
  - Categorical: Imputed with the most frequent value
- **Categorical encoding**: Converted to binary format using OneHotEncoder
- **Feature scaling**: Numeric data was scaled to standard normal distribution
- **Pipeline construction**: Used `ColumnTransformer` and `Pipeline` from scikit-learn to apply transformations consistently

### 3. Load

The transformed data was split into train and test sets using `train_test_split()` and saved into separate CSV files using `to_csv()`.

```python
X_train.to_csv("X_train.csv", index=False)
y_train.to_csv("y_train.csv", index=False)
```

---

## ✅ Outcomes

The project successfully automated the data preparation pipeline, resulting in clean, encoded, and scaled datasets ready for model training and evaluation. This approach ensures that the same preprocessing steps are applied to both training and test data, reducing the risk of data leakage and improving reproducibility.

---

## 🚀 Future Improvements

- Add a step to log data quality metrics (missing rate, class balance, etc.)
- Extend the pipeline to handle date/time features
- Integrate model training and evaluation
- Deploy the pipeline as a REST API using Flask or FastAPI

---

## 🙌 Acknowledgments

This project was built using open-source Python tools and practices commonly used in real-world data science projects. Special thanks to the developers of Pandas and Scikit-learn for providing such powerful tools.

---
