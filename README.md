# Sri Lankan Economic Crisis: Regression Analysis

## Project Overview
This project focuses on analyzing the Sri Lankan economic crisis using regression analysis. 
The dataset includes key economic indicators such as exports, imports, agriculture, tourism, tax and non-tax revenue, and external debts. 
The aim is to understand the relationships between these factors and their impact on the economy.

---


## Exploratory Data Analysis (EDA)

### Preprocessing Data

#### Data Preparation and Transformation

**Dataset Download:**
- Downloaded the dataset as an .xls file from the Central Bank of Sri Lanka
  
**Conversion to CSV:**
- Converted the .xls file into a .csv file for easier manipulation.
  
**Reading the Data:**
- Loaded the CSV file into a pandas DataFrame.

**Dropping Unnecessary Columns:**
- Identified and removed columns that were not relevant to the analysis.

**Transposing the Data:**
- Transposed the DataFrame to make columns into rows (years as rows) and rows into columns.

**Dropping Additional Columns:**
- Identified and dropped more unnecessary columns after transposing.

#### Handling Missing Values

**Checking for Null Values:**
- Detected missing values in the dataset.

**Replacing Missing Values:**
- Filled null values with the median of their respective columns, assuming the data might be skewed.


#### Data Cleaning and Visualization

**Renaming Columns:**
- Renamed columns to shorter and more descriptive names for easier access.

**Line Plots:**
- Plotted line plots for years against key indicators such as:
- Agriculture
- Imports
- Exports
- Revenue
  
**Example library used:** 
Matplotlib and Seaborn.

**Correlation Heatmap:**
Generated a correlation heatmap to observe relationships between all columns.




### Dataset Description
The dataset contains the following columns:
- **Exports**: Value of goods and services exported.
- **Imports**: Value of goods and services imported.
- **Agriculture**: Contribution of agriculture to the economy.
- **Tourism**: Revenue generated from tourism.
- **Tax Revenue**: Income from taxes.
- **Non-Tax Revenue**: Income from non-tax sources.
- **External Debts**: Total external debt obligations.

---

## Goals
1. Perform exploratory data analysis to identify key trends and patterns.
2. Build and evaluate regression models to predict the target variable.
3. Derive actionable insights about the relationships between economic indicators.

---

## Installation Instructions

### Prerequisites
1. **Python Version**: 3.8 or higher.
2. **Libraries**: Install the necessary Python libraries using the command:

   ```bash
   pip install -r requirements.txt
  

### Dataset
Ensure the dataset file (`sri_lankan_economy.csv`) is placed in the project directory.

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

## Methodology

## Exploratory Data Analysis (EDA)
- Analyze trends using visualization tools like Matplotlib and Seaborn.
- Identify correlations between variables using a heatmap.

### 2. Preprocessing
- Handle missing values.
- Standardize data for consistent scaling.
- Check for multicollinearity.

### 3. Regression Models
- Build models such as:
  - Linear Regression
  - Ridge Regression
  - Decision Trees
- Evaluate performance using metrics:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - R-squared

---

## Results
- Key insights about the economic indicators and their impact on the crisis.
- Model evaluation results with visualizations.

### Example Visualization: Correlation Heatmap
```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.heatmap(data.corr(), annot=True, cmap="coolwarm")
plt.show()
```

---

## Future Scope
1. Expand the dataset with more indicators.
2. Use advanced regression models such as Lasso or ElasticNet.
3. Build predictive models using time-series analysis.
4. Create an interactive dashboard for visualizing insights.

---

## Contributors
- **[Your Name]** ([GitHub Profile](https://github.com/your_username))

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
