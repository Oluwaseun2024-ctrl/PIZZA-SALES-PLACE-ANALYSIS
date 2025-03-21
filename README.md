# PIZZA-SALES-PLACE-ANALYSIS
An Excel project analyzing a year's worth of sales from a fictitious pizza sales place. The dataset encompasses details such as pizza type, size, quantity, price, and ingredients. The goal is to derive actionable insights to inform strategic decisions and optimize overall operational effectiveness.

## Table of Contents
- [Project Overview](https://github.com/Oluwaseun2024-ctrl/PIZZA-SALES-PLACE-ANALYSIS/edit/main/README.md#project-overview)
- _Project Scope_
- Project Objectives
- Expected Outcome
- Document Purpose
- Use Case
- Data Source
- Data Cleaning and Processing
- Data Analysis
- Data Visualization
- Recommendation
- Conclusion

## Project Overview
This project involves an in-depth analysis of a year's worth of sales data from a fictitious pizza place. The analysis is performed using Excel, providing valuable insights to drive strategic decisions and optimize operational effectiveness.

## Project Objectives
The primary objectives of this analysis are:
- **Sales Analysis:** Understand sales patterns over the year, identifying peak times and high-demand periods.
- **Product Performance:** Evaluate which types and sizes of pizzas are most popular and generate the most revenue.
- **Customer Preferences:** Analyze ingredient popularity and preferences to refine the menu offerings.
- **Operational Insights:** Uncover inefficiencies and areas for improvement in operations and supply chain management.

## Data Source
The dataset for this project is sourced from Maven Analytics [website](https://app.mavenanalytics.io/datasets?search=pizz) designed specifically for practice purposes. It is presented in an Excel file with four tables (Order Details, Orders, Pizza Types, and Pizzas) comprising 48,620, 21,350, 32, and 96 rows respectively, and 4, 3, 4, and 4 columns respectively. The dataset includes key attributes essential for a comprehensive analysis, such as:

![](https://github.com/Oluwaseun2024-ctrl/PIZZA-SALES-PLACE-ANALYSIS/blob/main/Number%20of%20Customers%20Per%20Day.png)

```Average Quantity = Sum of quantity/Count of quantity = 1000/10 = 1```

```SQL
SELECT 
	Month_Name,
COUNT 
	(Complaint_ID) AS [Total No of Complaints]
FROM
	Financial_Consumer_Complaints
GROUP BY 
	Month_Name, 
	Month_Number
ORDER BY 
	Month_Number ASC
```

```PYTHON
# Define the number of columns dynamically
num_cols = data.select_dtypes(include=['number']).columns  # Example numeric columns
num_plots = len(num_cols)

# Calculate grid size
rows = (num_plots - 1) // 4 + 1  # Dynamically calculate rows for up to 4 columns per row
cols = min(4, num_plots)  # Limit columns to 4

plt.figure(figsize=(15, rows * 3))  # Adjust height based on the number of rows

for i, col in enumerate(num_cols, 1):
    plt.subplot(rows, cols, i)
    sns.boxplot(x=data[col])
    plt.title(col)

plt.tight_layout()
plt.show()
```

| Name | Age | Class |
| ---- | --- | ----- |
| Seun | 12 | Python |
| Moji | 10 | Data |
| Tobi | 15 | Media |
