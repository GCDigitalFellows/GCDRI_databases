[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/2-buildtable.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/4-updatefield.md)  

#Inserting data into an SQL table

Now that we have a table structure, we need to insert some data.  

1. Insert "Anthropology", "Biology", and "Linguistics" into the table we just created. 

	**Remember:**  
		- Highlight this code before clicking the triangle to execute!  
		- Comment your code with `--`

	The syntax for inserting multiple records is: `INSERT INTO table_name(field_name) VALUES (record1), (record2), (record3)`

	```
	INSERT INTO programs(program_name) VALUES
	("Anthropology"),
	("Biology"),
	("Linguistics");
	```

2. Click on "Data" to view the data that you just inserted into the "programs" table.  

	![Click "Data" to view "programs" table with new data](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/view_table.png)  
	
[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/2-buildtable.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/4-updatefield.md)