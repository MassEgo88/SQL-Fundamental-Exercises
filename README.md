# SQL-Fundamental-Exercises
"This repository contains a series of hands-on written SQL fundamental exercises

# SQL Fundamentals – Learning Summary

This document highlights the key SQL fundamentals I have learned over the past few weeks. Each section includes core concepts and examples that helped me understand how to retrieve, manipulate, and analyze data effectively.

---

## Table of Contents

* SELECT Statement
* FROM Statement
* WHERE Statement
* Filtering
* Aggregation
* CASE Statements
* Joins
* UNION
* HAVING Statement
* Sorting (ORDER BY)
* NULL Handling
* Date Functions

---

## SELECT Statement

The `SELECT` statement is used to specify the columns you want to retrieve from a table.

```sql
SELECT column_name FROM table_name;
```

---

## FROM Statement

The `FROM` statement specifies the source of the data, including the database, schema, and table.

```sql
SELECT * FROM database.schema.table_name;
```

---

## WHERE Statement (Filtering)

The `WHERE` clause is used to filter rows based on specific conditions.

```sql
SELECT * 
FROM table_name
WHERE condition;
```

---

## Filtering

Filtering allows you to narrow down results using conditions such as:

* `=`, `>`, `<`
* `IN`
* `BETWEEN`
* `LIKE`

---

## Aggregation

Aggregation functions summarize data into meaningful insights.

Common functions:

* `SUM()` – total value
* `COUNT()` – number of rows
* `AVG()` – average value
* `MIN()` – smallest value
* `MAX()` – largest value

```sql
SELECT COUNT(*) AS total_rows
FROM table_name;
```

---

## CASE Statements

`CASE` statements create new columns based on conditions (useful for categorization or flags).

```sql
SELECT 
  price,
  CASE 
    WHEN price > 500000 THEN 'High'
    ELSE 'Low'
  END AS price_category
FROM table_name;
```

---

## Joins

Joins combine data from multiple tables using a common column.

Types of joins:

* `INNER JOIN` – returns matching records
* `LEFT JOIN` – returns all from left table + matches
* `RIGHT JOIN` – returns all from right table + matches

```sql
SELECT *
FROM table1
INNER JOIN table2
ON table1.id = table2.id;
```

---

## UNION

`UNION` combines results from two or more SELECT queries.

```sql
SELECT column_name FROM table1
UNION
SELECT column_name FROM table2;
```

---

## HAVING Statement

The `HAVING` clause filters aggregated data (used with GROUP BY).

```sql
SELECT category, COUNT(*)
FROM table_name
GROUP BY category
HAVING COUNT(*) > 10;
```

---

## Sorting (ORDER BY)

Sorting arranges data in ascending or descending order.

```sql
SELECT *
FROM table_name
ORDER BY column_name DESC;
```

---

## NULL Handling

NULL represents missing or unknown data.

Common functions:

* `IS NULL`
* `IS NOT NULL`
* `COALESCE()` – replaces NULL with a value

```sql
SELECT *
FROM table_name
WHERE column_name IS NULL;
```

```sql
SELECT COALESCE(column_name, 0)
FROM table_name;
```

---

## Date Functions

Date functions help analyze time-based data.

Common functions:

* `CURRENT_DATE`
* `EXTRACT()` (year, month, day)
* `DATE_TRUNC()`

```sql
SELECT CURRENT_DATE;
```

```sql
SELECT EXTRACT(YEAR FROM sale_date) AS sale_year
FROM table_name;
```

```sql
SELECT DATE_TRUNC('month', sale_date)
FROM table_name;
```

---

## Conclusion

These exercises helped me build a strong foundation in SQL, enabling me to:

* Retrieve and filter data efficiently
* Perform aggregations and analysis
* Combine datasets using joins
* Handle missing values and date-based data

This knowledge forms the foundation for advanced data analysis and business intelligence workflows.



