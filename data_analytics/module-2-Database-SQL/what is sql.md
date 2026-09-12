# what is SQL

## Definition

**SQL (Structured Query Language)** is a standardized programming language specifically designed for managing, querying, manipulating, and defining relational databases. It serves as the primary interface between users (or applications) and relational database management systems (RDBMS). SQL allows users to perform a wide range of operations — from simple data retrieval to complex database administration tasks — using a declarative syntax that specifies *what* data is needed rather than *how* to retrieve it.

SQL was initially developed at **IBM** in the early 1970s by **Donald D. Chamberlin** and **Raymond F. Boyce** as part of the **System R** project. It was originally called **SEQUEL (Structured English Query Language)** before being renamed to SQL. It was later standardized by the **American National Standards Institute (ANSI)** in 1986 and by the **International Organization for Standardization (ISO)** in 1987. Since then, SQL has undergone several revisions and extensions (SQL-86, SQL-89, SQL-92, SQL:1999, SQL:2003, SQL:2006, SQL:2008, SQL:2011, SQL:2016, SQL:2023).

## History of SQL

- **1970**: Edgar F. Codd publishes the relational model paper at IBM, laying the theoretical foundation for SQL.
- **1974**: IBM developers create SEQUEL (Structured English Query Language) for System R.
- **1979**: Oracle Corporation releases the first commercial SQL-based RDBMS (Oracle V2).
- **1986**: ANSI standardizes SQL (SQL-86).
- **1987**: ISO adopts the SQL standard.
- **1989–1992**: SQL-89 and SQL-92 standards refine and expand the language.
- **1999**: SQL:1999 introduces object-relational features, recursive queries, triggers, and regular expressions.
- **2003**: SQL:2003 adds XML support, window functions, and MERGE statements.
- **2006–2008**: SQL:2006 and SQL:2008 add XML transformations, TRUNCATE, and more administrative features.
- **2011**: SQL:2011 introduces temporal database features (system-versioned tables).
- **2016**: SQL:2016 adds polymorphic table functions and JSON improvements.
- **2023**: SQL:2023 adds SQL application packages and further enhancements.

## Sub-languages of SQL

SQL is divided into several sub-languages, each serving a distinct purpose:

### 1. DDL (Data Definition Language)
DDL is used to define and manage the structure (schema) of the database. It deals with creating, modifying, and deleting database objects such as tables, indexes, views, and constraints.

**Common DDL Commands:**

| Command | Description | Example |
|---------|-------------|---------|
| `CREATE` | Creates a new database object (table, index, view, etc.) | `CREATE TABLE Students (ID INT, Name VARCHAR(50), Age INT);` |
| `ALTER` | Modifies the structure of an existing database object | `ALTER TABLE Students ADD Email VARCHAR(100);` |
| `DROP` | Deletes an existing database object and all its data | `DROP TABLE Students;` |
| `TRUNCATE` | Removes all rows from a table without logging individual row deletions | `TRUNCATE TABLE Students;` |
| `RENAME` | Renames an existing database object | `RENAME TABLE Students TO Pupils;` |

### 2. DML (Data Manipulation Language)
DML is used to manipulate data within database objects — to query, insert, update, and delete records.

**Common DML Commands:**

| Command | Description | Example |
|---------|-------------|---------|
| `SELECT` | Retrieves data from one or more tables | `SELECT Name, Age FROM Students WHERE Age > 16;` |
| `INSERT` | Inserts new rows of data into a table | `INSERT INTO Students (ID, Name, Age) VALUES (104, 'Dave', 15);` |
| `UPDATE` | Modifies existing data in a table | `UPDATE Students SET Age = 16 WHERE ID = 102;` |
| `DELETE` | Removes rows from a table | `DELETE FROM Students WHERE ID = 103;` |
| `MERGE` | Combines INSERT and UPDATE operations (upsert) | `MERGE INTO Students USING temp_data ON (ID) WHEN MATCHED THEN UPDATE SET Age = temp_data.Age WHEN NOT MATCHED THEN INSERT VALUES (temp_data.ID, temp_data.Name, temp_data.Age);` |
| `CALL` | Invokes a stored procedure or function | `CALL UpdateStudentAge(101, 18);` |

### 3. DCL (Data Control Language)
DCL is used to control access to data — granting or revoking permissions and privileges to users and roles.

**Common DCL Commands:**

| Command | Description | Example |
|---------|-------------|---------|
| `GRANT` | Gives a user or role specific privileges on a database object | `GRANT SELECT, INSERT ON Students TO user1;` |
| `REVOKE` | Removes previously granted privileges | `REVOKE INSERT ON Students FROM user1;` |

### 4. TCL (Transaction Control Language)
TCL is used to manage transactions — groups of DML operations that are treated as a single unit of work.

**Common TCL Commands:**

| Command | Description | Example |
|---------|-------------|---------|
| `COMMIT` | Saves all changes made during the current transaction permanently | `COMMIT;` |
| `ROLLBACK` | Undoes all changes made during the current transaction | `ROLLBACK;` |
| `SAVEPOINT` | Sets a savepoint within a transaction to which you can later roll back | `SAVEPOINT point1;` |
| `SET TRANSACTION` | Sets characteristics of the current transaction | `SET TRANSACTION ISOLATION LEVEL READ COMMITTED;` |

### 5. DQL (Data Query Language)
Sometimes considered a subset of DML, DQL is specifically for querying data. The primary (and essentially only) DQL command is `SELECT`.

### 6. Embedded SQL
SQL statements can be embedded within host programming languages (C, Java, Python, COBOL, etc.) using specific syntax (EXEC SQL in COBOL/C, parameterized queries in Python/Java). This allows applications to interact with databases programmatically.

## Common SQL Commands with Examples

### SELECT Queries

```sql
-- Retrieve all columns from the Students table
SELECT * FROM Students;

-- Retrieve specific columns
SELECT Name, Age FROM Students;

-- Retrieve with conditions
SELECT Name, Age FROM Students WHERE Age >= 16;

-- Retrieve with sorting
SELECT Name, Age FROM Students ORDER BY Age DESC;

-- Aggregate functions
SELECT COUNT(*) AS TotalStudents, AVG(Age) AS AverageAge FROM Students;

-- Grouping and filtering
SELECT Grade, COUNT(*) AS Count FROM Students GROUP BY Grade HAVING COUNT(*) > 10;

-- Join two tables
SELECT Students.Name, Courses.CourseName
FROM Students
JOIN Enrollments ON Students.ID = Enrollments.StudentID
JOIN Courses ON Enrollments.CourseID = Courses.ID;
```

### DDL Examples

```sql
-- Create a table
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Department VARCHAR(50),
    Salary DECIMAL(10, 2),
    HireDate DATE
);

-- Add a column
ALTER TABLE Employees ADD Email VARCHAR(100);

-- Drop a column
ALTER TABLE Employees DROP COLUMN Email;

-- Drop a table
DROP TABLE Employees;

-- Create an index
CREATE INDEX idx_employees_department ON Employees(Department);

-- Create a view
CREATE VIEW HighSalaryEmployees AS
SELECT * FROM Employees WHERE Salary > 75000;
```

### DML Examples

```sql
-- Insert data
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary)
VALUES (1, 'Alice', 'Johnson', 'Engineering', 85000);

-- Update data
UPDATE Employees SET Salary = 90000 WHERE EmployeeID = 1;

-- Delete data
DELETE FROM Employees WHERE EmployeeID = 1;

-- Bulk insert
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary)
VALUES (2, 'Bob', 'Smith', 'Marketing', 65000),
       (3, 'Carol', 'White', 'Engineering', 80000);
```

### TCL Examples

```sql
-- Start a transaction
BEGIN TRANSACTION;

-- Perform multiple operations
UPDATE Employees SET Salary = Salary * 1.1 WHERE Department = 'Engineering';
DELETE FROM Employees WHERE HireDate < '2020-01-01';

-- Commit the changes
COMMIT;

-- Or rollback if something goes wrong
ROLLBACK;
```

### DCL Examples

```sql
-- Grant privileges
GRANT SELECT, INSERT, UPDATE ON Employees TO analyst_user;
GRANT ALL PRIVILEGES ON Employees TO admin_user;

-- Revoke privileges
REVOKE INSERT ON Employees FROM analyst_user;
```

## Types of SQL Operators

### Arithmetic Operators
- `+` (Addition), `-` (Subtraction), `*` (Multiplication), `/` (Division), `%` (Modulus)

### Comparison Operators
- `=` (Equal), `<>` or `!=` (Not Equal), `>` (Greater Than), `<` (Less Than), `>=` (Greater Than or Equal), `<=` (Less Than or Equal)

### Logical Operators
- `AND`, `OR`, `NOT`, `BETWEEN`, `IN`, `LIKE`, `IS NULL`, `EXISTS`, `ALL`, `ANY`

### Wildcard Operators
- `%` (Matches zero or more characters), `_` (Matches exactly one character)

## SQL Functions

### Aggregate Functions
- `COUNT()` — Counts the number of rows
- `SUM()` — Calculates the sum of a numeric column
- `AVG()` — Calculates the average value
- `MIN()` — Returns the minimum value
- `MAX()` — Returns the maximum value

### Scalar/String Functions
- `CONCAT()` — Concatenates strings
- `SUBSTRING()` — Extracts a substring
- `UPPER()` / `LOWER()` — Converts case
- `TRIM()` — Removes leading/trailing whitespace
- `LENGTH()` / `CHAR_LENGTH()` — Returns string length
- `ROUND()` — Rounds a numeric value
- `NOW()` / `CURRENT_DATE()` — Returns current date/time

## Advantages of SQL

- **Standardized**: SQL is an ANSI/ISO standard language, ensuring consistency across different database systems with minor variations.
- **Easy to Learn**: SQL uses English-like syntax that is intuitive and relatively easy to learn compared to general-purpose programming languages.
- **Powerful and Versatile**: SQL can perform complex data retrieval, manipulation, and administration tasks with concise syntax.
- **Widely Supported**: Almost every RDBMS (MySQL, PostgreSQL, Oracle, SQL Server, SQLite) supports SQL, making it universally applicable.
- **Non-Procedural**: SQL is declarative — users specify *what* they want, not *how* to get it. The DBMS engine determines the optimal execution plan.
- **Handles Large Data**: SQL is optimized for querying and managing massive datasets efficiently through indexing, query optimization, and parallel processing.
- **Data Integrity**: Through constraints, transactions, and ACID compliance, SQL helps maintain data integrity.
- **Flexibility**: Supports simple queries and complex multi-table joins, subqueries, views, stored procedures, and user-defined functions.
- **Rapid Development**: SQL enables fast development of database-driven applications with relatively little code.
- **Integration**: SQL can be embedded in host programming languages (Python, Java, C, etc.) and integrated with various tools and frameworks.
- **Community and Ecosystem**: Extensive documentation, tutorials, libraries, and a vast community of developers and DBAs.
- **Cost-Effective**: Many SQL databases (MySQL, PostgreSQL, SQLite) are open-source and free to use.

## Disadvantages of SQL

- **Steep Learning Curve for Advanced Features**: While basic SQL is easy to learn, advanced features (window functions, CTEs, complex joins, optimization) require significant expertise.
- **Vendor-Specific Extensions**: While SQL is standardized, each RDBMS vendor has its own extensions and proprietary features, which can reduce portability.
- **Complex Schema Changes**: Modifying database schemas (adding/removing columns, changing data types) can be time-consuming and risky, especially in production environments.
- **Limited Support for Unstructured Data**: SQL databases are not natively designed for storing and querying unstructured data (images, videos, documents) without additional handling.
- **Horizontal Scaling Challenges**: Scaling relational databases horizontally (across multiple servers) is more complex than scaling NoSQL databases.
- **Performance Overhead**: The overhead of maintaining ACID properties, relationships, and complex queries can impact performance in high-throughput scenarios.
- **Verbose Syntax for Simple Operations**: Some operations that are simple in a programming language may require multiple SQL statements.
- **Single Point of Failure**: In traditional client-server SQL databases, the database server can become a bottleneck or single point of failure (mitigated through replication and clustering).

## SQL vs NoSQL

| Feature | SQL (Relational) | NoSQL (Non-Relational) |
|---------|-----------------|----------------------|
| Data Model | Tables (rows and columns) | Documents, key-value, graph, wide-column |
| Schema | Fixed, predefined schema | Dynamic, flexible schema |
| Scalability | Vertical scaling preferred | Horizontal scaling preferred |
| Relationships | Native support via joins | Typically requires application-level joins |
| Consistency | ACID compliance | BASE (Basically Available, Soft state, Eventually consistent) |
| Query Language | Standardized SQL | Varies by database (e.g., MongoDB Query Language) |
| Best For | Structured data, complex queries, transactions | Unstructured data, high scalability, rapid development |
| Examples | MySQL, PostgreSQL, Oracle, SQL Server | MongoDB, Redis, Cassandra, CouchDB |

## SQL Standards

| Standard | Year | Key Features |
|----------|------|-------------|
| SQL-86 | 1986 | Initial ANSI standard; basic relational operations |
| SQL-89 | 1989 | Minor corrections and join syntax improvements |
| SQL-92 | 1992 | Major revision; added temp tables, nested queries, new date/time types |
| SQL:1999 | 1999 | Object-relational features, recursive queries, triggers, regular expressions |
| SQL:2003 | 2003 | XML support, window functions, MERGE, series generation |
| SQL:2006 | 2006 | XML transformations, embedding in programming languages |
| SQL:2008 | 2008 | TRUNCATE as DDL, BETWEEN enhancements, INSTEAD OF triggers |
| SQL:2011 | 2011 | Temporal tables, polymorphic table functions |
| SQL:2016 | 2016 | JSON improvements, polymorphic table functions |
| SQL:2023 | 2023 | SQL application packages, further syntax enhancements |