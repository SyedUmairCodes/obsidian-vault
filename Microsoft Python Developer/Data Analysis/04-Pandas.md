# Pandas for Data Analysis

Pandas is a Swiss army knife designed for handling data in Python. It's a library that allows you to load, clean, transform, analyze, and even visualize data.  Pandas is designed to be intuitive and user-friendly.

```python
import pandas as pd
```
  
**Use-cases**
*  Clean messy and inconsistent data.
*   Explore datasets to understand their structure and content.
*   Filter and select specific pieces of information.
*   Calculate summary statistics.
*   Spot trends and patterns.
*   Prepare data for visualization or machine learning.

## DataFrames
The core structure in Pandas is the **DataFrame**. Imagine a spreadsheet or a database table. It's a 2D, table-like data structure.

| Rows    | Represent individual observations or data points                                                               |
| ------- | -------------------------------------------------------------------------------------------------------------- |
| Columns | Represent different variables, features, or attributes of the data                                             |
| Index   | A special set of labels that uniquely identifies each row. It acts like an address for quickly accessing rows. |
>A DataFrame is essentially a container holding your data, an index for the rows, and names for the columns. 

## Common Methods

| `read_csv`           | Pandas can read data from various sources (CSV, Excel, SQL databases, etc.).                                          |
| -------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `df.head`            | View the first 5 rows of the dataframe.                                                                               |
| `df.info`            | Get a concise summary: column names, the number of non-null entries in each column, and the data type of each column. |
| `df.describe`        | Calculate summary statistics for numerical columns                                                                    |
| `df.shape`           | See the dimensions of the DataFrame (number of rows, number of columns).                                              |
| `.loc[]`             | Selects data using the *row index labels* and *column names*.                                                         |
| `.iloc[]`            | Selects data using *integer positions* (starting from 0), like list indexing. Ignores index labels and column names.  |
| `.at[]` and `.iat[]` | Optimized versions of `.loc` and `.iloc` specifically for accessing a *single value* very quickly.                    |

## Related Notes