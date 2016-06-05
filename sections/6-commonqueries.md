#Querying your database  

Now that we have a decent looking database, we can execute some queries to manipulate our data.  

Each query is made up of the same basic set of clauses:  
- The `SELECT` clause indicates the fields that you want to return.  
- The `FROM` clause indicates the table that the fields belong to.  
- The `WHERE` clause filters the results of the query.  

Together, the `SELECT` clause essentially creates a new table based on the criteria specified in the `FROM` and `WHERE` clauses.  

1. This query returns all of the records (i.e., rows) in the "students" table:  
	```
	--SHOW ALL FIELDS FOR EACH RECORD IN THE TABLE STUDENTS
	SELECT *   --( '*' is a wildcard in SQL )
	FROM students;
	```  

2. This query returns only the values in the "student" field for all records in the "students" table:  
	```
	--SHOW THE VALUE FOR ONLY THE STUDENT FIELD FOR ALL RECORDS IN THE
	--TABLE STUDENTS
	SELECT student
	FROM students;
	```  

3. This query returns two fields from the "students" table:  
	```
	--SHOW THE VALUES FOR THE STUDENT AND ID FIELDS FOR ALL THE RECORDS IN
	--THE TABLE STUDENTS
	SELECT student, id
	FROM students;
	```  

	###Challenge:  
	* - Write a query that returns 'program' and 'program level' for each record in the 'programs' table *  

4. This filters the records by their value in the "id" field:  
	```
	--SHOW ALL FIELDS FOR EACH RECORD IN THE TABLE STUDENTS WHERE THE VALUE OF THE
	--ID FIELD IS EQUAL TO "3"
	SELECT *
	FROM students
	WHERE id = '3';
	```  

	###Challenge:  
	* - Write a query that returns entire records for only Ph.D programs in the 'programs' table *  

	
[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/5-foreignkeys.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/7-innerjoin.md)