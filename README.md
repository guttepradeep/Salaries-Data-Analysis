# Salaries-Data-Analysis
San Francisco Salaries Data Analysis
Project Overview
This project involves analyzing a dataset of public sector salaries in San Francisco. The dataset, sourced from Kaggle, contains information on employees' names, job titles, and various pay components, including base pay, overtime pay, and benefits. The analysis includes performing data cleaning, exploring key statistics, and answering specific questions related to the dataset.

Dataset
Source: San Francisco Salaries Dataset on Kaggle
File: Salaries.csv
Features:
Id: Unique identifier for each employee
EmployeeName: Name of the employee
JobTitle: Title of the job held by the employee
BasePay: Base salary
OvertimePay: Payment for overtime work
OtherPay: Other types of payments
Benefits: Employee benefits
TotalPay: Total payment received by the employee
TotalPayBenefits: Total payment including benefits
Year: Year of the record
Notes, Agency, Status: Additional information
Steps and Analysis
1. Display the Top 10 Rows of the Dataset
Used df.head(10) to inspect the first 10 rows.
2. Display the Last 10 Rows of the Dataset
Used df.tail(10) to inspect the last 10 rows.
3. Find the Shape of the Dataset
Displayed the number of rows and columns using df.shape.
4. Get Information About the Dataset
Used df.info() to get details like the number of columns, datatypes, and memory usage.
5. Check for Null Values
Used df.isnull().sum() to check the number of missing values in each column.
6. Drop Unnecessary Columns
Dropped columns Id, Notes, Agency, and Status using df.drop().
7. Get Overall Statistics About the Dataframe
Used df.describe() to get statistical details of numerical columns.
8. Find the Occurrence of Employee Names
Used df['EmployeeName'].value_counts().head() to find the top 5 most common employee names.
9. Find the Number of Unique Job Titles
Used df['JobTitle'].nunique() to count unique job titles.
10. Find the Number of Job Titles Containing 'Captain'
Used len(df[df['JobTitle'].str.contains('CAPTAIN')]) to count job titles containing the word 'Captain'.
11. Display Employee Names from Fire Department
Used df[df['JobTitle'].str.contains('FIRE DEPARTMENT', case=False)]['EmployeeName'] to filter and display employee names.
12. Find Minimum, Maximum, and Average BasePay
Replaced 'Not Provided' in BasePay with NaN and converted the column to float.
Used df['BasePay'].min(), df['BasePay'].max(), and df['BasePay'].mean() to find the minimum, maximum, and average base pay.
13. Replace 'Not Provided' in EmployeeName Column to NaN
Used df['EmployeeName'].replace('Not Provided', np.NaN, inplace=True) to clean the EmployeeName column.
14. Drop Rows Having 5 Missing Values
Dropped rows with 5 missing values using df.drop().
15. Find How Much ALBERT PARDINI Made (Including Benefits)
Filtered the dataset to find the total pay (including benefits) for ALBERT PARDINI.
Tools and Libraries Used
Pandas: For data manipulation and analysis.
NumPy: For numerical operations and handling missing data.
Conclusion
This project provided insights into the salary structure of San Francisco public sector employees. The analysis covered various aspects, including cleaning the dataset, exploring statistical details, and answering specific queries about the data
