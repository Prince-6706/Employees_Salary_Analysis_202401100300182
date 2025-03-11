# Employees_Salary_Analysis_202401100300182
# Employee Salary Analysis - README

## Overview
This project analyzes employee salary data to gain insights into salary distribution, correlations, and trends based on factors such as age, experience, and department. The analysis uses Python and data visualization tools to present findings effectively.

## Project Details
- **Name:** Prince  
- **Branch:** CSE(AI)-C  
- **University Roll No.:** 202401100300182  
- **Class Roll No.:** 35  

## Purpose
The goal of this project is to:
- Understand salary distribution across departments.
- Examine the impact of experience on salary levels.
- Identify correlations between age, experience, and salary trends.
- Provide data-driven insights for improving salary structures and employee benefits.

## Scope
The analysis covers:
- Salary distribution across different departments.
- The relationship between experience and salary levels.
- Correlation between age and salary trends.
- Statistical insights derived from employee data.

## Methodology
1. **Data Collection**
   - The dataset consists of 20 employee records containing Employee ID, Age, Department, Experience, and Salary.
   - Data was sourced from company records and formatted for analysis.

2. **Data Preprocessing**
   - Handling missing values and outliers to ensure data integrity.

3. **Exploratory Data Analysis (EDA)**
   - Summary statistics (mean, median, standard deviation).
   - Visualization of salary distributions using histograms.
   - Boxplots for salary variations across departments.
   - Correlation analysis using scatter plots and matrices.

4. **Statistical Analysis**
   - Pearson correlation analysis between experience, age, and salary.
   - Comparative analysis of salary distributions by department.
   - Trend analysis using regression models.

5. **Data Visualization**
   - Histogram for salary distribution.
   - Boxplots for salary variations by department.
   - Heatmaps to visualize correlations.

## Code Implementation
The analysis is conducted using Python with the following libraries:
- **pandas** for data handling
- **matplotlib.pyplot** and **seaborn** for data visualization

### Sample Code
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load employee dataset
file_path = "employee_data.csv"
df = pd.read_csv(file_path)

# Salary statistics
print("Salary Statistics:")
print(df['Salary'].describe())

# Average salary by department
dept_salary = df.groupby('Department')['Salary'].mean()
print("\nAverage Salary by Department:")
print(dept_salary)

# Correlation between experience and salary
correlation = df[['Experience', 'Salary']].corr()
print("\nCorrelation between Experience and Salary:")
print(correlation)

# Salary distribution by department
plt.figure(figsize=(10, 6))
sns.boxplot(x='Department', y='Salary', data=df)
plt.title('Salary Distribution by Department')
plt.xticks(rotation=45)
plt.show()

# Scatter plot of Experience vs Salary
plt.figure(figsize=(10, 6))
sns.scatterplot(x='Experience', y='Salary', data=df)
plt.title('Experience vs Salary')
plt.xlabel('Years of Experience')
plt.ylabel('Salary')
plt.show()
```

## Results & Insights
- Salary distribution varies across departments.
- Experience positively correlates with salary growth.
- Departmental differences suggest a need for salary adjustments.

## Conclusion
This analysis provides key insights into employee salaries, helping organizations optimize salary structures and improve employee satisfaction. Future work may involve expanding the dataset and incorporating additional factors like job roles and performance metrics.



