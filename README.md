# PANDAS LIBRARY
* It sounds like you might be referring to Pandas in the context of programming, rather than HTML. Pandas is actually a Python library used for data manipulation and analysis. It's widely used for working with structured data, like tables, CSV files, and databases.

# Basic Operations:s

df = pd.read_csv("top universities.csv")
This reads the CSV file "top universities.csv" and stores it in the DataFrame df.

## 2Displaying Data:

* df.head() shows the first 5 rows of the DataFrame.
* df.tail() shows the last 5 rows of the DataFrame.
* df.sample() returns a random row(s) from the DataFrame.
* df.shape gives the dimensions of the DataFrame (rows, columns).
## 3 Renaming Columns:


df.rename(columns={"Global Rank": "Global"})
Renames the "Global Rank" column to "Global" in the DataFrame.

## 4 Display Options:


pd.set_option("display.max_rows", None)
Sets the option to display all rows in the DataFrame without truncation (use carefully for large datasets).

# Data Summary:
## 5 Basic Information:

* df.info() gives a concise summary of the DataFrame, including the number of non-null entries and data types.
* df.describe() provides summary statistics for numeric columns.
* df.describe(include="all") provides summary statistics for both numeric and categorical columns.
## 6 Accessing Specific Columns:

p
a = df["University"]
b = df[["University", "Global Rank"]]
a holds the "University" column as a Series.
b holds a new DataFrame with the "University" and "Global Rank" columns.
# Data Calculations:
## 7 Statistical Calculations:

df["Global Rank"].mean() calculates the mean of the "Global Rank" column.
df["Global Rank"].median() gives the median.
df["Global Rank"].mode() provides the mode(s).
df["Global Rank"].std() calculates the standard deviation.
## 8 Value Counts:

df["University"].value_counts()
df["Country"].value_counts()
Counts the frequency of each unique value in the "University" or "Country" column.
# Visualizations:
## 9 Plotting:
* df["Country"].value_counts().plot(kind="bar") creates a bar chart for the distribution of countries.
* df["Global Rank"].plot(kind="line") creates a line plot of the "Global Rank".
* df["Country"].value_counts().plot(kind="hist") creates a histogram of country counts.
* df["Country"].value_counts().plot(kind="pie") creates a pie chart for the distribution of countries.
# Handling Missing Data:
## 10 Null Data Handling:
* df.isnull() checks for missing values in the DataFrame.
* df.isnull().sum() gives the number of missing values per column.
* df[df["University"].isnull()] filters rows where the "University" column is missing.
* df["Global Rank"].fillna(df["Global Rank"].mean()) fills missing values in "Global Rank" with its mean.
* df.dropna() removes rows with any missing values.
# Data Grouping and Filtering:
## 11 Grouping:

df.groupby("University").describe()
Groups the DataFrame by the "University" column and calculates descriptive statistics for each group.

## 12 Selecting Specific Rows:
* df.loc[[2,5,8,12]] selects rows by index labels.
* df.iloc[[2,4]] selects rows by integer-based position.
* df[2:5] slices rows from index 2 to 4.
* df[1:7:2] slices rows from index 1 to 6, with a step of 2.
# Handling Duplicates:
## 13 Duplicate Detection:

print(df.duplicated())
Checks for duplicated rows in the DataFrame.

# 14 Filling Missing Values:

df.fillna(55)
Fills all missing values in the DataFrame with 55.

Kind='bar'
In the context of plot(kind='bar'), the kind='bar' is specifying that you want to create a bar plot (or bar chart).
