# Introduction to Database Management Systems (DBMS) and SQL

## Database

A database is a collection of data organized in a digital format that can be easily accessed.

## DBMS (Database Management System)

DBMS is an application used for managing databases.

## SQL (Structured Query Language)

SQL is a programming language designed for managing relational databases.

## Operations (CRUD)

CRUD stands for Create, Read, Update, Delete.

## MySQL

MySQL is a popular relational database management system.

## Commands and SQL Statements

### Database Operations

- Create a database: `CREATE DATABASE database_name;`
  Example: `CREATE DATABASE my_database;`
- Drop a database: `DROP DATABASE database_name;`
  Example: `DROP DATABASE my_database;`
- Use a particular database: `USE database_name;`
  Example: `USE my_database;`

### Table Operations

- Create a table:
  ```sql
  CREATE TABLE table_name(
      id INT PRIMARY KEY,
      name VARCHAR(255),
      email VARCHAR(255),
      password VARCHAR(255)
  );
  ```
  Example:
  ```sql
  CREATE TABLE users(
      id INT PRIMARY KEY,
      name VARCHAR(255),
      email VARCHAR(255),
      password VARCHAR(255)
  );
  ```
- Insert values into a table:
  ```sql
  INSERT INTO table_name VALUES (1,"john","john123@gmail.com","john@123");
  ```
  Example:
  ```sql
  INSERT INTO users VALUES (1, "John Doe", "john@example.com", "password123");
  ```
- Select everything from a table: `SELECT * FROM table_name;`
  Example: `SELECT * FROM users;`

### Additional Commands

- Check before creating a database (good practice): `CREATE DATABASE IF NOT EXISTS database_name;`
  Example: `CREATE DATABASE IF NOT EXISTS my_database;`
- Show all databases: `SHOW DATABASES;`
  Example: `SHOW DATABASES;`
- Show all tables for a given database: `SHOW TABLES;`
  Example: `SHOW TABLES;`

### Constraints and Checks

- Define foreign key:
  ```sql
  FOREIGN KEY (column_name) REFERENCES table_name (column_name)
  ```
- Setting default value for a column:
  ```sql
  column_name datatype DEFAULT value;
  ```
- Check constraint examples:
  ```sql
  CREATE TABLE city (
      id INT PRIMARY KEY,
      age INT NOT NULL,
      city VARCHAR(40),
      CONSTRAINT age_check CHECK (age >= 18 AND city = "mumbai")
  );
  CREATE TABLE new1 (
      id INT PRIMARY KEY,
      city VARCHAR(40),
      age INT NOT NULL CHECK (age >= 18 AND city = "mumbai")
  );
  ```

### WHERE Clauses and Operators

- `AND`, `OR`, `BETWEEN`, `IN`, `NOT`, `LIMIT`, etc.
- Examples provided in SQL syntax.

### Aggregate Functions

- `COUNT`, `MIN`, `MAX`, `SUM`, `AVG`, etc.
- Examples provided.

### Group By and Having Clause

- Grouping and applying conditions.
- Example provided in SQL syntax.

### UPDATE Section

- Updating records in a table.
- Example provided in SQL syntax.

### Adding Foreign Keys to a Table

- Example provided with SQL syntax.

### Table Related Queries

- Description provided.
