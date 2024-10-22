# SQL Statement Theory
__So before we get into some SQL queries, it's a good idea to know exactly what each statement and clause do (I know right, the boring stuff)__

__But It is definitely the right way to go before trying to write complex queries, and plus at the time of writing this I was still learning to!__

Now we have already touched upon a few statements like `SELECT` `UPDATE` `DELETE` `WHERE`

But in this doc we will go through most if not all all the of the basic statements and possibly more.
## The Basics
### `SELECT`
The `SELECT` statement is used to select data from a database.
```
-- Example 1 --
SELECT * from user_table;
-- Example 2 --
SELECT user_name from user_table;
```
### `FROM`
The `FROM` command is used to specify which table to select or delete data from.
```
-- Example 1 --
SELECT * from user_table;
-- Example 2 --
SELECT user_name from user_table;
-- Example 3 --
DELETE FROM user_table
WHERE user_name = 'John Doe';
```
### `WHERE`
The `WHERE` clause is used to filter records.  

It is used to extract only those records that fulfill a specified condition.

```
SELECT * FROM user_table
WHERE user_id = 1;
```
__Note__: The `WHERE` clause is not only used in `SELECT` statements, it is also used in `UPDATE`, `DELETE`, etc!

### `DELETE`
The DELETE statement is used to delete existing records in a table.
```
-- Example -- Delete a row --
DELETE from user_table
WHERE user_id = 1;

-- Example -- Delete All rows in table --
DELETE from user_table;

-- Example -- DROP entire table --
DROP table user_table;
```
### `UPDATE`
The `UPDATE` statement is used to modify the existing records in a table.

```
-- Example --
UPDATE user_table
SET user_name = 'John Doe', city_name = 'London'
WHERE user_id = 1;
```
### `INSERT`

`INSERT` is used in conjunction with into to insert new data into an existing table.
```
INSERT INTO
```
There are 2 different ways to insert data into a table.

1. Specify both the column names and the values to be inserted:
2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. 
```
-- Example 1 -- 
INSERT INTO user_table (col1, col2, col3)
VALUES (value1, value2, value2);

-- Example 2 -- 
INSERT INTO user_table
VALUES (value1, value2, value3, etc);
```

## Aggregate Statements

Aggregate queries in SQL are used to perform calculations on multiple rows of data, returning a single summary value or grouped results. These queries typically involve the use of aggregate functions, such as:  

`COUNT()` Returns the number of rows that match a specific condition.  
`SUM()` Calculates the total sum of a numeric column.  
`AVG()` Computes the average value of a numeric column.  
`MIN()` and `MAX()` Find the smallest and largest values in a column, respectively.  
`GROUP BY` Used to group rows that share a common value in specified columns, allowing aggregate functions to be applied to each group.  
`HAVING`: Filters the results of a GROUP BY clause based on a specified condition, similar to WHERE but for groups.

### `Count()`
The COUNT() function returns the number of rows that matches a criterion.

```
SELECT COUNT(user_name)
FROM user_table;
```