# SQL Basics

## What is SQL?

SQL stands for:

**Structured Query Language**

SQL is a programming language used to communicate with relational databases.

It allows users to:

- Retrieve data
- Insert new data
- Update existing data
- Delete data
- Manage database information

SQL is commonly used with database systems such as:

- MySQL
- PostgreSQL
- Microsoft SQL Server
- Oracle Database

---

# SELECT Statement

`SELECT` is used to retrieve data from a database.

Example:

```sql
SELECT CustomerName
FROM Customers;

This retrieves the CustomerName column from the Customers table.
FROM Statement

FROM specifies the table where the data will be retrieved from.

Example:

SELECT CustomerName
FROM KCC.dbo.Customers;

AS Keyword

AS is used to rename columns or tables using aliases.

Example:

SELECT CustomerName AS [Customer Name]
FROM KCC.dbo.Customers;

Output column name:

Customer Name

DISTINCT

DISTINCT removes duplicate values from the result.

Example:

SELECT DISTINCT CustomerName
FROM KCC.dbo.Customers;

Asterisk (*)

The * symbol selects all columns from a table.

Example:

SELECT *
FROM KCC.dbo.Customers;

Returns all columns from the table.
SELECT TOP

TOP limits the number of rows returned.

Example:

SELECT TOP(3) *
FROM KCC.dbo.Customers;

Returns only the first 3 rows.
SQL Comments

Comments are used to add explanations inside SQL code.
Single-line Comment

-- This is a comment

Multi-line Comment

/*
This is
a comment
*/

WHERE Clause

WHERE filters data based on a condition.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE State = 'WA';

Returns customers from Washington.
Comparison Operators
Not Equal

Can be written as:

<>

or:

!=

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE State <> 'WA';

Returns customers that are not from Washington.
IN Operator

IN checks multiple possible values.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE State IN ('WA','NY','YT');

Equivalent to using multiple OR conditions.
NOT IN Operator

Returns values that are not included in a list.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE State NOT IN ('WA','NY','YT');

AND and OR Operators

Used to combine multiple conditions.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE CustomerName = 'Trestles'
AND 
(Country = 'United States' OR Country = 'France');

LIKE Operator

LIKE is used for pattern matching.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE CustomerName LIKE 'A%';

A% means:

    Starts with the letter A

    Followed by any characters

Example matches:

Adam
Andrew
Alice

NOT LIKE Operator

Returns values that do not match a pattern.

Example:

SELECT *
FROM KCC.dbo.Customers
WHERE CustomerName NOT LIKE 'A%';

Comparison Operators
Greater Than

WHERE OrderTotal > 1000

Less Than

WHERE OrderTotal < 1000

Equal

WHERE OrderTotal = 1000

BETWEEN Operator

BETWEEN selects values inside a range.

Example:

SELECT *
FROM Orders
WHERE OrderTotal BETWEEN 1000 AND 2000;

Returns orders between 1000 and 2000.
JOIN

A JOIN combines data from multiple tables.

Example:

Database contains:

Orders Table
Customers Table

The customer information is stored in the Customers table, while order information is stored in the Orders table.

Example:

SELECT 
OrderDate,
Phone,
CustomerName

FROM dbo.Orders

JOIN dbo.Customers

ON dbo.Orders.CustomerID = dbo.Customers.CustomerID;

Using Aliases

Aliases make SQL queries easier to read.

Example:

SELECT
o.OrderDate,
c.Phone,
c.CustomerName

FROM dbo.Orders o

JOIN dbo.Customers c

ON o.CustomerID = c.CustomerID;

Aliases:

o = Orders
c = Customers

INNER JOIN

INNER JOIN returns only records that exist in both tables.

Example:

SELECT *

FROM dbo.Orders o

INNER JOIN dbo.Customers c

ON o.CustomerID = c.CustomerID;

Example result:

Only customers who have matching orders.
OUTER JOIN

OUTER JOIN returns matching records and also unmatched records from one side.

Example:

SELECT *

FROM dbo.Orders o

LEFT OUTER JOIN dbo.Customers c

ON o.CustomerID = c.CustomerID;

A LEFT JOIN returns:

    All records from the left table

    Matching records from the right table

    NULL values where no match exists

Specifying Columns from Tables

When multiple tables contain columns with the same name, specify the table name or alias.

Example:

SELECT
o.OrderDate,
c.Phone,
c.CustomerName

FROM dbo.Orders o

LEFT JOIN dbo.Customers c

ON o.CustomerID = c.CustomerID;

This:

    Avoids confusion

    Makes queries clearer

    Improves readability

SQL and Web Security

Understanding SQL is important for web security because many applications store sensitive data inside databases.

Common SQL-related vulnerabilities:

    SQL Injection (SQLi)

    Authentication bypass

    Data disclosure

    Unauthorized data access

Important rule:

    Never trust user input directly in SQL queries. Always use secure methods such as parameterized queries.


This is a good addition to your cybersecurity GitHub because SQL knowledge is required before learning **SQL Injection** in PortSwigger.
