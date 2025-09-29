# Queries

A dump of the SQL database was published by Prosobab in DANS (Waerzeggers and Groß 2022). To access the data in the dump we started MySql with the command:
```bash
mysql -u root -p
```
...and  created an empty database (you can use any name) in MySql:
```sql
mysql> CREATE DATABASE DB;
```
Using the command line, we inserted the dump into the new database:
```Bash
mysql -u root -p DB < prosobab-dump-2022-06-03.sql
```
Once back in MySql, we started using the the database:
```sql
mysql> USE DB;
```
To extract the data from the database, we had to create a file .my.conf in the home directory and add the path to the folder where we worked with these lines:
```bash
[mysqld]
secure_file_priv               = '<path_to_folder>'
```
The same path had to be used when writing the queries to file. These may differ depending on the computer and MySql version.

We executed the queries in the files in this folder. First one needs to create some temporary tables, i.e., to execute the queries in file CreateTemporaryTables.txt. The order of the other files is free.

#### Technical details

We used MySql Ver 9.2.0 for macos15.2 on arm64 on MacBook Air (M3) running on MacOS Sequoia 15.7.
