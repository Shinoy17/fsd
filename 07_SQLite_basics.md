# SQLite Basics

## 1. Create Database
Create a database (test.db) and start the SQLite session.

```
CMD>sqlite3 test.db
SQLite version 3.38.2 2022-03-26 13:51:10
Enter ".help" for usage hints.
sqlite>
sqlite> .databases
main: D:\Swaminathan\Academics\2022 Jan FSD\sqlite\test.db r/w
```

## 2. Create a Table
Create a STUDENT table with
* Roll number - an integer attribute and also the primary key
* Name - a variable lengthed string
* Degree - a variable lengthed string
* DoB - a date variable

```
sqlite> CREATE TABLE [Students] (
   ...> Id INTEGER PRIMARY KEY NOT NULL,
   ...> Name VARCHAR(30) NOT NULL,
   ...> Degree VARCHAR(20),
   ...> DoB DATE
   ...> );
sqlite> .tables
Students
sqlite>
```

You can delete or rename a table by using DROP and ALTER commands. You can try this at leisure. The syntax for both is given below.
* DROP &langle;table_name&rangle; ;
* ALTER &langle;old_name&rangle RENAME TO &langle;new_name&rangle ;

Use .tables to check for the changed effect.

## Insert Values into Table

```
sqlite> INSERT INTO Students (Id, Name, Degree, DoB) VALUES (1, 'Amit', 'M.Tech', '2000-09-15');
sqlite> INSERT INTO Students VALUES (2, 'Ashok', 'M.Tech', '2000-06-13');
sqlite> INSERT INTO Students (Id, Name, Degree) VALUES (11, 'Seema', 'B.Tech');
sqlite> INSERT INTO Students (Id, Name, DoB) VALUES (13, 'Kamal', '2002-05-17');
sqlite> INSERT INTO Students (Id, Name) VALUES (12, 'George');
sqlite> INSERT INTO Students (Id, Degree, DoB) VALUES (7, 'M.Tech', '2000-09-15');
Runtime error: NOT NULL constraint failed: Students.Name (19)
sqlite> INSERT INTO Students (Id, Name, Degree, DoB) VALUES (1, 'Swapna', 'M.Tech', '2000-03-22');
Runtime error: UNIQUE constraint failed: Students.Id (19)
```
