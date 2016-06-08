[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/9-excel_v_db.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/11-pyplussql-sql.md)

#SQL + Python = Awesome!  

You can create a program to interact with a database by embedding SQL syntax in a Python script (using the sqlite3 library)  

Let's write a short program that asks a user for a place name and returns all records from the database that contain the value in the "place" field.  

####Step 0: From the command line, create a file called "nypl_search.py" in the directory where the "nypldb.db" database is, then open the file in Sublime  
_**Hint:** Use_ `touch` to create the file  


####Step 1: Write the pseudocode in "nypl_search.py"

```Python
# import sqlite3 library

# connect to the database

# say hello to the user

# ask the user for a place

# search the place field in the "nypl_items" table for the place name

# return a list of records from the database that are from the place name
```  

[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/9-excel_v_db.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/11-pyplussql-sql.md)