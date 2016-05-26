#Databases - June 2016 GCDRI

## Session 1 
###Objectives:  
1. Develop a conceptual understanding of databases and SQL  
2. learn basic SQL syntax for creating databases and executing queries

####*What is a database?*

A database is a collection of data that is structured to allow for manipulation. There are different kinds of databases—one kind is a relational database. In a relational database, the data is contained in different tables. 

####*What is SQL?*

SQL (Structured Query Language) is a programming language for interacting with data in a relational database. There are different implementations of SQL—one implementation is [SQLite](https://www.sqlite.org/). Different implementations (such as [PostgreSQL](https://www.postgresql.org/) and [MySQL](https://www.mysql.com/)) have their own higher level specialized functions, but the all handle the same basic operations covered in this tutorial.

We’re going to use SQLite in this session because getting set up requires less work. SQLite is a little different from other implementations of SQL because it operates on regular plain old local files and does not require a server connection, unlike PostgreSQL and MySQL. The databases you work with in SQLite exist in .db files that you can store anywhere on your computer.

####*How do I use SQL?*

The database holds your data, but you need a client to see and interact with it. There are a couple options for SQLite GUI database mangers--for the first part of this session we will be suing [SQLiteStudio](http://sqlitestudio.pl/). SQLite also has a [command-line utility](http://www.sqlite.org/cli.html), which we will use in the second part of this session.

###Building a database
2. Build table (65 min)
  1. get concepts/reinforce variables and types

###**************Let's take a 15 minute break!**************

## Session 2
3. Import data into table (15 min)
4. General manipulation (30 min)
5. Databases vs. Excel (15 min)
6. SQL + Python 15 min)
  1. set up for Web Frameworks session