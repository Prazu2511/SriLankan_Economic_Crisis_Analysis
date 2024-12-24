# Sri Lankan Economic Crisis: Regression Analysis

## Project Overview
This project focuses on analyzing the Sri Lankan economic crisis using regression analysis. 
The dataset includes key economic indicators such as exports, imports, agriculture, tourism, tax and non-tax revenue, and external debts. 
The aim is to understand the relationships between these factors and their impact on the economy.

---

## Pre-processing Data

### 1. Data Preparation and Transformation

**1.1 Dataset Download:**
- Downloaded the dataset as an .xls file from the Central Bank of Sri Lanka

**1.2 Conversion to CSV:**
- Converted the .xls file into a .csv file for easier manipulation.

**1.3 Loading the Data:**
- Loaded the CSV file into a pandas DataFrame.

**1.4 Dropping Unnecessary Columns:**
- Identified and removed columns that were not relevant to the analysis.

**1.5 Transposing the Data:**
- Transposed the DataFrame to make columns into rows (years as rows) and rows into columns.

**1.6 Dropping Additional Columns:**
- Identified and dropped more unnecessary columns after transposing.

**1.7 Renaming Columns:**
- Renamed columns to shorter and more descriptive names for easier access.

### 2. Transformed Dataset Description
The dataset contains the following columns:
- **Exports**: Value of goods and services exported.
- **Imports**: Value of goods and services imported.
- **Agriculture**: Contribution of agriculture to the economy.
- **Tourism**: Revenue generated from tourism.
- **Revenue**: Income from taxes.
- **External Debts**: Total external debt obligations.

### 3. Handling Missing Values

**3.1 Checking for Null Values:**
- Detected missing values in the dataset.

**3.2 Replacing Missing Values:**
- Filled null values with the median of their respective columns, assuming the data might be skewed.


### 4. Data Visualization

**4.1 Line Plots:**
- Plotted line plots for years against key indicators such as:
- Agriculture
- Imports
- Exports
- Revenue

**4.2 Exploratory Data Analysis (EDA):**
- Analyze trends using visualization tools like Matplotlib and Seaborn.
- Identify correlations between variables using a heatmap.

**4.3 Correlation Heatmap:**
Generated a correlation heatmap to observe relationships between all columns.

**4.4 Modified Dataset:**
- Saving the dataset as a csv file.

---

## Regression Analysis

### 5. Post-EDA Steps: 
   
**5.1 Feature Scaling:**
- Used StandardScaler to standardize the dataset by scaling features to have a mean of 0 and a standard deviation of 1.
- This is essential for regression techniques like Lasso and Ridge, as they are sensitive to the scale of input data.

### 6. Regression Models:

- As multicollinearity exists, Lasso and Ridge Regularization models are used.
  **6.1 Linear Regression model:**
  - Performed Linear Regression on the attributes to understand the relationship between the features.
  - Used Standard Scaler to normalize the values.
  
**6.2 Lasso Regularization:**
- Performed Lasso Regularization, which adds an L1 penalty to reduce less important feature coefficients to zero, effectively performing feature selection.
- Hyperparameter alpha was tuned for optimal performance.

**6.3 Ridge Regularization:**
- Performed Ridge Regularization, which adds an L2 penalty to shrink feature coefficients, reducing multicollinearity and overfitting.
- Hyperparameter alpha was tuned similarly to Lasso.

### 7. Evaluation Metrics Calculation:

**7.1 Evaluated the performance of all models using the following metrics:**
- Mean Absolute Error (MAE): Measures the average magnitude of errors.
- Mean Squared Error (MSE): Squares errors, penalizing larger deviations more.
- R-squared (R²): Determines how well the model explains the variance in the data.

---

## Installation Instructions

### 8. Prerequisites
 **8.1 Python Version**: 3.8 or higher.
 **8.2 Libraries**: Install the necessary Python libraries using the command:

   ```bash
   pip install -r requirements.txt
```

---

## Usage Instructions

### 9. Running the Analysis
**9.1 Clone the repository:**
   ```bash
   git clone https://github.com/your_username/srilankan-economic-crisis.git
   ```
**9.2 Navigate to the project directory:**
   ```bash
   cd srilankan-economic-crisis
   ```
**9.3 Run the analysis script:**
   ```bash
   python analysis.py
   ```
   
---

## Future Scope
- Expand the dataset with more indicators.
- Further tuning (e.g., adjusting the alpha parameter) or using a hybrid model like ElasticNet may improve results.
- Build predictive models using time-series analysis.
- Create an interactive dashboard for visualizing insights.

---

## Results

**Lasso Model (L1 Regularization):**
- Suitable for feature selection as it can shrink less important features to zero.
- Performs well but might oversimplify by removing less significant predictors.
- Effective when you suspect that only a subset of features significantly impacts the target.
<img width="814" alt="Screenshot 2024-12-11 at 11 29 34 PM" src="https://github.com/user-attachments/assets/2922680d-fa10-4c54-aaf9-122802fb8572" />


**Ridge Model (L2 Regularization):**
- Handles multicollinearity better by penalizing large coefficients, making it robust against overfitting.
- Provides a better fit for the majority of the data but might not handle outliers as effectively.
<img width="809" alt="Screenshot 2024-12-11 at 11 29 53 PM" src="https://github.com/user-attachments/assets/b8a41e9b-9a73-47e0-985e-2c208dcaccb4" />

---

## Conclusion:

- Use Lasso when simplicity and feature selection are important.
- Use Ridge when you aim for a more robust overall fit, especially in the presence of multicollinearity.
 







