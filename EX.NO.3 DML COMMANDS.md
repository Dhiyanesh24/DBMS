# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```
update manager set salary=salary+(salary*0.10);
```


### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/1a248d05-48c0-4a77-9d36-2a32d5ab0edf)


### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
```
delete from manager where salary<2750;
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/107e2c40-0fd4-4137-98a6-912974418316)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
```
select ename as "Name",salary*12 as "Annual salary" from manager;
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/c67aceb3-a026-4c4f-9152-2c98d0c0bcee)

### Q4) List the name of Clerks from emp table


### QUERY:
```
select ename from manager where designation='clerk';
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/c14c8160-a8f7-47dc-87d7-56548d73edf0)



### Q5)	List the names of employee who are not Managers.


### QUERY:
```
select ename from manager where designation <> 'manager';
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/2ab0edb8-91c6-45e5-a6bb-360efc3768fd)


### Q6)	List the names of employees not eligible for commission.


### QUERY:
```
select ename from manager where commission=0;
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/17603e99-21f9-48d4-b5a8-3dfd2532a43b)


### Q7)	List employees whose name either start or end with ‘s’.


### QUERY:
```
select ename from manager where ename like '%s' or ename like 's%';
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/e4a888d5-3869-4141-935f-472439f4f524)


### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
```
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/68250ffe-633b-47cb-9374-cf5e87579ec0)



### Q9) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
```
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/ddd221f3-4bb5-4679-8f44-13df49ae4182)



### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
```
select ename,deptno,salary from manager order by deptno asc,salary desc;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/0295911a-b081-478f-a60a-79af3edff8b5)


### Q11) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
```
select ename from manager where deptno not in (30,40,10);
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/af587a65-aa5a-4ed3-89e7-939020bcaa34)


### Q12) Find number of rows in the table EMP

### QUERY:
```
select count(*) from manager;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/dd10001e-8cb5-485e-bfc0-314e093f2b84)



### Q13) Find maximum, minimum and average salary in EMP table.

### QUERY:
### MAXIMUM:
```
select max(salary) from manager;
```

### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/970202af-891d-42ce-b98e-4eafa45b1ade)
### MINIMUM:
```
select min(salary) from manager;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/29fd1c20-9567-49f1-97cb-287e71e91140)


### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
```
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;
```
### OUTPUT:
![image](https://github.com/DrUmaRaniV/DBMS/assets/118362288/c1785bb4-d375-404d-9d44-9fd7ffa3e81e)


## RESULT :
Thus the basic DML commands are executed.
