# <p align="center"> **Short Questions and Answers** </p>

### 1) **What is SQLite? What are the advantages and features of SQLite?**
   - SQLite is a lightweight, self-contained, serverless database engine. Advantages: zero configuration, portable, reliable, and supports ACID transactions.

### 2) **What datatype does SQLite support?**
   - Supports dynamic typing with types like `NULL`, `INTEGER`, `REAL`, `TEXT`, and `BLOB`.

### 3) **What is the use of the LIMIT clause with SELECT query?**
   - Restricts the number of rows returned in a query result.

### 4) **Why is the ORDER BY clause used with the SELECT statement?**
   - Sorts the result set based on specified columns, either ascending (`ASC`) or descending (`DESC`).

### 5) **What is the use of the SQLite GROUP BY clause?**
   - Groups rows with the same values in specified columns and performs aggregate operations on each group.

### 6) **What is the use of the DISTINCT clause in SQLite?**
   - Removes duplicate rows from a result set.

### 7) **Explain commit and rollback.**
   - `COMMIT`: Saves all changes made during a transaction.
   - `ROLLBACK`: Reverts all changes made during a transaction.

### 8) **Define .dump command.**
   - Exports the entire SQLite database into a text file, including SQL statements.

### 9) **What is a CSV file?**
   - A comma-separated values file storing tabular data in plain text.

### 10) **Define Module.**
   - A file containing Python code, including functions, classes, and variables.

### 11) **Explain PYTHONPATH.**
   - An environment variable specifying directories where Python looks for modules and packages.

### 12) **Define Packages.**
   - A collection of Python modules, often organized in directories containing `__init__.py` files.

### 13) **Difference between fetchone() and fetchall() methods.**
   - `fetchone()`: Retrieves the next row from the result set.
   - `fetchall()`: Retrieves all remaining rows.

### 14) **Explain commit() method.**
   - Saves changes made to the database during a transaction.

### 15) **Explain close() method.**
   - Closes the database connection to free resources.

### 16) **List File modes.**
   - Modes: `r` (read), `w` (write), `a` (append), `rb`, `wb`, `r+`, etc.

### 17) **Define CSV module.**
   - A Python module for reading and writing CSV files.

### 18) **Define Python Pandas.**
   - A Python library for data manipulation and analysis, using DataFrames and Series.

### 19) **How can we calculate the standard deviation from the Series?**
   - Use `Series.std()` method.

### 20) **Explain Data Visualization.**
   - The graphical representation of data to identify trends, patterns, and insights.

### 21) **Which is a Python package used for 2D graphics?**
   - `Matplotlib`.

### 22) **Define Matplotlib Python Libraries.**
   - A library for creating static, animated, and interactive visualizations in Python.

### 23) **Define set_title() method.**
   - Sets the title of a plot in Matplotlib.

### 24) **Explain xlabel and ylabel.**
   - `xlabel`: Sets the label for the x-axis.
   - `ylabel`: Sets the label for the y-axis.

### 25) **What is type affinity in SQLite?**
   - A flexible typing system where columns have a preferred storage class.

### 26) **What is the purpose of transaction rollback?**
   - Reverts the database to its previous state if an error occurs during a transaction.

### 27) **What is the difference between INTERSECT and EXCEPT filters?**
   - `INTERSECT`: Returns rows common to both queries.
   - `EXCEPT`: Returns rows in the first query but not in the second.

### 28) **Explain the syntax of Conditional Logic statements (CASE statements).**
   - `CASE WHEN condition THEN result ELSE result END`: Executes conditional logic.

### 29) **What is the difference between self join and full outer join?**
   - `Self Join`: Joins a table to itself.
   - `Full Outer Join`: Combines rows from both tables, including unmatched rows.

### 30) **What is a trigger?**
   - A database object that automatically executes a set of actions when certain events occur.

### 31) **How can a trigger be created and dropped? Give an example.**
   - **Create:** `CREATE TRIGGER trigger_name AFTER INSERT ON table_name BEGIN...END;`
   - **Drop:** `DROP TRIGGER trigger_name;`

# <p align="center"> **Long Questions and Answers** </p>

### 1. **Advantages of Using SQLite**
   - **Lightweight:** SQLite is small and requires minimal system resources, making it ideal for mobile apps or embedded systems.
   - **Self-contained:** It operates independently of external dependencies or servers.
   - **Portable:** Compatible across various operating systems (Windows, macOS, Linux).
   - **Zero-configuration:** No need for installation, setup, or server management.
   - **Transactional:** Supports ACID (Atomicity, Consistency, Isolation, Durability) transactions, ensuring data reliability.
   - **Cost-effective:** Open-source and free to use.
   - **Single-file database:** The entire database is stored in a single file, simplifying backup and transfer processes.

---

### 2. **SQLite Commands**
   SQLite supports standard SQL commands divided into categories:
   - **Data Definition Language (DDL):**
     - `CREATE TABLE`: Defines a new table.
     - `ALTER TABLE`: Modifies an existing table structure.
     - `DROP TABLE`: Deletes a table.
   - **Data Manipulation Language (DML):**
     - `INSERT`: Adds new records.
     - `SELECT`: Retrieves data from tables.
     - `UPDATE`: Modifies existing records.
     - `DELETE`: Removes records.
   - **Data Control Language (DCL):**
     - `GRANT` and `REVOKE`: Not fully supported in SQLite but exist in other SQL databases.
   - **Transaction Control:**
     - `BEGIN TRANSACTION`: Starts a transaction.
     - `COMMIT`: Saves changes.
     - `ROLLBACK`: Reverts changes.

---

### 3. **Difference Between SQL and SQLite**
   - **SQL (Structured Query Language):**
     - A standard language for managing relational databases.
     - Used with various database systems like MySQL, PostgreSQL, and Oracle.
   - **SQLite:**
     - A specific database engine that uses SQL syntax.
     - Embedded, serverless, and requires no configuration.
     - Ideal for applications with local databases.

---

### 4. **Types of Joins in SQLite**
   Joins combine rows from multiple tables based on related columns:
   - **INNER JOIN:**
     - Returns rows with matching values in both tables.
     ```sql
     SELECT * FROM table1 INNER JOIN table2 ON table1.id = table2.id;
     ```
   - **LEFT JOIN (LEFT OUTER JOIN):**
     - Returns all rows from the left table and matched rows from the right.
     ```sql
     SELECT * FROM table1 LEFT JOIN table2 ON table1.id = table2.id;
     ```
   - **CROSS JOIN:**
     - Produces a Cartesian product, combining all rows from both tables.
     ```sql
     SELECT * FROM table1 CROSS JOIN table2;
     ```

---

### 5. **UNION Operator**
   - **Definition:** Combines the results of two or more `SELECT` statements into a single result set.
   - **Behavior:** Removes duplicates unless `UNION ALL` is used.
   ```sql
   SELECT column FROM table1
   UNION
   SELECT column FROM table2;
   ```

---

### 6. **Triggers in SQLite**
   - **Trigger:** A SQL statement that executes automatically in response to specific database events.
   - **Types:**
     - **BEFORE Trigger:** Executes before the associated action.
     - **AFTER Trigger:** Executes after the action.
     - **INSTEAD OF Trigger:** Replaces the action with custom logic (used for views).
   ```sql
   CREATE TRIGGER log_update
   AFTER UPDATE ON students
   BEGIN
     INSERT INTO audit_log (action, timestamp) VALUES ('UPDATE', CURRENT_TIMESTAMP);
   END;
   ```

---

### 7. **Dump Entire Database into a File**
   - **Purpose:** Create a backup or transfer data.
   ```bash
   sqlite3 database.db .dump > backup.sql
   ```
   - This command exports all tables and data into an SQL file.

---

### 8. **Dump Specific Table and Table Structure**
   - **Dump Table Data:**
     ```bash
     sqlite3 database.db "SELECT * FROM table_name;" > table_data.sql
     ```
   - **Dump Table Structure:**
     ```bash
     sqlite3 database.db ".schema table_name" > table_schema.sql
     ```

---

### 9. **Dump Entire Database and Specific Table Data**
   - **Entire Database:**
     ```bash
     sqlite3 database.db .dump > entire_backup.sql
     ```
   - **Specific Table Data:**
     ```bash
     sqlite3 database.db "SELECT * FROM table_name;" > table_data.sql
     ```

---

### 10. **Import CSV into a Table**
   - **Steps:**
     ```sql
     .mode csv
     .import data.csv table_name
     ```
   - Ensure the CSV file structure matches the table schema.

---

### 11. **Export CSV from a Table**
   - **Steps:**
     ```sql
     .mode csv
     .output output.csv
     SELECT * FROM table_name;
     ```
   - Exports table data to a CSV file named `output.csv`.

---

### 12. **Setting PYTHONPATH, Namespace, Scope, and Packages in Python**
   - **PYTHONPATH:** 
     - An environment variable specifying directories where Python looks for modules and packages.
     - **Example:** 
       ```bash
       export PYTHONPATH="/path/to/your/module:$PYTHONPATH"
       ```
   - **Namespace:** 
     - A container holding a collection of identifiers (variables, functions, etc.).
     - Python's namespaces include:
       - **Local:** Variables within a function.
       - **Global:** Variables defined at the script’s top level.
       - **Built-in:** Core Python identifiers (e.g., `print`).
   - **Scope:** 
     - Defines where a variable can be accessed.
     - **Example:** 
       ```python
       x = 10  # Global scope
       def func():
           y = 5  # Local scope
       ```
   - **Packages:** 
     - Directories containing multiple Python modules and an `__init__.py` file.
     - **Example:**
       ```bash
       mypackage/
       ├── __init__.py
       └── module1.py
       ```

---

### 13. **Export Data from SQLite to a CSV File**
   ```python
   import sqlite3
   import csv

   conn = sqlite3.connect('database.db')
   cursor = conn.cursor()

   # Execute query to fetch data
   cursor.execute('SELECT * FROM table_name')

   # Export to CSV
   with open('output.csv', 'w', newline='') as file:
       writer = csv.writer(file)
       writer.writerow([i[0] for i in cursor.description])  # Column headers
       writer.writerows(cursor.fetchall())
   ```

---

### 14. **Loading a Module in Code**
   - **Importing standard modules:**
     ```python
     import math
     print(math.sqrt(16))  # 4.0
     ```
   - **Importing custom modules:**
     ```python
     from mymodule import myfunction
     myfunction()
     ```

---

### 15. **`connect()` and `execute()` Methods in `sqlite3`**
   - **`connect()` Method:** 
     - Establishes a connection to the SQLite database.
     - **Example:**
       ```python
       conn = sqlite3.connect('database.db')
       ```
   - **`execute()` Method:**
     - Executes a single SQL statement.
     - **Example:**
       ```python
       conn.execute('CREATE TABLE students (id INTEGER PRIMARY KEY, name TEXT)')
       conn.commit()  # Commit changes
       ```

---

### 16. **CRUD Operations Using `execute()`**
   - **Insert Data:**
     ```python
     conn.execute("INSERT INTO Student_tbl (id, name, dob, class, gender, city) VALUES (1, 'John', '2000-01-01', '10th', 'M', 'New York')")
     ```
   - **Update Data:**
     ```python
     conn.execute("UPDATE Student_tbl SET city = 'Los Angeles' WHERE id = 1")
     ```
   - **Delete Data:**
     ```python
     conn.execute("DELETE FROM Student_tbl WHERE id = 1")
     ```

---

### 17. **`open()` Function in Python**
   - **Definition:** Opens a file and returns a file object.
   - **Modes:**
     - `'r'`: Read.
     - `'w'`: Write (overwrites existing content).
     - `'a'`: Append.
   - **Example:**
     ```python
     with open('example.txt', 'r') as file:
         content = file.read()
         print(content)
     ```

---

### 18. **CSV Functions: `reader()`, `writer()`, `writerows()`, `DictReader()`, `DictWriter()`**
   - **`reader()`:** Reads CSV rows as lists.
     ```python
     with open('data.csv', 'r') as file:
         reader = csv.reader(file)
         for row in reader:
             print(row)
     ```
   - **`writer()`:** Writes rows to a CSV.
     ```python
     with open('output.csv', 'w', newline='') as file:
         writer = csv.writer(file)
         writer.writerow(['ID', 'Name'])  # Column headers
     ```
   - **`writerows()`:** Writes multiple rows.
     ```python
     writer.writerows([[1, 'John'], [2, 'Alice']])
     ```
   - **`DictReader()`:** Reads CSV as dictionaries.
     ```python
     with open('data.csv', 'r') as file:
         reader = csv.DictReader(file)
         for row in reader:
             print(row['Name'])
     ```
   - **`DictWriter()`:** Writes dictionaries to CSV.
     ```python
     with open('output.csv', 'w', newline='') as file:
         fieldnames = ['ID', 'Name']
         writer = csv.DictWriter(file, fieldnames=fieldnames)
         writer.writeheader()
         writer.writerow({'ID': 1, 'Name': 'John'})
     ```

---

### 19. **Different Types of Data Structures in Pandas**  
Pandas provides powerful data structures for data manipulation and analysis:
- **Series:**  
  A one-dimensional labeled array capable of holding any data type (integers, strings, etc.).  
  ```python
  import pandas as pd
  s = pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])
  print(s)
  ```

- **DataFrame:**  
  A two-dimensional labeled data structure, similar to a table in SQL or Excel spreadsheet.  
  ```python
  data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
  df = pd.DataFrame(data)
  print(df)
  ```

- **Panel (Deprecated):**  
  Used for handling 3D data; now replaced by multi-index DataFrames.

---

### 20. **Ways to Create a DataFrame in Pandas**  
1. **From a Dictionary:**  
   ```python
   data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
   df = pd.DataFrame(data)
   ```

2. **From a List of Dictionaries:**  
   ```python
   data = [{'a': 1, 'b': 2}, {'a': 3, 'b': 4}]
   df = pd.DataFrame(data)
   ```

3. **From a 2D Array:**  
   ```python
   data = [[1, 2], [3, 4]]
   df = pd.DataFrame(data, columns=['A', 'B'])
   ```

4. **From a CSV or Excel file:**  
   ```python
   df = pd.read_csv('data.csv')
   ```

---

### 21. **Extract and Write Commands for CSV and Excel Files**  
- **Extract Data:**  
  ```python
  df = pd.read_csv('data.csv')
  print(df.head())  # View first rows
  ```

- **Write to CSV:**  
  ```python
  df.to_csv('output.csv', index=False)
  ```

- **Write to Excel:**  
  ```python
  df.to_excel('output.xlsx', index=False)
  ```

---

### 22. **Key DataFrame Functions**  
- **`head()`:** Returns the first n rows (default 5).  
  ```python
  print(df.head(3))
  ```

- **`tail()`:** Returns the last n rows.  
  ```python
  print(df.tail(3))
  ```

- **`loc`:** Accesses rows and columns by labels.  
  ```python
  print(df.loc[0, 'Age'])
  ```

- **`iloc`:** Accesses rows and columns by index.  
  ```python
  print(df.iloc[0, 1])
  ```

- **`values`:** Returns a NumPy array of the DataFrame.  
  ```python
  print(df.values)
  ```

- **`to_numpy()`:** Converts DataFrame to NumPy array.  
  ```python
  arr = df.to_numpy()
  ```

- **`describe()`:** Generates summary statistics.  
  ```python
  print(df.describe())
  ```

---

### 23. **Measures of Central Tendency: NumPy Methods**  
- **Mean:**  
  ```python
  import numpy as np
  data = [1, 2, 3, 4, 5]
  print(np.mean(data))  # Output: 3.0
  ```

- **Median:**  
  ```python
  print(np.median(data))  # Output: 3.0
  ```

- **Mode:**  
  NumPy doesn’t directly provide a mode function; use `scipy`:  
  ```python
  from scipy import stats
  print(stats.mode(data))
  ```

- **Standard Deviation (`std`):**  
  ```python
  print(np.std(data))  # Measures data spread
  ```

- **Variance (`var`):**  
  ```python
  print(np.var(data))
  ```

---

### 24. **Installing Matplotlib**  
   ```bash
   pip install matplotlib
   ```

---

### 25. **`subplot()`, `legend()`, `columns()`, `len()` Functions**  
- **`subplot()`:** Creates multiple plots in one figure.  
  ```python
  import matplotlib.pyplot as plt
  plt.subplot(1, 2, 1)  # 1 row, 2 columns, first plot
  plt.plot([1, 2, 3])
  plt.subplot(1, 2, 2)  # Second plot
  plt.plot([4, 5, 6])
  plt.show()
  ```

- **`legend()`:** Adds a legend to the plot.  
  ```python
  plt.plot([1, 2, 3], label='Line 1')
  plt.legend()
  plt.show()
  ```

- **`columns()`:** Returns column labels of a DataFrame.  
  ```python
  print(df.columns)
  ```

- **`len()`:** Returns the number of elements in an object.  
  ```python
  print(len(df))  # Number of rows
  ```

---

### 26. **Scatter Plot with Example**  
   ```python
   plt.scatter([1, 2, 3], [4, 5, 6], color='red')
   plt.title('Scatter Plot Example')
   plt.xlabel('X-axis')
   plt.ylabel('Y-axis')
   plt.show()
   ```

---

### 27. **Bar Chart Concepts**  
- **`bar()`:** Creates vertical bar charts.  
  ```python
  plt.bar(['A', 'B', 'C'], [10, 20, 15])
  plt.title('Bar Chart')
  plt.xlabel('Categories')
  plt.ylabel('Values')
  plt.show()
  ```

---

### 28. **Concepts of Histogram Chart with Example**  

A **histogram** represents the distribution of a dataset by dividing it into bins (intervals) and counting the number of observations that fall into each bin. Unlike bar charts, histograms are used for continuous data.

**Code Example:**  
```python
import matplotlib.pyplot as plt

data = [10, 15, 20, 25, 20, 30, 35, 40, 45, 50, 55, 60]

# Plotting the histogram
plt.hist(data, bins=5, color='blue', edgecolor='black')
plt.title('Histogram Example')
plt.xlabel('Value Ranges')
plt.ylabel('Frequency')
plt.show()
```

**Explanation:**  
- **`bins`:** Determines the number of intervals. Here, the data is divided into 5 bins.
- **`color`:** Sets the bar color.
- **`edgecolor`:** Colors the edges of the bars for better visibility.

---

### 29. **Difference Between Scatter, Line, Histogram, and Bar Charts**  

| **Feature**        | **Scatter Plot**                     | **Line Chart**                     | **Histogram**                     | **Bar Chart**                     |
|--------------------|--------------------------------------|------------------------------------|-----------------------------------|-----------------------------------|
| **Purpose**        | Displays relationship between two variables | Shows trends over time or continuous data | Shows frequency distribution of continuous data | Compares categories or discrete data |
| **Data Type**      | Numerical, bivariate                 | Numerical, univariate              | Numerical, continuous             | Categorical or discrete numerical |
| **Axes**           | Both axes numeric                    | X-axis usually categorical or time | X-axis numeric (bins)             | X-axis categorical, Y-axis numeric |
| **Representation** | Points (dots)                        | Lines connecting points            | Bars representing bins            | Separate bars for each category   |
| **Example Use**    | Correlation between height and weight | Monthly sales trend                | Age distribution in a class       | Comparing sales across products   |

---

### 30. **Extract Specific Attributes and Rows from DataFrame**  

You can extract specific columns (attributes) or rows from a DataFrame using methods like `loc[]`, `iloc[]`, and column indexing.

**Example DataFrame:**  
```python
import pandas as pd

data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Los Angeles', 'Chicago']
}
df = pd.DataFrame(data)
```

**Extract Specific Columns (Attributes):**  
```python
# Extracting 'Name' and 'Age' columns
selected_columns = df[['Name', 'Age']]
print(selected_columns)
```

**Extract Specific Rows:**  
```python
# Extracting first two rows using iloc
selected_rows = df.iloc[0:2]
print(selected_rows)
```

**Extract Rows Based on Condition:**  
```python
# Extract rows where Age is greater than 28
filtered_rows = df[df['Age'] > 28]
print(filtered_rows)
```
