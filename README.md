# SQL Cheat Sheet
## DDL (Data Definition Language)


- **CREATE**: Creates a new database object, such as a table.
 ```sql
 CREATE TABLE table_name (
      column1 datatype,
      column2 datatype,
      ...
 );
 ```
- **ALTER**: Modifies a database object.
 ```sql
 ALTER TABLE table_name ALTER COLUMN column_name TYPE new_datatype;
 ```
- **DROP**: Deletes database objects.
 ```sql
 DROP TABLE table_name;
 ```
- **TRUNCATE**: Removes all records from a table.
 ```sql
 TRUNCATE TABLE table_name;
 ```

## DML (Data Manipulation Language)

- **INSERT**: Inserts a new row into a database table.
 ```sql
 INSERT INTO table_name (column1, column2) VALUES (value1, value2);
 ```
- **UPDATE**: Modifies an existing row in a database table.
 ```sql
 UPDATE table_name SET column1 = value1 WHERE condition;
 ```
- **DELETE**: Deletes a row from a database table.
 ```sql
 DELETE FROM table_name WHERE condition;
 ```
- **SELECT**: Retrieves data from a database.
 ```sql
 SELECT column1, column2 FROM table_name WHERE condition;
 ```

## DCL (Data Control Language)

- **GRANT**: Assigns user permissions to access database objects.
 ```sql
 GRANT SELECT, INSERT ON table_name TO user_name;
 ```
- **REVOKE**: Removes previously granted user permissions for accessing database objects.
 ```sql
 REVOKE SELECT, INSERT ON table_name FROM user_name;
 ```

## SQL Constraints

- **Primary Key**: Ensures uniqueness and non-nullability of a column.
 ```sql
 CREATE TABLE table_name (
      column_name datatype PRIMARY KEY
 );
 ```
- **Foreign Key**: Links two tables and ensures referential integrity.
 ```sql
 CREATE TABLE table_name (
      column_name datatype,
      FOREIGN KEY (column_name) REFERENCES other_table(column_name)
 );
 ```
- **Unique**: Ensures all values in a column are unique.
 ```sql
 CREATE TABLE table_name (
      column_name datatype UNIQUE
 );
 ```
- **Check**: Enforces domain integrity by restricting values that can be inserted into a column.
 ```sql
 CREATE TABLE table_name (
      column_name datatype CHECK (condition)
 );
 ```

## SQL Joins

- **INNER JOIN**: Returns records that have matching values in both tables.
 ```sql
 SELECT column1, column2 FROM table1 INNER JOIN table2 ON table1.column1 = table2.column1;
 ```
- **LEFT JOIN**: Returns all records from the left table, and the matched records from the right table.
 ```sql
 SELECT column1, column2 FROM table1 LEFT JOIN table2 ON table1.column1 = table2.column1;
 ```
- **RIGHT JOIN**: Returns all records from the right table, and the matched records from the left table.
 ```sql
 SELECT column1, column2 FROM table1 RIGHT JOIN table2 ON table1.column1 = table2.column1;
 ```
- **FULL JOIN**: Returns all records when there is a match in either left or right table.
 ```sql
 SELECT column1, column2 FROM table1 FULL JOIN table2 ON table1.column1 = table2.column1;
 ```

## Logical Operators

- **AND**: Returns true if both conditions are true.
 ```sql
 SELECT column1, column2 FROM table_name WHERE condition1 AND condition2;
 ```
- **OR**: Returns true if either condition is true.
 ```sql
 SELECT column1, column2 FROM table_name WHERE condition1 OR condition2;
 ```
- **NOT**: Returns true if the condition is false.
 ```sql
 SELECT column1, column2 FROM table_name WHERE NOT condition;
 ```

## Sorting Data

- **Order By Ascending**: Sorts the result set in ascending order.
```sql
SELECT column1, column2 FROM table_name ORDER BY column1 ASC;
```
- **Order By Descending**: Sorts the result set in descending order.
```sql
SELECT column1, column2 FROM table_name ORDER BY column1 DESC;
```
- **Order By Multiple Columns**: Sorts the result set by multiple columns.
```sql
SELECT column1, column2 FROM table_name ORDER BY column1 ASC, column2 DESC;
```

## Filtering Data

- **Filtering on Numeric Columns**: Filters rows based on numeric conditions.
```sql
SELECT * FROM table_name WHERE column_name >= 3;
```
- **Filtering on Text Columns**: Filters rows based on text conditions.
```sql
SELECT * FROM table_name WHERE column_name = 'value';
```
- **Filtering with LIKE**: Filters rows based on pattern matching.
```sql
SELECT * FROM table_name WHERE column_name LIKE 'pattern%';
```
- **Filtering with IN**: Filters rows where a column's value is in a list of values.
```sql
SELECT * FROM table_name WHERE column_name IN ('value1', 'value2');
```
- **Filtering with BETWEEN**: Filters rows where a column's value is within a range.
```sql
SELECT * FROM table_name WHERE column_name BETWEEN value1 AND value2;
```
- **Filtering with NULL**: Filters rows where a column's value is NULL or not NULL.
```sql
SELECT * FROM table_name WHERE column_name IS NULL;
SELECT * FROM table_name WHERE column_name IS NOT NULL;
```

## Combining Sorting and Filtering

- **Sorting and Filtering Together**: Combines sorting and filtering in a single query.
```sql
SELECT column1, column2 FROM table_name WHERE condition ORDER BY column1 ASC;
```

```

This cheat sheet combines the essential concepts of SQL, including DDL, DML, DCL, constraints, joins, and logical operators, providing a comprehensive guide for quick reference.

Citations:
[1] https://www.salvis.com/blog/2020/08/28/formatting-sql-code-blocks-in-markdown-files/
[2] https://hackr.io/blog/sql-cheat-sheet
[3] https://gist.github.com/janikvonrotz/6e27788f662fcdbba3fb
[4] https://thequickblog.com/sql-cheat-sheet-basic-ddl-and-dml-commands/
[5] https://blog.enterprisedna.co/sql-cheat-sheet/
[6] https://zerotomastery.io/cheatsheets/sql-cheat-sheet/
[7] https://www.sqlservercentral.com/articles/creating-markdown-formatted-text-for-results-from-sql-server-tables
[8] https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/
[9] https://learnsql.com/blog/what-is-dql-ddl-dml-in-sql/
[10] https://medium.com/analytics-vidhya/understanding-sql-with-sample-ddl-and-dml-commands-5d07ecc68d8e
[11] https://www.sparkcodehub.com/sql-dml
[12] https://zephyrnet.com/sql-commands-ddl-dml-dcl-tcl-dql-types-syntax-and-examples/
[13] https://learnsql.com/blog/sql-basics-cheat-sheet/
[14] https://www.markdownguide.org/cheat-sheet/
[15] https://www.comparitech.com/net-admin/sql-commands-cheat-sheet/
