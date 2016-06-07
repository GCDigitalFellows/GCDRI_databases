#SQLite “cheat sheet”

##Tips!
1. SQL is not case sensitive
2. End each SQL statement with a semicolon “;”
3. Use “*” to select an entire record
4. White space doesn’t matter
5. `SELECT` statement is like creating a new table
6. Field value needs to be in quotes
7. Use parentheses to force order of operations
8. Use two hyphens “--” to comment 

##C.R.U.D.

###Create
1. `CREATE DATABASE db_name` - creates a database

2. `CREATE TABLE table_name (field_name DATA_TYPE CONSTRAINTS)` - creates a table in the database
  1. Data types
    1. `DATE`
    2. `TIME`
    3. `TIMESTAMP`
    4. `VARCHAR/CHARACTER`
    5. `BOOLEAN`
    6. `INTEGER`
    7. `DOUBLE PRECISION (FLOAT)`
    8. `XML`

  2. Constraints
    1. `PRIMARY KEY`
    2. `FOREIGN KEY`
    3. `UNIQUE`
    4. `DEFAULT`
    5. `AUTOINCREMENT`
    6. `NOT NULL`

3. `INSERT INTO *table_name*(*field1, field2*) VALUES (*'value1'*, *'value2'*)` - insert data into a table for one record

4. `INSERT INTO *table_name*(*field1*) VALUES (*record1*), (*record2*), (*record3*)` - insert data into a table for multiple records


###Read
1. `SELECT *field1, field2* FROM *table_name*` - select fields from a table

2. `INNER JOIN *table1*, *table2* ON *table1.field = table2.field*` - create a new temporary table that includes data from table1 and table2 for only those records where table1.field = table2.field

3. `WHERE *table.field_a = "value_x"*` - only return records whose value for *field_a* is equal to *value_x*

4. `WHERE *table.field_a* IN ("value_x", "value_y", "value_z")` - only return records whose value for *field_a* is one of values in the parentheses 
5. `AND`
6. `BETWEEN`
7. `LIKE` (%..%)
8. `OR`

5. ORDER BY ASC/DESC
6. AS (alias for field name)

12. CONCAT
13. LENGTH
14. DISTINCT
15. UPDATE/SET
16. DELETE
17. LIMIT
18. BETWEEN
19. IS (NOT) NULL

##Functions
1. AVG()
2. COUNT()
3. MAX()
4. MIN()
5. SUM()
6. UCASE()
7. LCASE()
8. FIRST()
9. LAST()
10. GROUP BY

##Data types
1. DATE  
2. TIME  
3. VARCHAR  
4. INTEGER  
5. XML 

##Constraints  
    - PRIMARY KEY  
    - FOREIGN KEY  
    - UNIQUE  
    - DEFAULT  
    - AUTOINCREMENT  
    - NOT NULL

##Comparison operators  
1. `=`  
2. `==`  
3. `<`  
4. `<=`  
5. `>`  
6. `>=`  
7. `!=`  
8. `IN`  
9. `NOT IN`  
10. `BETWEEN`  
11. `IS`  
12. `IS NOT`  

##Update
1. `ALTER TABLE *table_name* RENAME TO *new_table_name*` - rename a table

2. `ALTER TABLE *table_name* ADD COLUMN *new_field_name* *DATA_TYPE* *CONSTRAINTS*` - add a new field to a table (include data type and field constraints)

##Delete
1. DELETE

2. `DROP TABLE *table_name*` - delete a whole table
