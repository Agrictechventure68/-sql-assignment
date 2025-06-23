SQL Assignment: Data Manipulation and Transactions

This repository contains my completed assignment on basic SQL operations using MySQL. The goal was to demonstrate essential database skills such as creating tables, inserting records, updating data, and querying results.


🎯 Learning Objectives

- Create tables and define a database structure
- Insert records into a table
- Update existing records
- Execute basic SQL queries using MySQL Workbench


 📁 Project Structure

sql-assignment/
│
├── answers.sql # Contains all the SQL commands used
├── README.md # This documentation file


 📝 Assignment Questions and Answers

🔹 Question 1: Create the `student` Table

*TASK:  
Write an SQL statement to create a table named `student` with the following columns:
- `id` (an integer, primary key)
- `fullName` (text, max 100 characters)
- `age` (integer)

*Answer:
```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    fullName VARCHAR(100),
    age INT
);
📘 This creates a table to store unique students using id as the primary identifier.

🔹 Question 2: Insert Records into student
Task:
Insert at least 3 student records into the table.

Answer:
INSERT INTO student (id, fullName, age) VALUES
(1, 'Ada Lovelace', 21),
(2, 'Chinua Achebe', 19),
(3, 'Grace Hopper', 23);
📘 These records populate the student table with sample data.

🔹 Question 3: Update a Student's Age
Task:
Update the age of the student with id = 2 to 20.

Answer:
UPDATE student
SET age = 20
WHERE id = 2;
📘 This command targets a specific student and updates the age field.

🔹 Bonus: View the Data
To verify that data was correctly inserted and updated:

SELECT * FROM student;
📘 This query fetches all rows from the student table.

💻 TOOLS USED
* MySQL Workbench 8.0.39
* Visual Studio Code
* Git and GitHub

✅ Result
All tasks were successfully executed and validated using the result grid in MySQL Workbench. The final dataset includes 3 students, with correct updates applied.

📌 Author
Bright Doro
Passionate about data, agriculture, and building smart tech solutions.
