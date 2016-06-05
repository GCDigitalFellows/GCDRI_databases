#Inner join!

Each of the queries up to now is just returning data from one table in the database. This final query combines our "students" and "programs" tables using the `INNER JOIN` and `ON` clause:  

```
--SHOW ALL THE RECORDS FOR STUDENT WITH THE INFORMATION ABOUT THEIR
--RESPECTIVE PROGRAMS
SELECT *
FROM students INNER JOIN programs
ON students.id_program = programs.id;
```  

This query should return what you see below:  

![Result of a query joining the "students" and "programs" tables](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/join_table.png)  

This query demonstrates the power of relational databases by using the foreign key in the "students" table to coordinating data with the "programs" table.  
	
[<<< Back](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/6-commonqueries.md) - [Next >>>](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/sections/breaktime.md)