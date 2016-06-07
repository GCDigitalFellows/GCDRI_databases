#Import data into table (15 min)  
1. Create a table with a field for each column in the csv file to import  
	```sqlite
	CREATE TABLE nypl_items (  
		id INTEGER PRIMARY KEY,  
		Title VARCHAR,  
		Contributor VARCHAR,  
		Date VARCHAR,  
		Language VARCHAR,  
		Description VARCHAR,  
		Note VARCHAR,  
		Subject VARCHAR,  
		Resource VARCHAR,  
		Genre VARCHAR,  
		Publisher VARCHAR,  
		Place VARCHAR,  
		url VARCHAR  
	);
	```  
2. Double click on the table in the databases window; click on the import icon  

3. Follow import instructions  

[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/7-innerjoin.md) - [Next >>>]()