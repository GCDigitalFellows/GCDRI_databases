###Building tables
The next step is to create tables to hold your data. From here onwards, we are going to execute database queries using the SQL editor to practice SQL syntax.  

The syntax for creating a table in SQLite is:

`CREATE TABLE [table_name] ( [field_name] [data type] [constraints] )`  

- The [data type](https://www.sqlite.org/datatype3.html) will affect the behavior of the data in that field.   
 

- The [constraints](http://www.tutorialspoint.com/sqlite/sqlite_constraints.htm) will  affect the behavior of the data in that field.   
  

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