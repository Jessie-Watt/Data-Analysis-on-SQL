# Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL.

# **INTRODUCTION**
In today's world data is widely used by different organizations to take decisions to aid improvemnt in work efficiency, research and many others facets. Structured Query Language(SQL) is a standardized programming language used to manage relatinal database. SQL will be used in this task to create three tables containing student's information, their health records and their performance.

# **ACTIVITY**
1. The creation of database names 'Students Record'.
2. The use creation of three tables in the Students Record Database
     a) Students Information (Student ID, Gender, Name, Age, Subject)
     b) Health Records (Students ID, Blood Group, Health, Weight)
     c) Performance(Student ID, Score, Grade)
4. Making the 'Student ID' column for the three tables to be unique 
5. Where a student that has no score, it should be '(0)' by default.
6. Adding a constraint that prevents the Student ID and subject from taking null values.
7. The droping of columns using constraint
8. The changing of column name from 'subject' to course

# **SKILL DEMONSTRATED**
Creating a new database
The use of operational keys
Creating tables and inserting values in the rows
Applying Constraint

# SOLUTIONS
A new database named 'Students Record' was created on the SQL server management by cliking on 'New Query', this activated a work interface where I wrote the code 'CREATE DATABASE STUDENTS_RECORD;' then executed the code, this developed a database accessed on the left-handside of the work interface. 

![Students Info](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/4c97c102-ab9d-458e-9bf1-f6ed374a741d)


In the students records database, the students_info table was formulated with operational keywords such as 'create', 'table' with the titles of all the column headers inserted in a bracket followed by a semicolon. All column titles were followed by a constraint to help enforce rules to prevent invalid data. This syntax; **CREATE TABLE _table_name(column1 datatype constrainst,...)_** was used to create the students_info table. The constraint 'INT' when an interger is involved, the 'PRIMARY KEY' Constraint is attached when a column is made to be unique, and 'NOT NULL' to prevent a particular column from taking values. The NOT NULL', PRIMARY KEY", and the INT"< constraints were all added to the 'student ID' column and the subject column to enforce thier rules. Values were inserted into the rows of the newly created columns using the 'Insert Into' and 'Values' keywords as seen in the screenshot above. The 'Age' column from students_info table was dropped by the use of syntax; **ALTER TABLE __table_name_ _DROP COLUMN __column_name_;**. This can be viewed on the screenshot below


![STUDENT INFO 2](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/9bb5c574-91cf-49a9-a5e6-494a74165ef8)

The health records and the performance tables were also created using the same syntax; **CREATE TABLE _table_name(column1 datatype constrainst,...)_**. The Students ID column was unique for both tables. Each column title of the health record table was given its specific constraint as;_ _**CREATE TABLE_ _HEALTH_RECORDS (STUDENT_ID INT PRIMARY KEY NOT NULL, BLOOD_GROUP VARCHAR(10), WEIGHT INT);_**. Values were inserted into the rows of the column as seen from the screenshot below, then_**SELECT * FROM HEALTH_RECORDS;_** was highlighted and the 'execute' button was clicked.

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/bef1990f-20ef-462b-bdcd-8e0a74abff8e)

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/0f19b192-5d51-411a-9838-ed58d4d08d90)
 
The column titled 'subject' in the Students_info table was change to 'course' using the this syntax _**EXEC sp_rename'STUDENTS_INFO.SUBJECT', 'COURSE', 'COLUMN';**__ see the screenshot below.

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/754acb72-71a7-430b-bb1d-8473252aefbf)

# CONCLUSION
This task has gradually exposed me to the use of SQL and its function. I look to learn more.      
