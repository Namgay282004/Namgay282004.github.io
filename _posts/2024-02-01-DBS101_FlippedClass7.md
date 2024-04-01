---
Title: DBS101 Flipped Class6
categories: [DBS101, Flipped_Class6]
tags: [DBS101]
---
## Topic: Creating a database from scratch

A database is an organized collection of structured data that is stored and can be accessed. It is made so that large amounts of data can be retrieved,inserted, or deleted.

### Main components of database
The main components of a database are:
- Tables: A table is a collection of related data organized into rows and columns.Tables are used to store data in a relational database.
- Fields: Fields are the individual pieces of data within a table. Each field contains a specific data type, such as a text string, numeric value, or date.
- Records: Records are individual rows in a table that contain related data. Each record corresponds to a single item or instance of data, such as a specific customer,
product, or transaction.
- Primary Key: The primary Key is a key that helps in uniquely identifying the tuple of the database. In other words, it tells the database, “hey, here I am!”
- Foreign Key: Foreign Key is a key that is used to identify the relationship between the tables through the primary key of one table, that is, the primary key of one table
acts as a foreign key to another table.
- Queries: A query is a request for data from a database. Queries are used to search and retrieve specific data from a database.
- Indexes: An index is a database structure that helps to speed up query performance by allowing the database to locate specific records quickly.
- Views: A view is a virtual table based on a query’s result. Views provide a way to
present a subset of data from a database in a specific format.

![alt text](../Images_for_DBS101/Float-vs.-Decimal-data-types-in-SQL-Server.jpg)

### How to create our own database?
- Determine the purpose and requirements of the database: What kind of data will
be stored, the relationships between the data, who will use the database, and what
kind of queries will be performed on the data.
- Choose a database management system (DBMS) that fits the requirements.
Examples of DBMS include MySQL, PostgreSQL, etc..
- Create a list of entities and a list of attributes: Create a visual representation of the
database structure, including tables, columns, data types, and relationships
between tables.
- Implement the database schema: Create tables and columns of a chosen DBMS,
and specify constraints such as primary keys and foreign keys.
- Populate the database with data: Add data to the tables and verify that it meets the
constraints.
- Test the database: Perform queries on the data to ensure that it can be retrieved,
deleted, or inserted as required.
- Maintain the database: Regularly back up the data, monitor performance, and
make updates as needed to ensure that the database continues to meet the needs
of its users.

![alt text](../Images_for_DBS101/Database-Development-SDLC.jpg)

### Some popular DBMS for database development include:
- MySQL: a widely used open-source relational database management system.
- PostgreSQL: a powerful and open-source object-relational database management
system.
- MongoDB: a document-oriented NoSQL database management system known for its
scalability and ease of use.

### Data Structures for implementing a relational database
1. B-trees: The B-tree module is a fundamental data structure used in chidb for
storing and retrieving data efficiently.
2. Database Machine (DBM): The DBM is a virtual machine designed to operate on
chidb files. It includes a set of instructions (low-level and high-level) for
manipulating the database.
3. SQL Compiler: The SQL compiler is responsible for translating SQL queries into
DBM programs
4. Hash Tables: For quick lookups of records based on keys.
5. API: The API provides a set of functions for interacting with the chidb system. It
includes functions for opening and closing database files, executing SQL
statements, and accessing query results.
6. Linked Lists: For managing records within a table or for maintaining a list of pages
in a B-tree
7. Shell: The shell provides a command-line interface for interacting with the chidb
system. It allows users to run SQL statements, DBM programs, and provides
utilities for parsing SQL and displaying the syntax tree and DBM program.
8. Arrays: For storing data in a structured format, such as the values in a table row.