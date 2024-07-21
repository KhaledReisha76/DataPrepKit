DataPrepKit
DataPrepKit is a comprehensive data preprocessing and exploratory data analysis (EDA) toolkit designed to streamline the initial phases of data analysis projects. This toolkit supports multiple file formats and provides essential functions for handling missing values, summarizing data, and encoding categorical data.

Features
Multi-format File Reading: Supports CSV, Excel, and JSON file formats for seamless data import.
Missing Value Handling: Various methods to handle missing values, including filling with zero, previous values, next values, or dropping rows based on conditions.
Summary Statistics: Generate key summary statistics for quick data insights.
Frequent Value Finder: Identify the most frequent value in a specified column.
Average Finder: Calculate the average of a specific numerical column.
Categorical Data Encoding: Encode categorical data using OneHotEncoder from scikit-learn.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/DataPrepKit.git
Install the necessary packages:

bash
Copy code
pip install -r requirements.txt
Usage
Reading Files
Use the read_file function to import data from different formats:

python
Copy code
import pandas as pd
import numpy as np
import os

# Read file
table = read_file()
print(table)
Handling Missing Values
Various methods to handle missing values:

python
Copy code
# Fill null values with zero
table1 = table.fillna(value=0)

# Fill null values with previous value
table1 = table.fillna(method='pad')

# Fill null values with next value
table1 = table.fillna(method='bfill')

# Drop rows with any null value
table1 = table.dropna(how='any')

# Drop rows where all elements are null
table1 = table.dropna(how='all')
Summary Statistics
Generate summary statistics of the dataset:

python
Copy code
# Summary statistics
stats = summary_statistics()
print(stats)
Finding Most Frequent Value
Find the most frequent value in a specified column:

python
Copy code
# Most frequent value in a specific column
most_freq = find_most_freq()
print(most_freq)
Finding Average
Find the average of a specific numerical column:

python
Copy code
# Average of a numerical column
avg = find_avg()
print(avg)
Encoding Categorical Data
Encode categorical data:

python
Copy code
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder

# Encoding categorical data
ohe = OneHotEncoder()
encoded_data = ohe.fit_transform(table1[['mfr']])
print(encoded_data)
print(ohe.categories_)
Contributing
Contributions are welcome! Please open an issue or submit a pull request.

License
This project is licensed under the MIT License.

https://pypi.org/project/AbdelrahmanReisha/0.1.1/
