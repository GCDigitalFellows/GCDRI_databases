###Import existing database (15 min)  


###Queries (30 min)
1. 

###Excursus: Databases vs. Excel (15 min)  
1. volume, volume, volume!  

###SQL + Python = Awesome (15 min)
You can embed SQL syntax in a Python script using the sqlite3 library  

Let's write a short Python script that will let the user query the database from the terminal.  

1. First write the Python part:  
	```
	# ask the user what kind of data they want

	# ask the user for key words

	# return records from the database that contain the keywords in a list
	```  

2. Next import the sqlite3 library, connect to the database, and create a cursor object  
	```
	# import the sqlite3 library
	import sqlite3

	# connect to the database
	conn = sqlite3.connect('testdb.db')

	# create a cursor object  
	c = conn.cursor()
	```  

3. 
	# use the '.execute' method of the cursor object to execute SQL queries  
	# 
