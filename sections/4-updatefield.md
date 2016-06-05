[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/3-insertdata.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/5-foreignkeys.md)  

#Updating fields  

You can alter tables after they've been created. The SQL syntax below adds another field to the existing table and then populates that field with data.    

1. Add another field for "program_level" to the existing table:    
	```
	--ADD ANOTHER FIELD TO THE PROGRAMS TABLE
	ALTER TABLE programs
	ADD program_level VARCHAR;
	```

	If the query was successful, your database should now look like this:  

	![Your database after adding the new "program_level" field](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/new_field.png)  



2. Now, let's populate the new empty "program_level" field with some data  
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
	
[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/3-insertdata.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/5-foreignkeys.md)