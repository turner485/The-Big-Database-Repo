## SQL (Structured Query Language)
```
-- Notes -- 

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
```
-- Browsing --
SHOW DATABASES;
SHOW TABLES;
SELECT * FROM dummy_table
DESC dummy_table
SHOW PROCESSLIST;
KILL process_number;
```
```
-- Keywords Reference --
REFER TO
https://www.w3schools.com/sql/sql_ref_keywords.asp
```
```
-- Create / Use / Drop Database --
CREATE DATABASE DatabaseName;
USE DatabaseName;
DROP DATABASE DatabaseName;
ALTER DATABASE DatabaseName CHARACTER SET utf8;
```
```
-- Create / Modify / Delete Tables --

-- Create --
CREATE TABLE dummy_table (dummy_field_1 type, dummy_field_2 type2);
CREATE TABLE dummy_table (dummy_field_1 type, dummy_field_2 type2, INDEX (field));
CREATE TABLE dummy_table (dummy_field_1 type, dummy_field_2 type2, PRIMARY KEY (dummy_field_1));
CREATE TABLE dummy_table (dummy_field_1 type, dummy_field_2 type2, PRIMARY KEY (field1,dummy_field_2));

-- Create with foreign keys --
CREATE TABLE dummy_table (fk1 type, field2 type2, 
    FOREIGN KEY (fk1) REFERENCES dummy_table_2 (t2_fieldA))
    [ON UPDATE or ON DELETE] [CASCADE or SET NULL]

-- Delete / Drop -- 
DROP TABLE table;
DROP TABLE IF EXISTS table;
DROP TABLE dummy_table, dummy_table_2

-- Alter / Update --
ALTER TABLE table MODIFY dummy_field type
ALTER TABLE table MODIFY dummy_field type NOT NULL ...
ALTER TABLE table CHANGE old_name_dummy_field new_name_dummy_field type
ALTER TABLE table CHANGE old_name_dummy_field new_name_dummy_field type NOT NULL ...
ALTER TABLE table ALTER dummy_field SET DEFAULT ...
ALTER TABLE table ALTER dummy_field DROP DEFAULT
ALTER TABLE table ADD new_name_dummy_field type
ALTER TABLE table ADD new_name_dummy_field type FIRST
ALTER TABLE table ADD new_name_dummy_field type AFTER another_field
ALTER TABLE table DROP dummy_field
ALTER TABLE table ADD INDEX (field);

-- Insert --
INSERT INTO dummy_table (field1, field2) VALUES (value1, value2);
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