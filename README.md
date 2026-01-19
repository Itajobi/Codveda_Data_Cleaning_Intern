##  Data Cleaning And Preprocessing

This repository documents my work for Level 1 Task 1 of my internship program.
The task focuses on basic data cleaning and preprocessing to ensure the dataset is ready for analysis.

## Task Objectives
Work with a raw dataset (e.g., CSV file) that
contains missing values, duplicates, and inconsistent
data formats.
- Load the dataset using pandas.
- Identify and handle missing values (via imputation or removal).
- Remove duplicate rows.
- Standardize inconsistent data formats (e.g., date formats, categorical variables).

## Tools & Libraries
- Python (Jupyter Notebook)
- pandas → data loading, cleaning, and manipulation

## Steps Implemented
- Data Loading
import pandas as pd
df = pd.read_csv('C:/Users/xpert/Downloads/iris.csv')
# Handle Missing Values
- Checked with df.isnull().sum()
- Checked duplicate rows and print with -df.duplicated().sum(), df[df.duplicated()]
## Drop duplicate rows and reset the index
df = df.drop_duplicates() 
df = df.reset_index(drop=True)
# Handling inconsistencies
df['species'] = df['species'].str.lower().str.strip()
# Verify unique values after normalization
df['species'].unique()

## Insights
- Dataset contained both numerical and categorical features.
- Duplicate records were removed to improve data quality.
- Standardization ensured consistency across formats, reducing errors in later analysis.
