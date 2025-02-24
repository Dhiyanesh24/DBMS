# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```
Create database studentdb;
```
### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/d3249f0e-b76f-461e-8f0c-c5b7d3e17163)


### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
 create table student(rollno int,name char(20),age int,address varchar(20),phoneno int);
```
### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/56bde580-1c1b-427a-80d7-1b9b38825df5)


### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table student add department char(30);
```
### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/7dc3b111-2895-4751-8b38-0e91c8859be0)


### 4) Rename the student table to mystudent

### SQL QUERY: 
```
drop table student;
```
### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/0b1b0f70-4bc6-45e6-8c0e-6ac5dc767a4b)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table student;
```
### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/9168dde8-82f5-471e-a576-ec260c0daf10)

### 4) Drop the mystudent table
 
### SQL QUERY: 
```
alter table student rename to mystudent;
```

### OUTPUT:
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/f37514ec-3f0c-4b62-8bfe-3bacf613a429)

## Result:
Thus the basic DDL commands in SQL are executed. 


