# **DATA ANALYSIS USING SQL SERVER AND ITS FUNCTIONS**


 
# **INTRODUCTION**
In today's world data is widely used by different organizations to take decisions to aid improvemnt in work efficiency, research and many others facets. Structured Query Language(SQL) is a standardized programming language used to manage relational database. On my first task SQL will be used to create three tables containing student's information, their health records and their performance. SQL advanced operators and clauses will also be used to retrieve, sort and filter datasets of employees in the second task, the last task will require the use of aggregate functions to perform calculations on sets of rows and return results.

# **TASK 1 - ANALYSIS ON STUDENTS HEALTH RECORDS AND PERFORMANCE**

# **ACTIVITY**
1. The creation of database 'Students Record'
2. The use creation of three tables in the Students Record Database;
     a) Students Information (Student ID, Gender, Name, Age, Subject
     b) Health Records (Students ID, Blood Group, Health, Weight)
     c) Performance (Student ID, Score, Grade)
4. Making the 'Student ID' column for the three tables to be unique 
5. Where a student that has no score, it should be '0' by default.
6. Adding a constraint that prevents the Student ID and subject from taking null values.
7. The dropping of columns using constraint
8. The changing of column name from 'subject' to 'course'

# **SKILL DEMONSTRATED**

1). Creating a new database 
2). The use of operational keywords 
3). Creating tables and inserting values in the rows 
4). Applying Constraint

# SOLUTION 1
A new database named 'Students Record' was created on the SQL server management by cliking on 'New Query', this activated a work interface where I wrote the code 'CREATE DATABASE STUDENTS_RECORD;' then executed the code, this developed a database accessed on the left-handside of the work interface. 

![Students Info](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/4c97c102-ab9d-458e-9bf1-f6ed374a741d)


In the students records database, the 'students_info' table was formulated with operational keywords such as 'create table' with the titles of all the column headers inserted in a bracket followed by a semicolon. All column titles were followed by a constraint to help enforce rules to prevent invalid data. This syntax; **CREATE TABLE _table_name(column1 datatype constrainst,...)_** was used to create the students_info table. The following constraint 'INT', was used when an interger is involved, the 'PRIMARY KEY' Constraint is attached when a column is made to be unique, and 'NOT NULL' to prevent a particular column from taking values. The 'NOT NULL', 'PRIMARY KEY", and the 'INT' constraints was added to the 'student ID' column to enforce the unique rule. Values were inserted into the rows of the newly created columns using the 'Insert Into' and 'Values' keywords as seen in the screenshot above. The 'Age' column from students_info table was dropped by the use of syntax; **ALTER TABLE __table_name_ _DROP COLUMN __column_name_;**. This can be viewed on the screenshot below 


![STUDENT INFO 2](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/9bb5c574-91cf-49a9-a5e6-494a74165ef8)

The health records and the performance tables were also created using the same syntax; **CREATE TABLE _table_name(column1 datatype constrainst,...)_**. The Students ID column was unique for both tables. Each column title of the health record table was given its specific constraint as;_ _ **CREATE TABLE_ _HEALTH_RECORDS (STUDENT_ID INT PRIMARY KEY NOT NULL, BLOOD_GROUP VARCHAR(10), WEIGHT INT);_**. Values were inserted into the rows of the column as seen from the screenshot below, then_**SELECT * FROM HEALTH_RECORDS;_** was highlighted and the 'execute' button was clicked.

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/bef1990f-20ef-462b-bdcd-8e0a74abff8e)

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/0f19b192-5d51-411a-9838-ed58d4d08d90)
 
The column titled 'subject' in the Students_info table was change to 'course' using the this syntax _**EXEC sp_rename'STUDENTS_INFO.SUBJECT', 'COURSE', 'COLUMN';**__ see the screenshot below.

![image](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/754acb72-71a7-430b-bb1d-8473252aefbf)





# **TASK 2 - ANALYSIS ON JESSICA'S COMPANY EMPLOYEE DETAILS AND THEIR SALARY SCALE MANAGEMENT DATA

# **ACTIVITY**
1. Select the employees table and show the data where city is Mumbai and Delhi.
2. Select the employee table where employee first name have both 'a' and 'e' in them.
3. Subset the employee table to have employee with date of birth above 1990.
4. Subset the salary table to show salaries less than one million and sort in an ascending order.
5. Modify email column of the employee table to contain just email without '@gmail.com '


# **SKILLS DEMONSTRATED**
1). Filtering my dataset using specified conditions
2). Retrieving data using operational keywords
3). Sorting retrieved values using clauses in specified orders

# TASK 2 SOLUTION
The Employee and Salary dataset was provided by my coach Victor Somadina, this was imported into my 'Business' SQL server management by right-cliking on database, point to tasks then I click Import Flat File. The two dataset was located in the tables section. A screenshot of the rawdataset can be seen below 

![Employee Raw Dataset](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/d093502a-6031-4f23-8714-5e5442cf5434)

![Salary Raw Dataset](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/08952810-10f7-4cb5-90f0-353d258bb4dd)

In my first activity the employee table will be filtered to show staff who are based in Mumbai and Delhi cities. This was achieved by using the 'WHERE' clause, this filtered the data providing only the rows with Mumbai and Delhi as city. I also introduced the 'Like' operator to evaluate my condition. The syntax used is;   syntax: **SELECT _column1, column2,_ ... FROM _table_name_ WHERE _condition;**. 

![Mumbai and Delhi Cities](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/0f9c8e4a-d2d3-47d5-8a7f-bcc6829aac3c)

To determine form the employee table where employee first name have both 'a' and 'e' in them. To evaluate this I used the 'WHERE' condition and the percentage(%) operator to return the pattern. **SELECT * FROM EMPLOYEE WHERE NAME LIKE '%[AE]%';**

![Firstname with A and E](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/a2c905db-467a-4349-bfe3-1f35c50b554a)

To retrive the data of employees whose date of birth is above 1990, the 'WHERE' clause and the camparison operators was used; **SELECT * FROM EMPLOYEE WHERE date_of_birth >= '1990';**

![Employee DOB above 1990](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/ecf91146-23dc-4d66-97b3-69e0bd91dd5f)

Subset the salary table to show salaries less than one million and sort in an ascending order. To retrive the data of employees whose salary scale is less than one million, the 'WHERE', 'ORDER BY' and comparison operator were used.

![EMP  less than 1million](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/b743f2c9-3cdc-4fae-9f7f-9643dbd0b213)

# **TASK 3 - CONTINUATION OF TASK 2**

# **ACTIVITY**
1. What is the total number of employees in our employee table.
2. To find out the top 5 cities with the highest number of employees, the filter the result to show cities with more    
    than 15 employess.
3. To find out the most used pin code by the employee. In this case, we want toknow the pin codes that is used the most


# **SKILLS DEMONSTRATED**
1). The use of Aggregate functions

# **TASK 3 SOLUTION**

The total number of employees, in the employee table was calulated using the 'count' function. The syntax applied is     **_ SELECT COUNT(*) FROM _table_name__**. The result can be seen in the screenshot below.

![Total Employee](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/05f9ec6f-dec7-4163-980c-cbf2486dd857)


The top five(5) cities with highest number of employees. The 'TOP N' clause is used to limit the number of rows that apppear in a query. the syntax used was  syntax: **SELECT TOP N _column1, column2_, ... FROM _table_name_**. The aggregate functio 'count' was used to count the cities and filter a new colmun renmaining it as 'Total Employee', which was later 'grouped by' 'city' to return the result in 'city' and 'total employee' columns. The 'total employee' column was 'order by' to be in a descending order. The 'having' clause was used to filter the result of a 'group by' clause 

![The top 5 cities](https://github.com/Jessie-Watt/Data-analysis-of-student-s-information-health-record-and-their-performance-using-SQL./assets/140435577/4486913a-3ef4-4fc8-8d9b-0360f3c21e3c)

The most used pincode by employees.

# CONCLUSION
These task has exposed me to the use of SQL and its function.     
