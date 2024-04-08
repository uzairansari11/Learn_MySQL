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
