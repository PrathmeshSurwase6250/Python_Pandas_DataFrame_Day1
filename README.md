🐼 Python Pandas DataFrame — Day 1

A practical Pandas DataFrame practice repository containing 50 exercises divided into 5 progressive levels.

This repository is focused on building a strong foundation in Pandas DataFrame operations, including data loading, inspection, selection, filtering, sorting, and creating/updating columns.

📌 About

This project is part of my Python and Data Analysis learning journey.

I practiced Pandas using a students.csv dataset and solved 50 DataFrame problems, starting from basic DataFrame inspection and gradually moving toward data manipulation and transformation.

The exercises are divided into:

🟢 Level 1 — Loading & Inspection

🟢 Level 2 — Selecting Data

🟢 Level 3 — Filtering

🟡 Level 4 — Sorting

🟡 Level 5 — Creating & Updating Columns

🛠️ Technologies Used

🐍 Python

🐼 Pandas

🔢 NumPy

📓 Jupyter Notebook

📄 CSV Dataset

📚 Levels & Topics

🟢 Level 1 — Loading & Inspection

Questions 1–10

In this level, I practiced loading a CSV file and understanding the basic structure of a DataFrame.

Topics Covered

Importing Pandas

Reading CSV files

head()

tail()

shape

columns

dtypes

describe()

isnull()

duplicated()

Examples

import pandas as pd

students = pd.read_csv("students.csv")

students.head()
students.tail()
students.shape
students.columns
students.dtypes
students.describe()

Checking missing values:

students.isnull().sum()

Checking duplicate student IDs:

students[students["student_id"].duplicated()]

🟢 Level 2 — Selecting Data

Questions 11–20

This level focuses on selecting specific rows and columns from a DataFrame.

Topics Covered

Selecting a single column

Selecting multiple columns

loc[]

iloc[]

Selecting rows

Setting an index

Resetting an index

Filtering by gender

Examples

Select one column:

students["name"]

Select multiple columns:

students[["name", "course", "marks"]]

Using iloc:

students.iloc[1:7]

Using loc:

students.loc[:, ["name", "marks"]]

Set student_id as index:

students.set_index("student_id", inplace=True)

Reset index:

students.reset_index(inplace=True)

🟢 Level 3 — Filtering

Questions 21–30

This level focuses on extracting records based on conditions.

Topics Covered

Comparison operators

Boolean filtering

Multiple conditions

& operator

| operator

between()

Filtering numerical data

Filtering categorical data

Examples

Students scoring above 80:

students[students["marks"] > 80]

Students from Pune:

students[students["city"] == "Pune"]

Students from Pune with marks above 80:

students[
    (students["city"] == "Pune") &
    (students["marks"] > 80)
]

Marks between 70 and 90:

students[students["marks"].between(70, 90)]

Students who paid more than ₹50,000:

students[students["fees_paid"] > 50000]

🟡 Level 4 — Sorting

Questions 31–40

This level focuses on arranging DataFrame records based on different columns.

Topics Covered

Ascending sorting

Descending sorting

Top records

Bottom records

Sorting by multiple columns

Finding maximum values

Finding minimum values

Finding second-highest values

nlargest()

Examples

Sort marks in ascending order:

students.sort_values("marks")

Sort marks in descending order:

students.sort_values(
    "marks",
    ascending=False
)

Find top 5 students:

students.sort_values(
    "marks",
    ascending=False
).head()

Sort by course and marks:

students.sort_values(
    ["course", "marks"],
    ascending=[True, False]
)

Find the second-highest marks:

students["marks"].nlargest(2).iloc[-1]

🟡 Level 5 — Creating & Updating Columns

Questions 41–50

This level focuses on creating new columns, modifying existing data, applying conditions, and deleting/renaming columns.

Topics Covered

Creating new columns

.apply()

Lambda functions

np.where()

Boolean columns

Updating column values

Adding bonus marks

Calculating final marks

Deleting columns

Renaming columns

Creating Pass/Fail

students["result"] = students["marks"].apply(
    lambda x: "Pass" if x >= 40 else "Fail"
)

Creating Attendance Status

students["attendance_status"] = students["attendance"].apply(
    lambda x:
        "Excellent" if x > 90
        else "Good" if x == 75
        else "Poor"
)

Creating a Boolean column

students["Boolean"] = students["marks"] > 40

Increasing marks

students["marks"] = students["marks"] + 5

Adding bonus marks

students["Bonus_marks"] = 5

Calculating final marks

students["final_marks"] = (
    students["marks"] + students["Bonus_marks"]
)

Deleting a column

students.drop(
    columns=["Bonus_marks"],
    inplace=True
)

📊 Practice Progress

Level

Questions

Topic

Status

Level 1

1–10

Loading & Inspection

✅ Completed

Level 2

11–20

Selecting Data

✅ Completed

Level 3

21–30

Filtering

✅ Completed

Level 4

31–40

Sorting

✅ Completed

Level 5

41–50

Creating & Updating Columns

✅ Completed

Total Practice Questions: 50

📂 Notebooks

The practice is divided into five Jupyter Notebooks:

level1.ipynb
level2.ipynb
level3.ipynb
level4.ipynb
level5.ipynb

Each notebook represents one stage of the Pandas DataFrame practice.

📄 Dataset

The exercises use a student dataset containing columns such as:

student_id

name

gender

city

course

marks

attendance

fees_paid

The dataset is used throughout the different levels to practice real DataFrame operations.

🚀 How to Run

1. Clone the repository

git clone https://github.com/PrathmeshSurwase6250/Python_Pandas_DataFrame_Day1.git

2. Enter the project

cd Python_Pandas_DataFrame_Day1

3. Install Pandas

python3 -m pip install pandas

4. Install Jupyter Notebook

python3 -m pip install notebook

5. Start Jupyter Notebook

jupyter notebook

Open any of the following notebooks:

level1.ipynb
level2.ipynb
level3.ipynb
level4.ipynb
level5.ipynb

🎯 Learning Objectives

Through these exercises, I am developing practical knowledge of:

Pandas DataFrame

Reading CSV datasets

DataFrame inspection

Row and column selection

loc and iloc

Boolean filtering

Multiple conditions

Sorting DataFrames

Finding top/bottom records

Creating calculated columns

Lambda functions

Applying functions

NumPy conditional operations

Updating DataFrame values

Deleting columns

Index management

📈 Pandas Learning Path

This repository represents the beginning of my Pandas learning journey.

Python
   ↓
NumPy
   ↓
Pandas Series
   ↓
Pandas DataFrame
   ↓
Data Cleaning
   ↓
Data Analysis
   ↓
Matplotlib
   ↓
Seaborn
   ↓
SQL
   ↓
Machine Learning

🔗 Repository

GitHub:

https://github.com/PrathmeshSurwase6250/Python_Pandas_DataFrame_Day1

👨‍💻 Author

Prathmesh Surwase

Computer Engineering Student

Interests

Python

Pandas

NumPy

Data Analysis

Machine Learning

MERN Stack

Java & DSA

GitHub

https://github.com/PrathmeshSurwase6250

⭐ Learning by Practicing

This repository focuses on hands-on practice rather than only learning theory.

The objective is to solve progressively difficult Pandas problems and develop the ability to manipulate and analyze datasets using Python.

⭐ If you find this repository useful, consider giving it a star!
