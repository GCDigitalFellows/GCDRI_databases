6. Create a table called "students" with a field for: (1) a primary key, (2) student name, and (3) a foreign key that will reference the "programs" table  
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

	The structure of your "students" table should look like this:  

	![Structure of the new "students" table](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/student_tab_struc.png)  

	The foreign key points to a primary key in another table, in this case the "programs" table. This relationship is specified with the clause `FOREIGN KEY (id_program) REFERENCES programs(id)`, which links the "id_program" field in the "students" table to the "id" field in the "programs" table.  

	All records in the "students" table must point to a valid primary key in the "programs" table.  

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