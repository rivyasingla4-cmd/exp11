Experiment 11: Creating, Loading, and Exploring Datasets in Pandas

# AIM:

To create datasets and load datasets in pandas library.

# Theory & Command Reference:

# 1. Dataset Creation & Exporting:

Pandas allows you to construct DataFrames from scratch using native Python data structures (like dictionaries) and save them to your local file system. * pd.DataFrame(data): Converts a dictionary (where keys are column names and values are lists of data) into a tabular Pandas DataFrame. * df.to_csv("filename.csv", index=False): Exports the DataFrame to a Comma-Separated Values (CSV) file. The index=False argument prevents Pandas from writing the row indices (0, 1, 2...) as a separate column in the file.

# 2. Loading External Datasets:

The most common way to analyze data in Pandas is by importing existing files. * pd.read_csv('filepath/filename.csv'): Reads a CSV file from the specified path and loads it into a Pandas DataFrame for analysis.

# 3. Detailed DataFrame Information:

Beyond basic inspection (.head(), .tail(), .shape, .size), Pandas provides powerful summary commands to instantly understand a dataset's profile.

df.info(): Prints a concise summary of the DataFrame. This includes the total number of rows and columns, the column names, the count of non-null values in each column, the data type of each column (e.g., int64, float64, object), and the memory usage.
df.describe(): Generates a statistical summary of all numerical columns in the dataset. It automatically calculates the count, mean, standard deviation (std), min, max, and quartiles (25%, 50%, 75%) for quick statistical insights.
# 4. Data Quality & Exploration Checks:

When working with real-world data (like the Cars93.csv dataset), it is crucial to check for missing values, duplicates, and general data cardinality.

df.sample(n): Returns a random sample of n rows from the DataFrame. This is useful for seeing a random cross-section of the data rather than just the top or bottom rows.
df.isnull().sum(): Chains two commands to check for missing data. isnull() creates a boolean mask of missing values, and .sum() adds them up column-wise. It returns the exact count of missing (NaN) values for each column.
df.duplicated().sum(): Checks the entire DataFrame for exact duplicate rows and returns the total count of duplicated entries.
df.nunique(): Returns the total number of unique elements (distinct values) present in each column. This is highly useful for identifying categorical variables.

# Conclusion:

In this experiment, we expanded our knowledge of the Pandas library by focusing on dataset input/output (I/O) and initial data profiling. We successfully learned how to create a dataset from a Python dictionary and export it to a CSV file. Furthermore, we imported a real-world external dataset (Cars93.csv) and utilized essential EDA commands to assess its shape, extract statistical summaries, and identify data quality issues such as missing values and duplicate records. These steps form the standard preliminary workflow for any Data Science or Machine Learning project.
