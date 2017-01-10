[<<< Back](7-commonqueries.md) - [Next >>>](9-importcsv.md)  

# Joins

Each of the queries up to now has just returned data from a single table in the database. This final query combines our "students" and "programs" tables using the `INNER JOIN` and `ON` clause:

```
-- SHOW ALL THE RECORDS FOR STUDENTS WITH 
-- INFORMATION ABOUT THEIR RESPECTIVE PROGRAMS

SELECT *
FROM students INNER JOIN programs
ON students.id_program = programs.id;
```

This query should return what you see below:

![Result of a query joining the "students" and "programs" tables](https://github.com/GCDigitalFellows/GCDRI_databases/blob/master/images/join_table.png)  

This query demonstrates the power of relational databases by using the foreign key in the "students" table to coordinating data with the "programs" table.  

### Challenge

Write a query that returns only the name of each student and their respective program level.  


### Solution

```
SELECT student, program_level
FROM students INNER JOIN programs
ON students.id_program = programs.id;
```
	
[<<< Back](7-commonqueries.md) - [Next >>>](9-importcsv.md)
