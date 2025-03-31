# Data Transformation with Pandas

Data transformation is about reshaping, combining, and summarizing your data to uncover patterns, answer specific questions, and prepare it for analysis or machine learning.

**Why Transform Data?**

*   **Combine Information:** Bring together data from different sources (e.g., user demographics + purchase history).
*   **Highlight Trends:** Order data to easily spot top performers, outliers, or changes over time.
*   **Summarize Effectively:** Calculate key metrics for different groups within your data (e.g., average sales per region).
*   **Focus Analysis:** Isolate specific subsets of data relevant to your question.
*   **Create New Features:** Derive new information from existing columns (e.g., calculate profit from sales and cost).
*   **Prepare for Modeling:** Structure data in the format required by machine learning algorithms.

**Setting the Stage: Importing Pandas and Loading Data**

Before we transform, we need our tools and materials.

1.  **Import Pandas:** This line makes the Pandas library available in our Python environment, typically using the alias `pd`.
    ```python
    import pandas as pd
    print(f"Pandas version: {pd.__version__}")
    ```
2.  **Load Data:** We often start with data from files like CSVs. `pd.read_csv()` loads this data into a **DataFrame**, the core data structure in Pandas (think of it as a smart, programmable spreadsheet).
    ```python
    # Assuming you have a CSV file named 'sales_data.csv'
    try:
        df = pd.read_csv('sales_data.csv')
        print("Data loaded successfully.")
    except FileNotFoundError:
        print("Error: 'sales_data.csv' not found. Using sample data instead.")
        # Create sample data if file not found
        data = {'Region': ['North', 'South', 'East', 'West', 'North', 'South', 'East', 'West'],
                'Product': ['A', 'B', 'A', 'B', 'C', 'A', 'B', 'C'],
                'Sales': [1200, 800, 1500, 950, 500, 1100, 750, 1300],
                'Users': [150, 110, 180, 120, 80, 140, 90, 160]}
        df = pd.DataFrame(data)
    ```
3.  **Initial Inspection:** Get a feel for your data using `.head()`.
    ```python
    print("First 5 rows of the DataFrame:")
    print(df.head())

    print("\nDataFrame Info:")
    df.info() # Shows column types and non-null counts
    ```

---

## Core Data Transformation Techniques

Let's explore the key transformations mentioned:

**1. Combining DataFrames: `merge` and `concat`**

Often, your data is split across multiple tables or files.

*   **`pd.merge()` (Joining like Puzzle Pieces)**
    *   **Concept:** Combines DataFrames based on common columns (keys) or indices. Similar to SQL JOINs.
    *   **Purpose:** To enrich a dataset by adding related information from another dataset.
    *   **Example:** Combine user demographics with product preferences using a common `UserID`.
    *   **Syntax:**
        ```python
        # Assume df_demographics has 'UserID', 'Age', 'Location'
        # Assume df_preferences has 'UserID', 'Product', 'Rating'
        # merged_df = pd.merge(df_demographics, df_preferences, on='UserID', how='inner')
        # 'how' can be 'inner', 'outer', 'left', 'right'
        print("\n--- Merging (Example Structure) ---")
        print("merged_df = pd.merge(df1, df2, on='common_column', how='inner')")
        ```
*   **`pd.concat()` (Stacking or Placing Side-by-Side)**
    *   **Concept:** Stacks DataFrames vertically (row-wise, `axis=0`) or horizontally (column-wise, `axis=1`).
    *   **Purpose:** Combine datasets with the *same* structure (e.g., sales data from different months) or add new columns from another DataFrame that shares the same index.
    *   **Example:** Combine monthly sales reports into a single yearly report.
    *   **Syntax:**
        ```python
        # Assume df_jan_sales and df_feb_sales have the same columns
        # yearly_sales = pd.concat([df_jan_sales, df_feb_sales], axis=0, ignore_index=True)
        # 'ignore_index=True' resets the index for the combined DataFrame
        print("\n--- Concatenating (Example Structure) ---")
        print("combined_df = pd.concat([df1, df2], axis=0)") # Stacking rows
        ```

**2. Sorting Data: `df.sort_values()`**

*   **Concept:** Arranges rows based on the values in one or more columns.
*   **Purpose:** Easily identify extremes (highest/lowest values), order data chronologically, or prepare for certain types of analysis.
*   **Example:** Find the products with the highest sales.
*   **Syntax:**
    ```python
    print("\n--- Sorting ---")
    df_sorted_by_sales = df.sort_values(by='Sales', ascending=False) # Sort by Sales, highest first
    print("DataFrame sorted by Sales (Descending):")
    print(df_sorted_by_sales.head())
    ```

**3. Grouping and Aggregating: `df.groupby()` and `df.agg()`**

This is a powerful pattern: Split -> Apply -> Combine.

*   **`df.groupby()` (Splitting into Groups)**
    *   **Concept:** Splits the DataFrame into groups based on the values in one or more specified columns (the grouping key(s)).
    *   **Purpose:** To perform calculations *within* specific categories or segments of your data.
    *   **Example:** Group sales data by 'Region' to analyze performance per region.
*   **Aggregation (Applying Calculations)**
    *   **Concept:** Applying a function (like `sum`, `mean`, `count`, `min`, `max`) to each group created by `groupby()`.
    *   **Purpose:** To summarize the characteristics of each group.
    *   **Example:** Calculate the *total* sales (`sum()`) or *average* sales (`mean()`) for each region.
    *   **Syntax (Common Chaining):**
        ```python
        print("\n--- Grouping and Aggregating ---")
        # Group by 'Region' and calculate the sum of 'Sales' for each region
        regional_sales_sum = df.groupby('Region')['Sales'].sum()
        print("Total Sales per Region:")
        print(regional_sales_sum)

        # Group by 'Region' and calculate multiple aggregations
        regional_stats = df.groupby('Region').agg(
            Total_Sales=('Sales', 'sum'),
            Average_Sales=('Sales', 'mean'),
            Number_of_Entries=('Region', 'size') # 'size' counts rows per group
        )
        print("\nMultiple Aggregations per Region:")
        print(regional_stats)
        ```
*   **`df.agg()` (DataFrame-level Aggregation)**
    *   **Concept:** Apply aggregation functions across the entire DataFrame (or specific columns) without grouping first.
    *   **Purpose:** Get overall summary statistics.
    *   **Example:** Calculate the average sales across *all* transactions.
    *   **Syntax:**
        ```python
        print("\n--- DataFrame-level Aggregation ---")
        average_overall_sales = df['Sales'].mean() # Specific column
        # Or using agg()
        overall_avg_sales = df.agg(Average_Sales=('Sales', 'mean'))
        print(f"Overall Average Sales: {average_overall_sales:.2f}")
        print(overall_avg_sales)
        ```

**4. Filtering Data (Boolean Indexing)**

*   **Concept:** Selecting rows based on conditions.
*   **Purpose:** To isolate specific subsets of data for focused analysis.
*   **Example:** Analyze only the high-value sales transactions.
*   **Syntax:**
    ```python
    print("\n--- Filtering ---")
    high_sales = df[df['Sales'] > 1000]
    print("Rows with Sales > 1000:")
    print(high_sales)

    north_region_sales = df[df['Region'] == 'North']
    print("\nRows for 'North' Region:")
    print(north_region_sales)
    ```

**5. Applying Custom Functions: `df.apply()`**

*   **Concept:** Apply a function (either predefined or custom `lambda` function) row-wise or column-wise.
*   **Purpose:** Perform complex or custom transformations not covered by built-in functions. Create new features based on existing data.
*   **Example:** Calculate a 'Sales_with_Discount' column.
*   **Syntax:**
    ```python
    print("\n--- Applying Custom Functions ---")
    # Define a function to apply a 10% discount
    def calculate_discount(sale_price):
        return sale_price * 0.90

    # Apply the function to the 'Sales' column to create a new column
    df['Discounted_Sales'] = df['Sales'].apply(calculate_discount)
    # Alternatively, using a lambda function for simple operations:
    # df['Discounted_Sales'] = df['Sales'].apply(lambda x: x * 0.90)
    print("DataFrame with 'Discounted_Sales' column:")
    print(df.head())
    ```

**6. Reshaping Data: `df.pivot_table()`**

*   **Concept:** Reshapes data from a "long" format to a "wide" format, summarizing values. Similar to pivot tables in spreadsheet software.
*   **Purpose:** Create summary tables for easier comparison across different categories.
*   **Example:** Create a table showing total sales for each Product within each Region.
*   **Syntax:**
    ```python
    print("\n--- Pivoting ---")
    # Create a pivot table: Regions as rows, Products as columns, Sales as values
    # aggfunc defaults to mean, let's use sum
    pivot_df = pd.pivot_table(df, values='Sales', index='Region', columns='Product', aggfunc='sum', fill_value=0)
    print("Pivot Table (Sales by Region and Product):")
    print(pivot_df)
    ```

**7. Handling Missing Data: `df.fillna()` and `df.dropna()`**

Real-world data often has gaps (`NaN` - Not a Number).

*   **`df.fillna()` (Imputation)**
    *   **Concept:** Replace missing values with a specified value (e.g., 0, mean, median, mode).
    *   **Purpose:** Keep all rows/columns while ensuring calculations don't fail due to `NaN`s. Choose the fill value carefully based on context.
    *   **Syntax:**
        ```python
        # Example: Fill missing sales with 0 (use cautiously!)
        # df_filled = df.fillna({'Sales': 0})
        # print(df_filled)
        print("\n--- Handling Missing Data (Fill) ---")
        print("df_filled = df.fillna(0) # Fills all NaN with 0")
        # Check for missing values before potentially filling
        print("\nMissing values before fillna (example):")
        # Introduce a NaN for demonstration if none exist
        if df['Sales'].isnull().sum() == 0:
             df.loc[0, 'Sales'] = pd.NA # Introduce a missing value
        print(df.isnull().sum())
        df_filled_mean = df.fillna(df['Sales'].mean()) # Fill with mean
        print("\nMissing values after filling with mean:")
        print(df_filled_mean.isnull().sum())
        print(df_filled_mean.head())
        # Restore original value if we changed it for demo
        if pd.isna(df.loc[0, 'Sales']):
            df.loc[0, 'Sales'] = 1200
        ```
*   **`df.dropna()` (Deletion)**
    *   **Concept:** Remove rows or columns containing missing values.
    *   **Purpose:** Ensure data integrity by removing incomplete records. Can lead to information loss if many rows are dropped.
    *   **Syntax:**
        ```python
        # Example: Drop rows with any missing values
        # df_dropped_rows = df.dropna(axis=0)
        # Example: Drop columns with any missing values
        # df_dropped_cols = df.dropna(axis=1)
        print("\n--- Handling Missing Data (Drop) ---")
        print("df_dropped = df.dropna() # Drops rows with any NaN")
        ```

---

## Best Practices for Data Transformation

1.  **Start with a Clear Goal:** Know *what* question you're trying to answer or *what* structure you need before you start transforming.
2.  **Document Your Steps:** Use comments in your code (`#`) or markdown cells in notebooks to explain *why* you are performing each transformation. This aids reproducibility and understanding later.
3.  **Validate Your Results:** After each significant transformation (especially merges, pivots, complex aggregations), check the output. Does the shape (`df.shape`) make sense? Are the values reasonable (`df.head()`, `df.describe()`)? Did the merge work as expected?
4.  **Experiment and Iterate:** Data analysis is often iterative. Don't be afraid to try different grouping strategies, aggregations, or ways of handling missing data. See what yields the most insight.
5.  **Work on Copies (Often):** Especially when starting, you might want to assign the result of a transformation to a *new* DataFrame (`df_sorted = df.sort_values(...)`) rather than modifying the original `df` in place, unless you're sure. Many Pandas methods have an `inplace=True` option, but use it cautiously.

---

## Related Notes