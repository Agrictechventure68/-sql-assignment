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

week 5 Assignment Questions and Answers

 🔹 Question 1: Create the `student` Table

*TASK:  
Create a table named `student` with the following:
- A unique ID for each student
- `name` (string, max 100 chars, required)
- `age` (integer, default = 18)
- `gender` (string, max 10 chars, default = 'Unknown')

*Answer:
```sql
CREATE TABLE student (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT DEFAULT 18,
    gender VARCHAR(10) DEFAULT 'Unknown'
);
📘 This structure ensures data integrity, readability, and flexibility.

🔹 Question 2: Create an Index on age
TASK:
Add an index named IdxAge to optimize queries filtering by age.

Answer:
CREATE INDEX IdxAge ON student(age);

📌 Author
Bright Doro
Passionate about data, agriculture, and building smart tech solutions.

COMBINING WEEK 3-7 SOLUTIONS TO SHOW MASTERING.
 SQL Techniques Demonstrated

✅ Table Creation with Constraints
CREATE TABLE student (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT DEFAULT 18,
    gender VARCHAR(10) DEFAULT 'Unknown'
);
 INSERT:
INSERT INTO student (name, age, gender) VALUES
('Ada Lovelace', 21, 'Female'),
('Chinua Achebe', 20, 'Male');

DELETE:
DELETE FROM spending WHERE amount < 10;

ALTER:
ALTER TABLE spending ADD description VARCHAR(100);

TRANSACTION:
START TRANSACTION;
UPDATE student SET age = age + 1 WHERE student_id = 1;
DELETE FROM spending WHERE student_id = 3;
COMMIT;

Grouping & Summarization

Total Spending by Category:
SELECT category, SUM(amount) AS total_spent
FROM spending
GROUP BY category;

Spending by Student and Category:
SELECT s.name, sp.category, SUM(sp.amount) AS total_spent
FROM spending sp
JOIN student s ON s.student_id = sp.student_id
GROUP BY s.name, sp.category;

Hobbies Table (4NF):
CREATE TABLE student_hobbies (
    hobby_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    hobby VARCHAR(50),
    FOREIGN KEY (student_id) REFERENCES student(student_id)
);

Courses and Enrollment Tables (3NF):
CREATE TABLE course (
    course_id INT AUTO_INCREMENT PRIMARY KEY,
    course_name VARCHAR(100)
);

CREATE TABLE enrollment (
    enrollment_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    course_id INT,
    FOREIGN KEY (student_id) REFERENCES student(student_id),
    FOREIGN KEY (course_id) REFERENCES course(course_id)
);

Repsql-assignment/
├── student_spending_normalization.sql
├── README.mdository Structure:

👨‍💻 Author

Bright DoroAgritech Solution Builder | Data Enthusiast | Smart Farming Advocate





