# Sri Lankan Economic Crisis: Regression Analysis

## Project Overview
This project focuses on analyzing the Sri Lankan economic crisis using regression analysis. 
The dataset includes key economic indicators such as exports, imports, agriculture, tourism, tax and non-tax revenue, and external debts. 
The aim is to understand the relationships between these factors and their impact on the economy.

---

## Pre-processing Data

### 1. Data Preparation and Transformation

**Dataset Download:**
- Downloaded the dataset as an .xls file from the Central Bank of Sri Lanka

**Conversion to CSV:**
- Converted the .xls file into a .csv file for easier manipulation.

**Loading the Data:**
- Loaded the CSV file into a pandas DataFrame.

**Dropping Unnecessary Columns:**
- Identified and removed columns that were not relevant to the analysis.

**Transposing the Data:**
- Transposed the DataFrame to make columns into rows (years as rows) and rows into columns.

**Dropping Additional Columns:**
- Identified and dropped more unnecessary columns after transposing.

**Renaming Columns:**
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

**Checking for Null Values:**
- Detected missing values in the dataset.

**Replacing Missing Values:**
- Filled null values with the median of their respective columns, assuming the data might be skewed.


### 4. Data Visualization

**Line Plots:**
- Plotted line plots for years against key indicators such as:
- Agriculture
- Imports
- Exports
- Revenue

**Exploratory Data Analysis (EDA):**
- Analyze trends using visualization tools like Matplotlib and Seaborn.
- Identify correlations between variables using a heatmap.

**Correlation Heatmap:**
Generated a correlation heatmap to observe relationships between all columns.

**Modified Dataset:**
- Saving the dataset as a csv file.

---

## Regression Analysis

### 1. Post-EDA Steps: 
   
**Feature Scaling:**
- Used StandardScaler to standardize the dataset by scaling features to have a mean of 0 and a standard deviation of 1.
- This is essential for regression techniques like Lasso and Ridge, as they are sensitive to the scale of input data.

### 2. Regression Models:

- As multicollinearity exists, Lasso and Ridge Regression models are used.
  
**Lasso Regression:**
- Performed Lasso Regression, which adds an L1 penalty to reduce less important feature coefficients to zero, effectively performing feature selection.
- Hyperparameter alpha was tuned for optimal performance.

**Ridge Regression:**
- Performed Ridge Regression, which adds an L2 penalty to shrink feature coefficients, reducing multicollinearity and overfitting.
- Hyperparameter alpha was tuned similarly to Lasso.

### 3. Evaluation Metrics Calculation:

**Evaluated the performance of all models using the following metrics:**
- Mean Absolute Error (MAE): Measures the average magnitude of errors.
- Mean Squared Error (MSE): Squares errors, penalizing larger deviations more.
- R-squared (R²): Determines how well the model explains the variance in the data.

---

## Installation Instructions

### Prerequisites
1. **Python Version**: 3.8 or higher.
2. **Libraries**: Install the necessary Python libraries using the command:

   ```bash
   pip install -r requirements.txt


---

## Usage Instructions

### Running the Analysis
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/srilankan-economic-crisis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd srilankan-economic-crisis
   ```
3. Run the analysis script:
   ```bash
   python analysis.py
   ```
   
---

## Future Scope
1. Expand the dataset with more indicators.
2. further tuning (e.g., adjusting the alpha parameter) or using a hybrid model like ElasticNet may improve results.
3. Build predictive models using time-series analysis.
4. Create an interactive dashboard for visualizing insights.

---

## Results

**Lasso Model:**
- Suitable for feature selection as it can shrink less important features to zero.
- Performs well but might oversimplify by removing less significant predictors.
- Effective when you suspect that only a subset of features significantly impacts the target.
<img width="814" alt="Screenshot 2024-12-11 at 11 29 34 PM" src="https://github.com/user-attachments/assets/2922680d-fa10-4c54-aaf9-122802fb8572" />


**Ridge Model:**
- Handles multicollinearity better by penalizing large coefficients, making it robust against overfitting.
- Provides a better fit for the majority of the data but might not handle outliers as effectively.
<img width="809" alt="Screenshot 2024-12-11 at 11 29 53 PM" src="https://github.com/user-attachments/assets/b8a41e9b-9a73-47e0-985e-2c208dcaccb4" />

---

## Conclusion:

- Use Lasso when simplicity and feature selection are important.
- Use Ridge when you aim for a more robust overall fit, especially in the presence of multicollinearity.
 







