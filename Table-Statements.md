# Table Specific SQL Statements
Create, Drop, Alter & Truncate

### The SQL CREATE TABLE Statement
The SQL CREATE TABLE statement is used to create a database table. We use this table to store records (data).

Now remember the data types we spoke about [here](./Data-Types.md).  
We are using them below to define our table columns.

```
-- Example --
CREATE TABLE Companies (
  id int,
  name varchar(50),
  address text,
  email varchar(50),
  phone varchar(10)
);
```

### The SQL DROP TABLE Statement
DROP TABLE is a SQL statement that permanently deletes a table and all its data from a database.
```
-- Example -- 
DROP TABLE table_name;
```
It’s important to note that the DROP TABLE statement is a powerful command that can have serious consequences if misused. Therefore, it should be used with caution and only when you are sure that you want to delete the table and all its data.

### The SQL TRUNCATE TABLE Statement
The SQL TRUNCATE TABLE command is used to empty a table. This command is a sequence of DROP TABLE and CREATE TABLE statements and requires the DROP privilege.  

You can also use DROP TABLE command to delete a table but it will remove the complete table structure from the database and you would need to re-create this table once again if you wish you store some data again.

```
-- Example -- 
TRUNCATE TABLE table_name;
```

You can read up on the TRUNCATE vs DELETE here;  
https://www.tutorialspoint.com/sql/sql-truncate-table.htm

### The SQL ALTER TABLE Statement
The SQL ALTER TABLE statement is used to add, modify, or drop/delete columns in a table. The SQL ALTER TABLE statement is also used to rename a table.

Add Column in table
```
-- Example add column --
ALTER TABLE supplier
    ADD supplier_name char(50);
-- Example add multiple --
ALTER TABLE supplier
    ADD (supplier_name char(50),
        city char(45)
        );
```
Modify column in table
```
-- Example Modify Column -- 
ALTER TABLE supplier
  MODIFY supplier_name VARCHAR(100) NOT NULL;
-- Example Modify Multiple --
ALTER TABLE supplier
  MODIFY supplier_name VARCHAR(100) NOT NULL,
  MODIFY city VARCHAR(75);
```
Drop Column in table
```
-- Example Drop Column --
ALTER TABLE supplier
  DROP COLUMN supplier_name;
```
Rename Column in table
```
sp_rename 'supplier.supplier_name', 'sname', 'COLUMN';
```
Rename table 
```
sp_rename 'supplier', 'vendor';
```

These examples seen in the alter section are SQL server.  
for more info resource here;  
https://www.techonthenet.com/sql/tables/alter_table.php
