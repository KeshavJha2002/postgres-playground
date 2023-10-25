+ `\l` -> lists all the databases in the system.
+ `\help` -> lists all the postgres commands.

## It seems that sometimes postgres is case sensitive by default. So it is expected to use uppercase for keywords.

### Working on a list of databases
+ `\c database_name` -> to open a database.
+ `CREATE DATABASE database_name;` -> to create a database.      

### Working inside a database
+ `\dt` -> to list all the tables in a list.
+ `CREATE TABLE table_name(col1 col_type,...);` -> to create a table.
+ `CREATE TABLE students(id SERIAL PRIMARY KEY,name char,age int,adult boolean);` -> SERIAL is kind of a datatype that acts like an auto-increment.
+ `DROP TABLE table_name;` -> drops the table/tables permanently.
