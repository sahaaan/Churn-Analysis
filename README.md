# Churn Analysis

A customer churn analysis project using the Telco Customer Churn dataset. This project performs exploratory data analysis, handles class imbalance with SMOTE, trains multiple classification models (Decision Tree, Random Forest, XGBoost), and evaluates performance to identify key drivers of churn.

## Repository structure

- data/
  - WA*Fn-UseC*-Telco-Customer-Churn.csv # Telco customer churn dataset
  - processed/ # Cleaned and preprocessed datasets used for modeling
- notebooks/
  - churn_analysis.ipynb # Main analysis notebook with EDA and modeling
- src/ # Source code (data processing, training, evaluation)
- models/ # Trained model artifacts (.pkl files)
- reports/ # Generated reports and figures
- requirements.txt # Python dependencies
- README.md # Project overview (this file)

## Getting started

### Prerequisites

- Python 3.8+
- pip

### Install dependencies

```bash
pip install -r requirements.txt
```

Required packages:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn (for SMOTE)
- xgboost

### Run Jupyter notebooks

```bash
jupyter lab
```

or

```bash
jupyter notebook
```

## Data

The dataset used is the **Telco Customer Churn dataset** (`WA_Fn-UseC_-Telco-Customer-Churn.csv`) which contains customer information including:

- Demographics (gender, SeniorCitizen, Partner, Dependents)
- Services (PhoneService, InternetService, OnlineSecurity, etc.)
- Account information (tenure, Contract, PaymentMethod, MonthlyCharges, TotalCharges)
- Target variable: **Churn** (Yes/No)

### Data Preprocessing Steps

1. Removed `customerID` column (not useful for analysis)
2. Handled missing values in `TotalCharges` (replaced with 0)
3. Converted `TotalCharges` to float type
4. Addressed class imbalance using SMOTE oversampling

## Quick start: train a model

Open and run the `notebooks/churn_analysis.ipynb` notebook which includes:

1. **Data Loading and Understanding**

   - Load dataset and explore structure
   - Check data types and unique values

2. **Data Preprocessing**

   - Handle missing values
   - Drop irrelevant columns
   - Convert data types

3. **Exploratory Data Analysis (EDA)**

   - Statistical summaries
   - Numerical feature analysis
   - Target variable distribution (class imbalance detected)

4. **Feature Engineering**

   - Label encoding for categorical variables
   - SMOTE oversampling for class balance

5. **Model Training**

   - Decision Tree Classifier
   - Random Forest Classifier
   - XGBoost Classifier
   - Cross-validation scoring

6. **Model Evaluation**

   - Accuracy score
   - Classification report (precision, recall, F1-score)
   - Confusion matrix

7. **Model Persistence**
   - Save trained models using pickle

## What this repo does

- Loads and cleans Telco customer data
- Performs exploratory data analysis (EDA) to identify churn patterns
- Handles class imbalance using SMOTE technique
- Trains multiple classification models:
  - Decision Tree
  - Random Forest
  - XGBoost
- Evaluates models with accuracy, precision, recall, F1-score, and confusion matrix
- Saves trained models for deployment
- Produces visualizations and insights for stakeholders

## Key Findings

- **Class Imbalance**: The dataset shows imbalanced churn distribution (identified in EDA)
- **Models Used**: Decision Tree, Random Forest, and XGBoost classifiers
- **Technique Applied**: SMOTE oversampling to balance the dataset

## Contributing

Contributions are welcome. Please open issues or pull requests for bug reports, feature requests, or improvements.

Suggested workflow:

- Fork the repo
- Create a feature branch: `git checkout -b feat/your-feature`
- Commit changes and open a pull request

## License

Specify a license for your project (e.g., MIT). Add a LICENSE file to the repository.

## Contact

For questions or help, open an issue in this repository.
