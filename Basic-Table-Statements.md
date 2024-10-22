# Basic Table Statements
Select, Insert, Delete & update

### SELECT

- __Used to retrieve data from one or more tables in a database.__
- `SELECT` is one of the most fundamental SQL commands.
- It allows you to specify which columns to fetch, apply filtering conditions, sort results, and perform various operations on the data. 
- The `SELECT` statement is versatile, supporting joins, subqueries, aggregations, and more, making it essential for data querying and analysis in relational databases.

```
-- Examples 1 --
SELECT * from user_table;

-- Example 2 -- 
SELECT * col1, col2 from user_table;
```

### INSERT

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
### UPDATE
The `UPDATE` statement is used to modify the existing records in a table.

When using the `UPDATE` statement you will see we need to be using there `WHERE` statement also, we will talk about that further on.

```
-- Example --
UPDATE user_table
SET col1 = value1, col2 = value2 
WHERE condition;
```
Now the above is just the generic syntax for the `UPDATE` statement. to get a better understanding lets to a dummy query.
```
-- Example --
UPDATE user_table
SET user_name = 'John Doe', city_name = 'London'
WHERE user_id = 1;
```
An __important__ thing to note:  
You need to be careful when using the `WHERE` clause, for the statement above we can be sure we are only updating the fields of a single row because are using a unique identifier otherwise known as a `PRIMARY KEY` (We'll talk about those further on) If we were use something like
```
WHERE user_name = 'John Doe'
```
We may be at risk of changing more than just the 1 row because there maybe more than 1 john doe in the user table.
### DELETE
The `DELETE` statement is used to delete existing records in a table.  

Much like the `UPDATE` statement above, the `DELETE` statement uses the `WHERE` clause so be careful when using.

It can be used to `DELETE` single rows or entire tables.
```
-- Example -- Delete a row --
DELETE from user_table
WHERE user_id = 1;

-- Example -- Delete All rows in table --
DELETE from user_table;

-- Example -- DROP entire table --
DROP table user_table;