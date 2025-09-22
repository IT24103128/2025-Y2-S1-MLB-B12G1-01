# Hypertension Risk Prediction Project

## Overview
This project focuses on developing a predictive model for hypertension risk using machine learning techniques. The project includes comprehensive data preprocessing, feature engineering, and exploratory data analysis (EDA) to identify key factors associated with hypertension. The goal is to build a robust model that can accurately predict hypertension risk based on various clinical and lifestyle factors.

## Dataset Details
### Dataset: `hypertension_dataset.csv`
- **Source**: [hypertension_dataset.csv](https://www.kaggle.com/datasets/ankushpanday1/hypertension-risk-prediction-dataset)
- **Size**: 174,982 rows, 23 columns
- **Features**:
  - **Demographics**: Age, Gender, Education Level, Country
  - **Clinical Measurements**: 
    - BMI (Body Mass Index)
    - Blood Pressure (Systolic and Diastolic)
    - Cholesterol (Total, LDL, HDL, Triglycerides)
    - Glucose levels
    - Heart Rate
  - **Lifestyle Factors**:
    - Physical Activity Level
    - Alcohol Intake
    - Smoking Status
    - Salt Intake
    - Sleep Duration
    - Stress Level
  - **Medical History**:
    - Diabetes status
    - Family History of Hypertension
  - **Socioeconomic Factors**:
    - Employment Status
- **Target Variable**: Hypertension (Low/High)

## Group Members and Roles
1. **IT24103017** - Handling Missing Values and Encoding 
   - Label and one-hot encoding for categorical variables

2. **IT24103032** - Handling Imbalanced Data and Duplication
   - Applied SMOTE for handling class imbalance
   - Checked and removed duplicate entries

3. **IT24103026** - Feature Engineering
   - Created new features to enhance predictive power

4. **IT24102998** - Feature Scaling
   - Applied standardization to numerical features
   - Ensured all features have zero mean and unit variance
   - Processed both original and engineered numerical features

5. **IT24103128** - Feature Selection
   - Implemented multiple feature selection techniques:
     - Variance Threshold
     - Mutual Information
     - SelectKBest 
     - Random Forest Importance
   - Combined results to identify most predictive features

6. **IT24103139** - Dimensionality Reduction
   - Applied Principal Component Analysis (PCA)
   - Reduced feature space while preserving variance
   - Visualized explained variance ratios

## How to Run the Code

### Prerequisites
1. **Install necessary libraries**:
   - Required Python packages (install via pip):
     ```
     pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn matplotlib-venn
     ```

2. **Ensure dataset is in place**:
   - Place `hypertension_dataset.csv` in `./data/raw/` directory

3. **Run the notebook**:
   - Open `group_pipeline.ipynb` in Jupyter Notebook or JupyterLab
   - Execute all cells by clicking the "Run All" button or running cells sequentially

4. **Check outputs**:
   - Processed datasets will be saved in `./results/outputs/`
   - EDA visualizations will be saved in `./results/eda_visualizations/`

## Notes
- The preprocessing script automatically creates necessary directories (`results/outputs` and `results/eda_visualizations`)
- All visualizations are saved in PNG format with high resolution (300 DPI)
- The script includes print statements to track progress and confirm successful completion