# 🗄 SQL Notes

> Detailed notes for **Module 4** of **Course 4 – Tools of the Trade: Linux and SQL** from the Google Cybersecurity Professional Certificate.

---

# 📑 Contents

- Introduction to Databases
- Querying Databases with SQL
- Basic SQL Queries
- Filtering Data
- Comparison Operators
- Logical Operators
- SQL Joins
- Aggregate Functions
- Practical Labs
- Module Summary

---

<details open>
<summary><h1>📘 Module 4 — Databases & SQL</h1></summary>

## 🎯 What This Module Covers

Learned the fundamentals of relational databases and SQL, including querying data, filtering results, joining multiple tables, and summarizing information using aggregate functions.

---

<details>
<summary><h2>🗄 Database Fundamentals</h2></summary>

## Database

An organized collection of data that can be efficiently stored, managed, and retrieved.

---

## Relational Database

Stores data in **tables** that are related to one another using keys.

---

## Table

A collection of related data organized into rows and columns.

---

## Row (Record)

Represents one complete record in a table.

---

## Column (Field)

Represents one attribute of the data.

Example:

| EmployeeID | Name | Department |
|------------|------|------------|

EmployeeID, Name and Department are columns.

---

## Primary Key

- Uniquely identifies every row
- Cannot contain duplicate values
- Cannot be NULL

Example:

```
EmployeeID
```

---

## Foreign Key

- Connects one table with another
- References the Primary Key of another table
- Maintains relationships between tables

</details>

---

<details>
<summary><h2>💻 SQL Basics</h2></summary>

## SQL (Structured Query Language)

Used to communicate with relational databases.

Common uses:

- Retrieve data
- Insert records
- Update records
- Delete records
- Filter information
- Sort results
- Join tables

---

## SQL vs Linux Filtering

| Linux | SQL |
|--------|-----|
| Works with files & directories | Works with databases |
| Uses commands like grep, find | Uses SQL queries |
| Unstructured output | Structured tabular output |
| Cannot join data | Can join multiple tables |

---

## Accessing SQL

Example:

```bash
sqlite3
```

After opening SQLite, commands are interpreted as SQL queries instead of Linux commands.

</details>

---

<details>
<summary><h2>📝 Basic SQL Queries</h2></summary>

## Basic Query Structure

```sql
SELECT column_name
FROM table_name;
```

---

## SELECT

Specifies which columns to retrieve.

```sql
SELECT firstname, lastname
FROM employees;
```

---

## Select All Columns

```sql
SELECT *
FROM employees;
```

---

## FROM

Specifies the table to query.

---

## ORDER BY

Sorts query results.

Ascending (default)

```sql
ORDER BY city;
```

Descending

```sql
ORDER BY city DESC;
```

Sort using multiple columns

```sql
ORDER BY country, city;
```

</details>

---

<details>
<summary><h2>🔍 Filtering Data</h2></summary>

## WHERE

Filters records based on a condition.

```sql
SELECT *
FROM employees
WHERE title='IT Staff';
```

---

## LIKE

Searches for patterns.

```sql
WHERE title LIKE 'IT%'
```

---

## Wildcards

### %

Represents zero or more characters.

Examples

```text
IT%
%admin
%user%
```

---

### _

Represents exactly one character.

Example

```text
N_
```

Matches:

```
NY
NV
NT
```

</details>

---

<details>
<summary><h2>⚖ Comparison Operators</h2></summary>

| Operator | Meaning |
|----------|---------|
| = | Equal |
| <> | Not Equal |
| != | Not Equal |
| > | Greater Than |
| < | Less Than |
| >= | Greater Than or Equal |
| <= | Less Than or Equal |

---

### BETWEEN

Filters values within a range.

```sql
WHERE hiredate
BETWEEN '2023-01-01'
AND '2023-12-31';
```

**BETWEEN is inclusive.**

</details>

---

<details>
<summary><h2>🧠 Logical Operators</h2></summary>

## AND

Both conditions must be true.

```sql
WHERE country='USA'
AND department='IT'
```

---

## OR

Either condition can be true.

```sql
WHERE country='USA'
OR country='Canada'
```

---

## NOT

Excludes matching records.

```sql
WHERE NOT country='USA'
```

Logical operators can be combined to create more specific filters.

</details>

---

<details>
<summary><h2>🔗 SQL Joins</h2></summary>

Joins combine information from multiple related tables.

---

## INNER JOIN

Returns only matching rows.

```sql
SELECT *
FROM employees
INNER JOIN machines
ON employees.device_id = machines.device_id;
```

---

## LEFT JOIN

Returns:

- All rows from left table
- Matching rows from right table

---

## RIGHT JOIN

Returns:

- All rows from right table
- Matching rows from left table

---

## FULL OUTER JOIN

Returns all rows from both tables.

Useful when combining complete datasets.

</details>

---

<details>
<summary><h2>📊 Aggregate Functions</h2></summary>

Aggregate functions perform calculations on multiple rows and return a single value.

| Function | Purpose |
|----------|---------|
| COUNT() | Count rows |
| AVG() | Average |
| SUM() | Total |

---

### COUNT

```sql
SELECT COUNT(firstname)
FROM customers;
```

---

### AVG

```sql
SELECT AVG(price)
FROM products;
```

---

### SUM

```sql
SELECT SUM(amount)
FROM invoices;
```

Aggregate functions can also be combined with filters.

Example

```sql
SELECT COUNT(*)
FROM customers
WHERE country='USA';
```

</details>

---

<details>
<summary><h2>🧪 Practical Labs Completed</h2></summary>

Throughout this module, I completed hands-on SQL activities covering:

- Understanding relational databases
- Writing SELECT queries
- Retrieving specific columns
- Using `SELECT *`
- Sorting results with ORDER BY
- Filtering with WHERE
- Pattern matching using LIKE
- Using `%` and `_` wildcards
- Comparison operators
- BETWEEN operator
- AND, OR and NOT filters
- Joining multiple tables
- Using aggregate functions (COUNT, AVG, SUM)

</details>

---

<details>
<summary><h2>🎯 Module Summary</h2></summary>

By completing this module, I learned how to:

- Understand relational databases and table relationships
- Write basic SQL queries
- Retrieve and sort data
- Filter information efficiently
- Search using wildcards and patterns
- Work with numeric and date filters
- Combine conditions using logical operators
- Join multiple tables to retrieve related information
- Summarize data using aggregate functions
- Reinforce every concept through hands-on SQL labs

</details>

</details>