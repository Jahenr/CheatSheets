*Pull Request Description* 

Title: Introduction of Basic Pandas Operations

Description:This pull request introduces a variety of basic operations using the Pandas library to demonstrate DataFrame and Series functionalities. The additions include creating DataFrames and Series, viewing data, selecting and filtering data, basic data manipulations (such as adding and removing columns), data aggregation, file input/output operations, and basic text and data type manipulations. This will serve as a foundational script for our future assignments and projects where data manipulation and analysis are required.

Course: DIGT1161

Group Members and Contributions:
Mahjabin: Focused on file input/output functions and data filtering methods.
Alicia: Worked on data creation, viewing, and basic DataFrame operations.
Sienna: Handled text manipulation functions and data type conversions.
Steeve: Implemented statistical methods and basic plotting features.

This collective effort has ensured a comprehensive introduction to handling data using Pandas, tailored to assist our class peers in getting up to speed with Python data manipulation.

Pull Request
# Import the pandas library
import pandas as pd

# Create an empty DataFrame
pd.DataFrame()

# Create a DataFrame from a dictionary of lists
# Each key becomes a column name, and the list elements are the column values
pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

# Create a Series from a list
pd.Series([1, 2, 3, 4, 5])

# View the first few rows of a DataFrame
# Helps to quickly inspect the beginning of large DataFrames
df.head()

# View the last few rows of a DataFrame
# Useful for checking the end portions of large DataFrames
df.tail()

# Select a single column, returns a Series
df['column_name']

# Select multiple columns, returns a DataFrame
df[['column1', 'column2']]

# Select rows by position (integer-location based)
df.iloc[0]  # First row
df.iloc[0:5]  # First five rows

# Select a specific value by row and column position
df.iloc[0, 0]  # Value in first row and first column

# Filter rows based on column values
df[df['column'] > 10]

# Get basic statistics for numerical columns
df.describe()

# Get the data types of columns
df.dtypes

# Check for missing values
df.isnull()

# Drop rows with any missing values
df.dropna()

# Fill missing values with a specified value
df.fillna(value)

# Create a new column
df['new_column'] = [value1, value2, value3]

# Drop a column
df.drop('column_name', axis=1, inplace=True)

# Rename columns
df.rename(columns={'old_name': 'new_name'}, inplace=True)

# Sum of a column's values
df['column'].sum()

# Average (mean) of a column's values
df['column'].mean()

# Converts all characters in the column to uppercase
df[‘text_coloumn’].str.upper()

# Converts all characters in the column to lowercase
df[‘text_column’].str.lower()

# Removes leading and trailing whitespace from each entry in the column
df[‘text_column’].str.strip()

# Aligns text to the left
df[‘text_column’].str.ljust(width)

# Aligns text to the right
df[‘text_column’].str.rjust(width)

# Aligns text to the center
df[‘text_column’].str.center(width)

# Read data from a CSV file into a DataFrame
pd.read_csv('filename.csv') #Other types: read_json, read_html, read_xml, read_excel

# Write data from a DataFrame to a CSV file
df.to_csv('filename.csv', index=False) #Other types: to_json, to_html, to_xml, to_excel

# Sort DataFrame by a column
df.sort_values(by='column_name')

# Get unique values from a column
df['column_name'].unique()

# Get the number of unique values in a column
df['column_name'].nunique()

# Get the count of occurrences of each unique value in a column
df['column_name'].value_counts()

# Set a column as the index of the DataFrame
df.set_index('column_name', inplace=True)

# Reset the index, turning it back into a column
df.reset_index(inplace=True)

# Convert a column's data type
df['column_name'] = df['column_name'].astype('new_type') #e.g. “float32”

# Basic plotting (requires matplotlib)
df['column_name'].plot()

# Save a plot to a file (requires matplotlib)
df['column_name'].plot().figure.savefig('plot.png')
