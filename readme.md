# SQL Cheat sheet

### Relational database management system

A relational database management system (RDBMS) is a software layer of tools and services that manages relational tables. In practice, the terms RDBMS and relational database are considered to be synonyms. A relational database provides a consistent interface between applications, users, and relational database. 
#### RDBMS Benefits
- Structured Data: RDBMS allows data storage in a structured way, using rows and columns in tables. This makes it easy to manipulate the data using SQL (Structured Query Language), ensuring efficient and flexible usage.

- ACID Properties: ACID stands for Atomicity, Consistency, Isolation, and Durability. These properties ensure reliable and safe data manipulation in a RDBMS, making it suitable for mission-critical applications.

- Normalization: RDBMS supports data normalization, a process that organizes data in a way that reduces data redundancy and improves data integrity.

- Scalability: RDBMSs generally provide good scalability options, allowing for the addition of more storage or computational resources as the data and workload grow.

- Data Integrity: RDBMS provides mechanisms like constraints, primary keys, and foreign keys to enforce data integrity and consistency, ensuring that the data is accurate and reliable.

- Security: RDBMSs offer various security features such as user authentication, access control, and data encryption to protect sensitive data.

#### limitations of using an RDBMS:

- Complexity: Setting up and managing an RDBMS can be complex, especially for large applications. It requires technical knowledge and skills to manage, tune, and optimize the database.

- Cost: RDBMSs can be expensive, both in terms of licensing fees and the computational and storage resources they require.

- Fixed Schema: RDBMS follows a rigid schema for data organization, which means any changes to the schema can be time-consuming and complicated.

- Handling of Unstructured Data: RDBMSs are not suitable for handling unstructured data like multimedia files, social media posts, and sensor data, as their relational structure is optimized for structured data.

- Horizontal Scalability: RDBMSs are not as easily horizontally scalable as NoSQL databases. Scaling horizontally, which involves adding more machines to the system, can be challenging in terms of cost and complexity.

## Overview of commands
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
-- Primary Keys --
The PRIMARY KEY constraint uniquely identifies each record in a table.
Primary keys must contain UNIQUE values, and cannot contain NULL values.

-- Foreign Keys --
The FOREIGN KEY constraint is used to prevent actions that would destroy links between tables.

A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the PRIMARY KEY in another table.
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
-- SQL field data types --  
More info https://www.w3schools.com/sql/sql_datatypes.asp
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
-- Triggers --
Triggers can be set up in RDMS as a sort of automation, when one thing happens it can can 'trigger' an action elsewhere in the db.

more info;
https://www.datacamp.com/tutorial/sql-triggers
```
```
-- Notes --
LIKE - Case sensitive
ILIKE - Not case sensitive
```