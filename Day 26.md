# **Database**
**Database Servers:-**
* MySQL
* Postgre SQL
* MSSQL
* DB2
* Oracle 
* Aurora
* MariaDB

Take out the information as soon as possible


Attacks:-
* SSL Heartbleed
* BASH Injection
* SQL Injection

**Single Tier Architecture of Web Application->** In which same machine has Website and Database which is less secure as if website got hacked then DB is automatically hacked

**RDS (Relational Database Services)=>** It is a Amazon Portal which includes MySQL, Postgre SQL, MSSQL, Oracle, Aurora, MariaDB Servers (except DB2).

* SQL (Structured Query Language)-> Structured which includes rows, columns, etc.

* NOSQL (Not Only SQL)-> DynamoDB; Realtime Example:- PUBG

**Difference B/W SQL and NOSQL:-**

Where Schema is dynamic that is called NOSQL
Means where no need to create a seperate column for any specific data like if any user gives name and hobbies and you do not have hobbies section and other users are not giving hobbies.


**NOTE:-** MYSQL Database PORT NO - 3306

We can Remote SQL from anywhere in the world but Amazon declines the SSH usage as it does not gives any key. So it can connect with its PORT - 3306.

```
yum install mysql
```
Connecting using Endpoint from different system 
```
mysql -u root -h  _ENDPOINT_NAME_ -p
```
Commands In MYSQL:- 
```
show databases;

O/P:-
+--------------------+
| Database           |
+--------------------+
| information_schema |
| adhoc              |
| hello              |
| innodb             |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
7 rows in set (0.01 sec)
```
```
create database hello;
```
Database Migration:-

Migrating data from any Cloud to RDS

```
use adhoc;
```
```
show tables;
```

```
wget https://raw.githubusercontent.com/redashu/dbconnect/master/mysqldump/myfile.sql
```
```
mysql -u root -h _ENDPOINT_NAME_ -p adhoc <myfile.sql
```

How to connect database to Backend Language:-
---
* JAVA - JDBC(Java to DB Connector) / ODBC
* PYTHON - MySQL - Connector -> In Python DB is called Library
* PHP - MySQLi

```
pip3 install mysql-connector-python
```

```dbconn.py```
```
#!/usr/bin/python3

import mysql.connector as mysql
# RDS Information
u='root' # u=username
p='_PASSWD_'# p=password
db='adhoc'
h='_ENDPOINT_NAME_'  # h=host( ENDPOINT)

# now connceting
conn=mysql.connect(user=u,password=p,database=db,host=h)
# now generating a sql language cursor
cur=conn.cursor()

# now we can write sql query
cur.execute("show  tables;")
# now printing result
print(cur.fetchall())

# closing connection
conn.close()
```
