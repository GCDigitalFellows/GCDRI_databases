[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/10-pyplussql-pseudo.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/12-youdidit.md)

###SQL + Python = Awesome!  

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
print("Hello! I will search your nypl_items table for you! ")

# ask the user for a keyword
keyword = input("Please give me a keyword to search for: ")

# search the database for the keyword
# need SQL to query db!

# return a list of records from the database that contain the keyword
print
``` 

[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/10-pyplussql-pseudo.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/12-youdidit.md)




3. 
	# use the '.execute' method of the cursor object to execute SQL queries  
	# 