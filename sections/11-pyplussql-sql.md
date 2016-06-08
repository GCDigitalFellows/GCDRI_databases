[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/10-pyplussql-pseudo.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/12-youdidit.md)

#SQL + Python = Awesome!  

####Step 2: Import the sqlite3 library, connect to the database, and create a cursor object (don't worry about this last part)

```Python
# import sqlite3 library
import sqlite3

# connect to the database
conn = sqlite3.connect('/Users/ianphillips/Dropbox/DigitalFellows/GCDRI-db/nypldb.db')

# create a cursor object  
c = conn.cursor()
```  

####Step 3: Translate pseudocode to Python and SQL

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

####Step 4: Run the program from the command line  

1. Open the command line, `cd` to the directory containing your "nypl_search.py" file and "nypldb.db" database  

2. Type `python nypl_search.py` and hit Enter  


[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/10-pyplussql-pseudo.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/12-youdidit.md)
