Pandas:

```bash
        # Import the pandas library
                import pandas as pd

        # Create an empty DataFrame
                pd.DataFrame()

        # Create a DataFrame from a dictionary of lists
                pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

        # Create a Series from a list
                pd.Series([1, 2, 3, 4, 5])
```

Data Viewing:

```bash
        # View the first few rows of a DataFrame
                df.head()

        # View the last few rows of a DataFrame
                df.tail()

        # Get the data types of columns
                df.dtypes

        # Get basic statistics for numerical columns
                df.describe()
```

Selecting Data:

```bash
        # Select a single column (returns a Series)
                df['column_name']

        # Select multiple columns (returns a DataFrame)
                df[['column1', 'column2']]

        # Select rows by position (integer-location based) — first row
                df.iloc[0]

        # Select the first five rows
                df.iloc[0:5]

        # Select a specific value by row and column position (first row, first column)
                df.iloc[0, 0]

        # Filter rows based on a condition
                df[df['column_name'] > 10]
```

Missing Values:

```bash
        # Check for missing values
                df.isnull()

        # Drop rows with any missing values
                df.dropna()

        # Fill missing values with a specified value
                df.fillna(value)
```

Columns & Indexing:

```bash
        # Create a new column
                df['new_column'] = [value1, value2, value3]

        # Drop a column
                df.drop('column_name', axis=1, inplace=True)

        # Rename columns
                df.rename(columns={'old_name': 'new_name'}, inplace=True)

        # Set a column as the index of the DataFrame
                df.set_index('column_name', inplace=True)

        # Reset the index, turning it back into a column
                df.reset_index(inplace=True)

        # Convert a column's data type (e.g., to float32)
                df['column_name'] = df['column_name'].astype('float32')
```

Statistics & Aggregations:

```bash
        # Sum of a column's values
                df['column_name'].sum()

        # Average (mean) of a column's values
                df['column_name'].mean()

        # Get unique values from a column
                df['column_name'].unique()

        # Get the number of unique values in a column
                df['column_name'].nunique()

        # Get the count of occurrences of each unique value in a column
                df['column_name'].value_counts()
```

GroupBy:

```bash
        # Group by a single column and calculate mean
                df.groupby('column_name').mean()

        # Group by multiple columns
                df.groupby(['col1', 'col2']).sum()

        # Apply multiple aggregations
                df.groupby('column_name').agg({'other_column': ['mean', 'max']})
```

Merge & Join:

```bash
        # Merge two DataFrames on a common column (inner join by default)
                pd.merge(df1, df2, on='key')

        # Left join
                pd.merge(df1, df2, on='key', how='left')

        # Join on index
                df1.join(df2, how='outer')
```

Concatenate:

```bash
        # Concatenate DataFrames vertically (stack rows)
                pd.concat([df1, df2])

        # Concatenate DataFrames horizontally (add columns)
                pd.concat([df1, df2], axis=1)
```

Reshape:

```bash
        # Pivot table (summarize data)
                df.pivot_table(values='sales', index='region', columns='year', aggfunc='sum')

        # Unstack: move row index to columns
                df.unstack()

        # Stack: move columns to row index
                df.stack()
```

Date & Time:

```bash
        # Convert a column to datetime
                df['date'] = pd.to_datetime(df['date'])

        # Extract year, month, day
                df['year'] = df['date'].dt.year
                df['month'] = df['date'].dt.month
                df['day'] = df['date'].dt.day

        # Filter by date range
                df[(df['date'] >= '2023-01-01') & (df['date'] <= '2023-12-31')]
```

Sampling:

```bash
        # Random sample of n rows
                df.sample(n=5)

        # Random sample of a fraction of rows
                df.sample(frac=0.1, random_state=1)
```

Apply & Lambda:

```bash
        # Apply a function to each element of a column
                df['col'] = df['col'].apply(lambda x: x*2)

        # Apply a function row-wise
                df.apply(lambda row: row['col1'] + row['col2'], axis=1)
```

String Operations:

```bash
        # Convert all characters in the column to uppercase
                df['text_column'].str.upper()

        # Convert all characters in the column to lowercase
                df['text_column'].str.lower()

        # Remove leading and trailing whitespace from each entry in the column
                df['text_column'].str.strip()

        # Align text to the left with a given width
                df['text_column'].str.ljust(width)

        # Align text to the right with a given width
                df['text_column'].str.rjust(width)

        # Align text to the center with a given width
                df['text_column'].str.center(width)
```

Sorting:

```bash
        # Sort DataFrame by a column
                df.sort_values(by='column_name')
```

Input / Output:

```bash
        # Read data from a CSV file into a DataFrame
                pd.read_csv('filename.csv')
                        # Other readers include: read_json, read_html, read_xml, read_excel

        # Write data from a DataFrame to a CSV file
                df.to_csv('filename.csv', index=False)
                        # Other writers include: to_json, to_html, to_xml, to_excel
```

Plotting (requires matplotlib):

```bash
        # Basic plotting of a single column
                df['column_name'].plot()

        # Save a plot to a file
                df['column_name'].plot().figure.savefig('plot.png')
```
