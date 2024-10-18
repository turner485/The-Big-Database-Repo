# Data Definition Language (DDL) 
- Data Definition Language (DDL) is a group of SQL statements that you can execute to manage database objects, including tables, views, and more. 
- Using DDL statements, you can perform powerful commands in your database such as creating, modifying, and dropping objects. 
- DDL commands are usually executed in a SQL browser or stored procedure.
- DDL is contrasted with Data Manipulation Language (DML) which is the SQL that is used to actually access and manipulate data in database objects.
- The majority of data analysts will rarely execute DDL commands and will do the majority of their work creating DML statements to model and analyze data.
### Types of DDL Statements
- DDL statements are used to create, drop, and manipulate objects in your database. They are often, but not always, unforgiving and irreversible.
- Important - The syntax for DDL commands can be pretty database-specific.

`ALTER`  
- Using the ALTER DDL command, you can change an object in your database that already exists. By "change", we specifically mean you can:
- Add new, remove, and rename columns to views and tables  
- Rename a view or table
- Modify the structure of a view or table

```
-- Table Column Example --
ALTER TABLE customers rename column last_name as last_initial;
```

`DROP`
- The DROP command. Probably the most high-stakes DDL statement one can execute. 
- One that should be used with the utmost of care. At its core, an executed DROP statement will remove that object from the database. 
- You can drop tables, views, schemas, databases, users, functions, and more.
```
-- Example drop table -- 
DROP TABLE customers;
```
`CREATE`
- With the CREATE statement, you can create new objects in your database. The most common objects created with this statement are tables, schemas, views, and functions. 
- Unlike DROP, ALTER, and TRUNCATE commands, there’s little risk with running CREATE statements since you can always drop what you create.
- Creating tables and views with the CREATE command requires a strong understanding of how you want the data structured, including column name and data type. 
- Using the CREATE command to establish tables and views can be laborious and repetitive, especially if the schema objects contain many columns, but is an effective way to create new objects in a database. 
- After you create a table, you can use DML INSERT statements and/or a transformation tool such as dbt to actually get data in it.
```
-- Example table create --
CREATE TABLE prod.jaffle_shop.jaffles (
	id varchar(255),
	jaffle_name varchar(255)
	created_at timestamp,
	ingredients_list varchar(255),
	is_active boolean
);
```
`TRUNCATE`  
- The TRUNCATE command will remove all rows from a table while maintaining the underlying table structure. 
- The TRUNCATE command is only applicable for table objects in a database. 
- Unlike DROP statements, TRUNCATE statements don’t remove the actual table from the database, just the data stored in them.
```
-- Example truncate --
TRUNCATE TABLE payments;
```

more information from resource here;  
https://www.getdbt.com/blog/guide-to-ddl