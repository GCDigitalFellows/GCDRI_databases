[<<< Back](9-excel_v_db.md) - [Back to top](../README.md)

# SQL + Python = Awesome!

You can create a program to interact with a database by embedding SQL syntax in a Python script (using the sqlite3 library, which comes standard with every Python install)

Let's write a short program that asks a user for a place name and returns all records from the database that contain the value in the "place" field.  

0\. From the command line, create a file called "nypl_search.py" in the directory where the "nypldb.db" database is, then open the file in Sublime  
_**Hint:** Use_ `touch` to create the file  

1\. Write the pseudocode in "nypl_search.py"

```Python
# import sqlite3 library

# connect to the database

# say hello to the user

# ask the user for a place

# search the place field in the "nypl_items" table for the place name

# return a list of records from the database that are from the place name
```

2\. Import the sqlite3 library, connect to the database, and create a cursor object (don't worry about this last part)

```Python
# import sqlite3 library
import sqlite3

# connect to the database
conn = sqlite3.connect('nypldb.db')

# create a cursor object  
c = conn.cursor()
```  

3\. Translate pseudocode to Python and SQL

```Python
# say hello to the user
print("Hello! I will search your database for items from any place you tell me! ")

# ask the user for a place name
place_name = input("Please give me a place name: ")

# search the place field for the place name
cur.execute("SELECT * FROM nypl_items WHERE place = ?", (place_name,))

# return a list of records from the database that contain the keyword
record_list = cur.fetchall()

for i in record_list:
	print("\n\n", i)
``` 

4\. Run the program. First, open the command line, `cd` to the directory containing your "nypl_search.py" file and "nypldb.db" database. Then type 

    python3 nypl_search.py
	
and hit Enter.

[<<< Back](9-excel_v_db.md) - [Back to top](../README.md)
