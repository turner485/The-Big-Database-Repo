## SQL vs NoSQL Databases
### Structured Query Language (SQL)
#### What is SQL?
SQL, which stands for Structured Query Language, is a domain-specific programming language (e.g., a language targeted to a specific task or problem) that is commonly used for tasks such as inserting, updating, querying, and deleting data within a database. SQL is also used to create and modify database schemas (e.g., data formatting rules, table/index structure ) as well as define database access and administration parameters.

#### What is structured data?
Structured data is data that is organized in a consistent, predefined format and often consists of alphanumeric characters. Examples include financial transactions, inventory records, or customer lists which are often stored in SQL databases (e.g., relational databases).

#### What is a SQL database?
When the term "SQL database" is used, it refers to a type of database where SQL is the primary programming language used to create and manage that database. SQL application programming interfaces (APIs) contain groups of functions that enable developers to execute and manage database operations without having to create individual SQL commands over and over.

Regardless of whether a SQL database is used to store transactions for a retailer or financial information for a corporation, SQL databases fall under a type of database referred to as relational databases.

#### Relational databases
Relational databases, or relational database management systems (RDBMSs), store data within rows and columns which are used to form tables. A relationship between the two tables (or more) can be created using a foreign key. These foreign keys (e.g., unique identifiers) maintain predefined relationships that exist between the tables.

#### Vertical Scaling 
The vertical scaling approach, sometimes referred to as "scaling up," focuses on adding more resources or more processing power to a single machine. These additions may include CPU and RAM resources upgrades which will increase the processing speed of a single server or increase the storage capacity of a single machine to address increasing data requirements.

One of the advantages of scaling vertically is that it is easier than the alternative horizontal scaling approach. Specifically, since hardware resources and/or computing resources are only being added to one machine, there is less complexity involved. 

### Not only Structured Query Language (NoSQL)
#### What is NoSQL?
NoSQL, which stands for Not only SQL, is a database management system approach used to ingest, store, and retrieve unstructured data and semi-structured data within a database. This means that data that cannot be analyzed or counted through traditional relational databases (e.g., SQL) can remain in its native format and be ingested into a NoSQL database. The reason it is called NoSQL is to emphasize that these databases can handle non-tabular, non-relational data models as well as support SQL-like query languages.

#### What is unstructured data?
Unstructured data is data that doesn't have a predefined data model or consistent organization. In addition, unstructured data, such as social media posts, can update and change rapidly while structured data, such as bank transactions, have a much lower rate of change. Examples of unstructured data include pictures, audio files, videos, and maps.

#### What is a NoSQL database?
NoSQL databases are databases that utilize a flexible schema that accommodates unstructured data and semi-structured data while also utilizing a non-tabular data storage method.

The use of a flexible schema enables NoSQL databases to ingest unstructured data in its native format (e.g., .txt, .JPG, MP3), which is not possible with SQL databases due to the requirement that all data align to a predefined format. Further, when NoSQL databases store data, flexible data models are employed so that unstructured data files can have different data structures and still be stored within the same 
collection

#### Horizontal Scaling
the horizontal scaling approach, sometimes referred to as "scaling out," entails adding more machines to further distribute the load of the database and increase overall storage and/or processing power. There are two common ways to perform horizontal scaling — they include sharding, which increases the overall capacity of the system, and replication, which increases the availability and reliability of the system.

Read more from the resource;  
[https://www.mongodb.com/resources/basics/databases/nosql-explained/nosql-vs-sql](https://www.mongodb.com/resources/basics/databases/nosql-explained/nosql-vs-sql)  
Watch youtube video  
[https://www.youtube.com/watch?v=_Ss42Vb1SU4](https://www.youtube.com/watch?v=_Ss42Vb1SU4)