SQL Commands Explanation:

1. SHOW DATABASES;
   - This command lists all the databases available in the database management system.

2. USE advance_queries;
   - This command selects the "advance_queries" database for further operations.

3. SHOW TABLES;
   - After selecting the database, this command lists all the tables present in the selected database.

4. CREATE TABLE employee_table (
      id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
      name VARCHAR(50) NOT NULL,
      occupation VARCHAR(35) NOT NULL,
      age INT NOT NULL
   );
   - This command creates a new table named "employee_table" with columns: id, name, occupation, and age.
   - The id column is set as the primary key with auto-increment, ensuring each record gets a unique identifier.

5. SHOW TABLES;
   - After creating the table, this command lists all the tables present in the database to verify the creation of "employee_table".

6. DESCRIBE employee_table;
   - This command displays the structure of the "employee_table", showing details such as column names, data types, and constraints.

7. ALTER TABLE employee_table ADD COLUMN salary INT NOT NULL DEFAULT 25000 AFTER occupation;
   - This command adds a new column named "salary" to the "employee_table".
   - The salary column is of type INT, not allowing NULL values, and the default value is set to 25000.
   - It is positioned after the "occupation" column in the table.

8. ALTER TABLE employee_table ADD COLUMN dob DATE NOT NULL AFTER name, ADD COLUMN married BOOL NOT NULL DEFAULT 0;
   - This command adds two new columns, "dob" (date of birth) and "married", to the "employee_table".
   - The "dob" column is of type DATE, not allowing NULL values, and is positioned after the "name" column.
   - The "married" column is of type BOOL (boolean), not allowing NULL values, with a default value of 0 (false).

9. ALTER TABLE employee_table MODIFY salary INT NOT NULL;
   - This command modifies the "salary" column in the "employee_table", ensuring it cannot contain NULL values.

10. ALTER TABLE employee_table CHANGE salary employee_salary INT NOT NULL;
   - This command changes the name of the column "salary" to "employee_salary" in the "employee_table".
   - It also modifies the data type of the column to INT and ensures it cannot contain NULL values.

11. ALTER TABLE employee_table DROP COLUMN dob;
    - This command removes the "dob" column from the "employee_table".

This file contains a sequence of SQL commands demonstrating the creation, alteration, and deletion of columns in the "employee_table" within the "advance_queries" database.
# SQL Commands Explanation

This README file provides explanations for a series of SQL commands executed in a database environment.

## Database Operations

- `SHOW DATABASES;`: Displays the list of databases available in the database server.
- `USE advance_queries;`: Switches to the database named "advance_queries".
- `SHOW TABLES;`: Lists all tables in the current database.

## Creation and Alteration of Tables

- `CREATE TABLE employee_table ...`: Creates a table named "employee_table" with columns for ID, name, occupation, age, salary, and marital status.
- `DESCRIBE employee_table;`: Shows the structure of the "employee_table" table.
- `ALTER TABLE employee_table ...`: Modifies the structure of the "employee_table" by adding and renaming columns.
- `ALTER TABLE employee_table DROP COLUMN dob;`: Removes the "dob" column from the "employee_table".
- `ALTER TABLE employee ...`: Modifies the "employee" table by changing the data type of the "age" column and adding a check constraint for age between 18 and 70.

## Data Manipulation and Views

- `INSERT INTO employee ...`: Inserts records into the "employee" table.
- `CREATE TABLE dummy_employee LIKE employee;`: Creates a new table "dummy_employee" with the same structure as "employee".
- `INSERT INTO dummy_employee SELECT * FROM employee;`: Copies data from "employee" to "dummy_employee".
- `DROP TABLE dummy_employee;`: Deletes the "dummy_employee" table.
- `CREATE VIEW view1 AS SELECT ...`: Creates a view "view1" based on the "dummy_employee" table.

## Foreign Keys and Relationships

- `CREATE TABLE hobbies ...`: Defines a table "hobbies" with a foreign key referencing the "employee" table.
- `DESCRIBE hobbies;`: Displays the structure of the "hobbies" table.

## More Table Operations

- `CREATE TABLE Person ...`: Creates a table "Person" with columns for ID, name, email, and city.
- `DROP TABLE Person;`: Drops the "Person" table.
- `INSERT INTO Person ...`: Inserts records into the "Person" table.
- `REPLACE INTO PERSON ...`: Replaces or inserts records into the "Person" table.
- `INSERT IGNORE INTO Person ...`: Inserts records into the "Person" table, ignoring duplicates.
- `CREATE TABLE person_info ...`: Creates a table "person_info" to store information from the "Person" table.
- `INSERT INTO person_info ...`: Inserts data from the "Person" table into the "person_info" table.

## Retrieval Queries

- `SELECT * FROM person_info;`: Retrieves all records from the "person_info" table.

This README summarizes the SQL commands and their purposes in setting up tables, manipulating data, and querying information in the database environment.
