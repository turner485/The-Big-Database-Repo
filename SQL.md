## SQL (Structured Query Language)
```
-- Simple Browsing --
SHOW DATABASES;
SHOW TABLES;
SELECT * FROM dummy_table
DESC dummy_table
SHOW PROCESSLIST;
KILL process_number;

-- Create / Use / Drop Database --
CREATE DATABASE DatabaseName;
USE DatabaseName;
DROP DATABASE DatabaseName;
ALTER DATABASE DatabaseName CHARACTER SET utf8;

-- Delete / Drop -- 
DROP TABLE dummy_table;
DROP TABLE IF EXISTS table;
DROP TABLE dummy_table, dummy_table_2
``` 
```
-- Logic --
FOR EACH
IF
ELSEIF
ELSE
END IF
```
```
-- Conditionals -- 
field1 = value1
field1 <> value1
field1 LIKE 'value _ %'
field1 IS NULL
field1 IS NOT NULL
field1 IS IN (value1, value2)
field1 IS NOT IN (value1, value2)
condition1 AND condition2
condition1 OR condition2
```
```
-- Wildcards --
% = any
# = characters (plural)
_ = character (single)
```
```
-- Keywords --
https://www.w3schools.com/sql/sql_ref_keywords.asp

-- Primary Keys --
The PRIMARY KEY constraint uniquely identifies each record in a table.
Primary keys must contain UNIQUE values, and cannot contain NULL values.

-- Foreign Keys --
The FOREIGN KEY constraint is used to prevent actions that would destroy links between tables.

A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the PRIMARY KEY in another table.

-- Triggers --
Triggers can be set up in RDMS as a sort of automation, when one thing happens it can can 'trigger' an action elsewhere in the db.

more info;
https://www.datacamp.com/tutorial/sql-triggers

-- SQL field data types --  
More info https://www.w3schools.com/sql/sql_datatypes.asp

LIKE - Case sensitive
ILIKE - Not case sensitive
```