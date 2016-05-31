#Databases - June 2016 GCDRI

## Session 1 
###Objectives:  
1. Develop a conceptual understanding of databases and SQL  
2. Learn basic SQL syntax for creating databases and executing queries

####*What is a database?*

A database is a collection of data that is structured to allow for manipulation. There are different kinds of databases—one kind is a relational database. In a relational database, the data is contained in different tables. 

####*What is SQL?*

SQL (Structured Query Language) is a programming language for interacting with data in a relational database. There are different implementations of SQL—one implementation is [SQLite](https://www.sqlite.org/). Different implementations (such as [PostgreSQL](https://www.postgresql.org/) and [MySQL](https://www.mysql.com/)) have their own higher level specialized functions, but the all handle the same basic operations covered in this tutorial.

We’re going to use SQLite in this session because getting set up requires less work. SQLite is a little different from other implementations of SQL because it operates on regular plain old local files and does not require a server connection, unlike PostgreSQL and MySQL. The databases you work with in SQLite exist in .db files that you can store anywhere on your computer.

####*How do I use SQL?*

The database holds your data, but you need a client to see and interact with it. There are a couple options for SQLite GUI database mangers--for the first part of this session we will be suing [SQLiteStudio](http://sqlitestudio.pl/). SQLite also has a [command-line utility](http://www.sqlite.org/cli.html), which we will use in the second part of this session.

###Building a database  
1. Create a database file using the SQLite GUI.  

	![Create a database using SQLite GUI](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/add_db.png)  

2. Give your database a name and make sure to save it to a directory that is outside of the SQLiteStudio download folder.  

	![Name your database file and save it outside of the SQLiteStudio download folder](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/db_info.png)  

3. Connect to the database you just created.    

	![Connect to the database you just created](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/conn_db.png)  

###Building tables
The next step is to create tables to hold your data. From here onwards, we are going to execute database queries using the SQL editor, so you can get used to SQL syntax.  

The syntax for creating a table in SQLite is:

`CREATE TABLE [table_name] ( [field_name] [data type] [constraints] )`  

- The [data type](https://www.sqlite.org/datatype3.html) will affect the behavior of the data in that field. SQL data types are things like DATE, TIME, VARCHAR, INTEGER, XML.  

- The [constraints](http://www.tutorialspoint.com/sqlite/sqlite_constraints.htm) will  affect the behavior of the data in that field. Constraints are things like PRIMARY KEY, FOREIGN KEY, UNIQUE, DEFAULT, AUTOINCREMENT, NOT NULL.  

1. Open the SQL editor.  

	![To open SQL editor, click “Tools” and “Open SQL editor”](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/open_sql_ed.png)  

	Your SQLiteStudio interface should look like this:  

	![SQLiteStudio interface with SQL editor and databases window](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/sqlite_wkspace.png)  

2. Create a table called "programs" with a field (i.e., column) for academic programs  
	```
	CREATE TABLE programs  
	(  
	id INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,  
	program VARCHAR  
	);
	```

	![Creating "programs" table](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/create_table.png)  

3. Insert some data into the table we just created  
	```
	INSERT INTO programs(program) VALUES
	(‘Anthropology’),
	(‘Biology’),
	(‘Linguistics’);
	```

	Click on "Data" to view the data that you just inserted into the "programs" table.  

	![Click "Data" to view "programs" table with new data](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/view_table.png)

4. Add another field for "program_level" to the existing table  
	```
	--ADD ANOTHER FIELD TO THE PROGRAMS TABLE
	ALTER TABLE programs
	ADD program_level VARCHAR;
	```

	If the query was successful, your database should now look like this:  

	![Your database after adding the new "program_level" field](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/new_field.png)  

5. Now, let's populate the new empty "program_level" field with some data  
	```
	--UPDATE THE PROGRAM_LEVEL FIELD FOR "LINGUISTICS"
	UPDATE programs
	SET program_level = 'Master''s'
	WHERE program = 'Linguistics';
	```  

	```
	--UPDATE THE PROGRAM_LEVEL FIELD FOR "ANTHROPOLOGY" AND "BIOLOGY"
	UPDATE programs
	SET program_level = 'Ph.D.'
	WHERE program IN ('Anthropology', 'Biology');
	```  

	At this point, we're going to create another table called "students" to illustrate the relational nature of relational databases. We use the same syntax that we used to create the "programs" table, but with one extra element: a foreign key.  

6. Create a table called "students" with a field for (1) a primary key, (2) student name, and (3) a foreign key that will reference the "programs" table  
	```
	--CREATE A TABLE FOR STUDENTS (PAY ATTENTION TO THE FOREIGN KEY!)
	CREATE TABLE students
	(
	id INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
	student VARCHAR(255),
	id_program INTEGER,
	FOREIGN KEY (id_program) REFERENCES programs(id)
	);
	```  

	The structure of your "studnets" table should look like this:  

	![Structure of the new "students" table](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/student_tab_struc.png)  

	The foreign key points to a primary key in another table, in this case the ‘programs’ table. This relationship is specified with the clause `FOREIGN KEY (id_program) REFERENCES programs(id)`, which links the ‘id_program’ field in the ‘students’ table to the ‘id’ field in the ‘programs’ table. This relationship requires that all records in the ‘students’ table point to a valid primary key in the ‘programs’ table.  

7. The last step is to add some data to the new "students" table
	```
	--INSERT SOME DATA INTO THE STUDENTS TABLE
	--REMEMBER THAT THE PRIMARY KEY WILL AUTOINCREMENT
	--FOREIGN KEYS MUST BE ENTERED MANUALLY
	INSERT INTO students(student, id_program) VALUES
	('Josefina', 3),
	('Cecilia', 2),
	('Nico', 2),
	('Sarah', 1);
	```  

###**************Let's take a 15 minute break!**************

## Session 2
###Objectives: 
1. Practice querying your data  
2. Learn how to import existing data into a db table  
3. Integrate SQL with Python


###Import data into table (15 min)
###General manipulation (30 min)
###Excursus: Databases vs. Excel (15 min)
###SQL + Python = Awesome (15 min)
  1. set up for Web Frameworks session