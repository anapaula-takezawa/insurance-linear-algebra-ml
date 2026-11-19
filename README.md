# Insurance Data Protection — Linear Algebra & Machine Learning

**Author:** Ana Paula Takezawa 
**Program:** MBA in Data Science & Artificial Intelligence — TripleTen Brasil  
**Field:** Data Science | Machine Learning | Linear Algebra  
**Technologies:** Python | Pandas | NumPy | Scikit-learn | Matplotlib | Seaborn  
**Project Type:** Machine Learning | Predictive Modeling | Data Privacy

## Project Overview

This project explores how linear algebra and machine learning techniques can be applied to insurance customer data. Using a dataset provided by an insurance company, the analysis focuses on customer similarity, benefit prediction, and personal data protection through mathematical obfuscation.

The project demonstrates how data transformation techniques can protect sensitive information while preserving the predictive performance of machine learning models.

## Business Context

The insurance company **Sure Tomorrow** aims to improve its marketing strategy, predict customer benefits, and protect policyholders' personal information.

The analysis addresses four main tasks:

1. **Customer Similarity:** Identify customers with profiles similar to a given customer using K-Nearest Neighbors (kNN).
2. **Benefit Prediction:** Develop a machine learning model to predict whether a customer is likely to receive insurance benefits.
3. **Regression Modeling:** Apply linear regression to estimate the number of insurance benefits.
4. **Data Protection:** Implement a data obfuscation method using an invertible matrix and evaluate whether model predictions remain unchanged.

## Dataset

The project uses the `insurance_us.csv` dataset, which contains customer information.

**Features:**
- Gender
- Age
- Salary
- Number of family members

**Target variable:**
- `insurance_benefits`: Number of insurance benefits received by the customer over the last five years.

## Methodology

### 1. Data Exploration and Preparation
- Data loading and inspection
- Data type validation
- Missing values and duplicate analysis
- Statistical summary and data preparation

### 2. Customer Similarity — k-Nearest Neighbors
- Implementation of the kNN algorithm
- Euclidean and Manhattan distance metrics
- Comparison of results using original and scaled features
- Application of feature scaling with MaxAbsScaler

### 3. Machine Learning — Classification
- Transformation of the target variable into a binary classification problem
- kNN classifier implementation
- Comparison against a DummyClassifier baseline
- Model evaluation using F1-score and confusion matrix

### 4. Linear Regression
- Implementation of linear regression using NumPy
- Model evaluation using RMSE and R²
- Comparison between original and scaled data

### 5. Personal Data Protection — Obfuscation
- Generation of an invertible transformation matrix
- Application of the transformation to customer features
- Recovery of the original data using the inverse matrix
- Comparison of model predictions before and after obfuscation

## Key Results

The following results were obtained during the analysis:

| Model / Metric | Result |
|---|---:|
| kNN Classification — F1-score | 0.9354 |
| Linear Regression — RMSE | 0.364 |
| Linear Regression — R² | 0.423 |
| Obfuscated Data — RMSE | 0.364 |
| Obfuscated Data — R² | 0.423 |

The regression results remained unchanged after applying the invertible matrix transformation, demonstrating that this mathematical obfuscation approach preserved the model's predictive performance in the experiment.

## Technologies and Libraries

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Repository Structure

```text
insurance-linear-algebra-ml/
│
├── data/
│   ├── README.md
│   └── insurance_us.csv
│
├── insurance_linear_algebra_professional.ipynb
│
└── README.md
```

## How to Run

1. Clone this repository.
2. Open the Jupyter Notebook in Google Colab or a local Jupyter environment.
3. Upload or place the dataset `insurance_us.csv` in the `data/` directory.
4. Run the notebook cells sequentially.

## Important Considerations

The matrix transformation explored in this project demonstrates mathematical data obfuscation, not cryptographic security or guaranteed anonymization. Additional security measures and privacy assessments would be necessary before applying such a technique to real customer data.

## Conclusion

This project demonstrates the application of linear algebra and machine learning to practical insurance business challenges.

The results show that an invertible matrix transformation can change the representation of customer data while preserving the predictions of a linear regression model under the tested conditions.

The analysis highlights the importance of combining predictive modeling, mathematical foundations, and data protection considerations in responsible data science.
