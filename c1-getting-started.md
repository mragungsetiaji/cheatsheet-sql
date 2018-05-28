# Chapter 1: Getting started with SQL
|Version |Short Name| Standard| Release Date|
|---|----|---|---|
| 1986 |SQL-86 |ANSI X3.135-1986, ISO 9075:1987 |1986-01-01| 
| 1989 |SQL-89 |ANSI X3.135-1989, ISO/IEC 9075:1989 |1989-01-01| 
| 1992 |SQL-92 |ISO/IEC 9075:1992 |1992-01-01 |
| 1999 |SQL:1999 |ISO/IEC 9075:1999 |1999-12-16| 
| 2003 |SQL:2003 |ISO/IEC 9075:2003 |2003-12-15 |
| 2006 |SQL:2006 |ISO/IEC 9075:2006 |2006-06-01 |
| 2008 |SQL:2008 |ISO/IEC 9075:2008 |2008-07-15 |
| 2011 |SQL:2011 |ISO/IEC 9075:2011 |2011-12-15 |
| 2016 |SQL:2016 |ISO/IEC 9075:2016 |2016-12-01 |

## Section 1.1: Overview
Structured Query Language (SQL) is a special-purpose programming language designed for managing data held in a Relational Database Management System (RDBMS). SQL-like languages can also be used in Relational Data Stream Management Systems (RDSMS), or in "not-only SQL" (NoSQL) databases.

SQL comprises of 3 major sub-languages:
1. Data Deﬁnition Language (DDL): to create and modify the structure of the database;
2. Data Manipulation Language (DML): to perform Read, Insert, Update and Delete operations on the data of the database; 
3. Data Control Language (DCL): to control the access of the data stored in the database.

### SQL article on Wikipedia
The core DML operations are Create, Read, Update and Delete (CRUD for short) which are performed by the statements INSERT, SELECT, UPDATE and DELETE. There is also a (recently added) MERGE statement which can perform all 3 write operations (INSERT, UPDATE, DELETE).

### CRUD article on Wikipedia
Many SQL databases are implemented as client/server systems; the term "SQL server" describes such a database. At the same time, Microsoft makes a database that is named "SQL Server". While that database speaks a dialect of SQL, information speciﬁc to that database is not on topic in this tag but belongs into the SQL Server documentation.