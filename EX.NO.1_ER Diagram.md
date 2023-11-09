# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/666efc95-91a0-440d-9a81-9fd84fe9af6a)



### Relational model
![image](https://github.com/Dhiyanesh24/DBMS/assets/118362288/c22332c6-044e-4005-bf1b-7aac814b5a1d)


### SQL DDL Schema 
```
CREATE TABLE Doctors
(
  Name INT NOT NULL,
  Address INT NOT NULL,
  PRIMARY KEY (Name),
  UNIQUE (Address)
);

CREATE TABLE Patients
(
  Type INT NOT NULL,
  Details INT NOT NULL,
  PRIMARY KEY (Type)
);

CREATE TABLE Tests
(
  Type INT NOT NULL,
  Description INT NOT NULL,
  PRIMARY KEY (Type)
);

CREATE TABLE Doctors_Specialization
(
  Specialization INT NOT NULL,
  Name INT NOT NULL,
  PRIMARY KEY (Specialization, Name),
  FOREIGN KEY (Name) REFERENCES Doctors(Name)
);

CREATE TABLE Doctors_Qualification
(
  Qualification INT NOT NULL,
  Name INT NOT NULL,
  PRIMARY KEY (Qualification, Name),
  FOREIGN KEY (Name) REFERENCES Doctors(Name)
);
```
## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
