📊 Data Cleaning and Exploratory Data Analysis Using Pandas

📌 Project Overview

This project demonstrates how to perform Data Cleaning and Exploratory Data Analysis (EDA) using Python and the Pandas library.

The program analyzes a student dataset containing names, departments, attendance percentages, and academic marks.

It identifies missing values, replaces them with appropriate statistical values, removes duplicate records, and performs descriptive statistical analysis.

The project also calculates department-wise average marks and generates a summary of student performance.

🎯 Objectives

- Understand data cleaning techniques using Pandas.
- Identify missing values in datasets.
- Handle missing data using mean imputation.
- Remove duplicate records.
- Perform descriptive statistical analysis.
- Calculate department-wise average marks.
- Analyze student attendance and academic performance.
- Understand fundamental Exploratory Data Analysis techniques.

🛠️ Technologies Used

- Programming Language: Python
- Library: Pandas
- Development Environment: Visual Studio Code
- Concepts: Data Cleaning, Data Preprocessing, Exploratory Data Analysis, Statistical Analysis

✨ Features

1. Dataset Creation

Creates a structured student dataset using a Pandas DataFrame.

2. Missing Value Detection

Identifies missing values using the "isnull()" function.

3. Missing Value Treatment

Replaces missing attendance and marks with their respective column averages using "fillna()".

4. Duplicate Removal

Removes duplicate records using "drop_duplicates()".

5. Descriptive Statistics

Generates statistical information, including count, mean, standard deviation, minimum, maximum, and quartiles.

6. Department-Wise Analysis

Calculates average marks for each department using "groupby()".

7. Exploratory Data Analysis

Displays the highest mark, lowest mark, average mark, and average attendance.

💻 Source Code

import pandas as pd

data = {
    "Name": ["Anitha", "Bala", "Chitra", "Dinesh", "Ezhil", "Fathima"],
    "Department": ["CSE", "CSE", "ECE", "CSE", "ECE", "CSE"],
    "Attendance": [92, 85, None, 88, 95, 90],
    "Mark": [86, 91, 78, None, 95, 82]
}

df = pd.DataFrame(data)

print("--- Original Dataset ---")
print(df)

print("\nMissing Values:")
print(df.isnull().sum())

# Missing value treatment
df["Attendance"] = df["Attendance"].fillna(df["Attendance"].mean())
df["Mark"] = df["Mark"].fillna(df["Mark"].mean())

# Remove duplicate records
df = df.drop_duplicates()

print("\n--- Cleaned Dataset ---")
print(df)

print("\n--- Descriptive Statistics ---")
print(df.describe())

print("\n--- Department-wise Average Marks ---")
print(df.groupby("Department")["Mark"].mean().round(2))

print("\n--- EDA Summary ---")
print("Highest Mark :", df["Mark"].max())
print("Lowest Mark :", df["Mark"].min())
print("Average Mark :", round(df["Mark"].mean(), 2))
print("Average Attendance :", round(df["Attendance"].mean(), 2))

📊 Sample Output

Original Dataset

      Name Department  Attendance  Mark
0   Anitha        CSE        92.0  86.0
1     Bala        CSE        85.0  91.0
2   Chitra        ECE         NaN  78.0
3   Dinesh        CSE        88.0   NaN
4    Ezhil        ECE        95.0  95.0
5  Fathima        CSE        90.0  82.0

Missing Values

Name          0
Department    0
Attendance    1
Mark          1
dtype: int64

Cleaned Dataset

      Name Department  Attendance  Mark
0   Anitha        CSE        92.0  86.0
1     Bala        CSE        85.0  91.0
2   Chitra        ECE        90.0  78.0
3   Dinesh        CSE        88.0  86.4
4    Ezhil        ECE        95.0  95.0
5  Fathima        CSE        90.0  82.0

Department-Wise Average Marks

Department
CSE    86.35
ECE    86.50
Name: Mark, dtype: float64

EDA Summary

Highest Mark : 95.0
Lowest Mark : 78.0
Average Mark : 86.4
Average Attendance : 90.0

⚙️ Installation and Execution

Step 1: Install Python

Ensure Python is installed on your computer.

Step 2: Install Pandas

Open the terminal in Visual Studio Code and execute:

py -m pip install pandas

Step 3: Save the Program

Save your Python code as:

main.py

Step 4: Run the Program

Execute:

py main.py

🔍 Working Principle

Step 1: Dataset Creation

Student information is stored in a Python dictionary and converted into a Pandas DataFrame.

Step 2: Missing Value Identification

The "isnull().sum()" function identifies the number of missing values in each column.

Step 3: Missing Value Treatment

Missing attendance and marks are replaced with the mean values of their respective columns.

Step 4: Duplicate Removal

The "drop_duplicates()" function removes repeated records.

Step 5: Statistical Analysis

The "describe()" function generates descriptive statistics for numerical columns.

Step 6: Department-Wise Analysis

The "groupby()" function groups students according to their departments and calculates average marks.

Step 7: EDA Summary

The program displays important statistical insights, including maximum marks, minimum marks, average marks, and average attendance.

🌍 Applications

- Student Performance Analysis
- Academic Data Management
- Educational Data Analytics
- Data Preprocessing
- Data Science Projects
- Statistical Data Analysis

🚀 Future Enhancements

- Import student records from CSV and Excel files.
- Visualize academic performance using Matplotlib.
- Create department-wise attendance reports.
- Identify students with low attendance.
- Develop an interactive data analytics dashboard.
- Export cleaned datasets to CSV files.
- Implement advanced data preprocessing techniques.

📚 Learning Outcomes

Through this project, I gained practical experience in:

- Creating and manipulating Pandas DataFrames.
- Identifying and handling missing values.
- Performing mean-based data imputation.
- Removing duplicate records.
- Generating descriptive statistics.
- Grouping and analyzing structured datasets.
- Performing basic Exploratory Data Analysis.

👨‍💻 Author

KARTHICK B

Computer Science and Engineering
Chennai Institute of Technology

📄 Conclusion

This project demonstrates essential data cleaning and exploratory data analysis techniques using Python and Pandas.

By handling missing values, removing duplicates, calculating descriptive statistics, and analyzing department-wise academic performance, the program provides a foundation for more advanced data analytics and machine learning applications.