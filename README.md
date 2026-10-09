# Retail Sales Analysis

> Note: This notebook includes explanations for every query, covering the logic behind the code, the purpose of each operation, and the reasoning behind the data cleaning and analysis decisions.
> 
## Overview
This project explores retail transaction data to identify sales patterns across product categories, payment methods and monthly sales trends. The goal is to demonstrate how data cleaning and exploratory data analysis (EDA) can turn raw data into meaningful business insights.

## Tools & Technologies
- Python — Programming language
- Pandas — Data manipulation and cleaning
- Matplotlib — Data visualization
- Jupyter Notebook — Analysis and documentation

## Project Workflow
1. Inspected the dataset structure, columns, and data types.
2. Identified and analysed missing values.
3. Checked for duplicate records.
4. Converted transaction dates into datetime format.
5. Validated recorded transaction totals against unit price and quantity.
6. Created a cleaned dataset while preserving useful records with incomplete fields.
7. Performed exploratory data analysis to compare sales across categories, payment methods, and months.
8. Created visualizations to communicate the findings.

## Key Findings
- Top-performing category: Butchers recorded the highest sales among product categories.
- Lowest-performing category: Milk Products recorded the lowest sales among product categories.
- Payment methods: Cash accounted for the highest recorded sales among the payment methods analysed.
- Monthly trends: Sales fluctuated over time, with a sharp decline in December 2024 that requires further investigation.

## Data Cleaning
The original dataset contained 12,575 rows and 11 columns.

- Identified missing values across several columns.
- Found no exact duplicate rows.
- Removed 604 rows where both `Quantity` and `Total Spent` were missing, leaving 11,971 rows.
- Retained rows with missing item names and unit prices when recorded transaction totals were available.
- Preserved missing discount statuses rather than assuming they indicated no discount.
- Converted `Transaction Date` to a datetime format.
- Verified that all 11,362 records with complete unit prices, quantities, and totals were consistent within a tolerance of 0.01.

## Visualizations
The project includes:
- Total recorded sales by product category
- Monthly recorded sales trends
- Total recorded sales by payment method

## Limitations
- Recorded sales do not represent profit because product costs are unavailable.
- The dataset contains missing item names, unit prices, and discount statuses.
- The interpretation of unit prices relative to discounts has not been independently verified.
- The decline in December 2024 requires further investigation before drawing conclusions about business performance.
- Findings are based on the available records and may not represent the complete underlying business activity.

## Dataset
Source: Retail Store Sales — Dirty for Data Cleaning, Kaggle.

[View the dataset on Kaggle](https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning)

Please refer to the original dataset page for its documentation and licence.

## How to Run
1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install pandas matplotlib jupyter
   ```

3. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `retail sales analysis.ipynb` and run the cells in order.
5. Place the dataset in the expected location or update the file path in the notebook.

## Conclusion
This project demonstrates the use of Python for data cleaning, validation, exploratory analysis, and visualization. It highlights how retail transaction data can be used to identify category-level performance, compare payment methods, and examine changes in monthly sales.

The project also demonstrates the importance of documenting data-quality issues and acknowledging limitations when interpreting analytical results.
