## Database Languages

- ****Data Definition Language****
- ****Data Manipulation Language****
- ****Data Control Language****
- ****Transactional Control Language****

## Data Definition Language (DDL)

****DDL**** is the short name for Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database.

- ****CREATE:**** to create a database and its objects like (table, index, views, store procedure, function, and triggers)
- ****ALTER:**** alters the structure of the existing database
- ****DROP:**** delete objects from the database
- ****TRUNCATE:**** remove all records from a table, including all spaces allocated for the records are removed
- ****COMMENT:**** add comments to the data dictionary
- ****RENAME:**** rename an object

## Data Manipulation Language (DML)

****DML**** is the short name for Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete and update data in a database. ****Data query language(DQL)**** is the subset of “Data Manipulation Language”. The most common command of DQL is ****SELECT**** statement. SELECT statement help on retrieving the data from the table without changing anything in the table.

- ****SELECT:**** retrieve data from a database
- ****INSERT:**** insert data into a table
- ****UPDATE:**** updates existing data within a table
- ****DELETE:**** Delete all records from a database table
- ****MERGE:**** UPSERT operation (insert or update)
- ****CALL:**** call a PL/SQL or Java subprogram
- ****EXPLAIN PLAN:**** interpretation of the data access path
- ****LOCK TABLE:**** concurrency Control

## Data Control Language (DCL)

****DCL**** is short for Data Control Language which acts as an access specifier to the database.(basically to grant and revoke permissions to users in the database

- ****GRANT:**** grant permissions to the user for running DML(SELECT, INSERT, DELETE,…) commands on the table
- ****REVOKE:**** revoke permissions to the user for running DML(SELECT, INSERT, DELETE,…) command on the specified table

## Transactional Control Language (TCL)

****TCL**** is short for Transactional Control Language which acts as an manager for all types of transactional data and all transactions. Some of the command of TCL are

- ****Roll Back:**** Used to cancel  or Undo changes made in the database 
- ****Commit:**** It is used to apply or save changes in the database
- ****Save Point:**** It is used to save the data on the temporary basis in the database

## ****Data Query Language (DQL)****

****Data query language(DQL)**** is the subset of ****“Data Manipulation Language”****. The most common command of DQL is the ****SELECT statement****. SELECT statement helps us in retrieving the data from the table without changing anything or modifying the table. DQL is very important for retrieval of essential data from a database.


![[DBMS Languages Graph.png]]