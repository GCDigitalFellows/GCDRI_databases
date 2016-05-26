#SQLite “cheat sheet”

##Tips!
1. SQL is not case sensitive
2. End each SQL statement with a “;”
3. Use “*” to select a record
4. White space doesn’t matter
5. Select statement is like creating a new table
6. Field value needs to be in quotes
7. se parentheses to force order of operations
8. “--” to comment 

##Creating databases
1. CREATE DATABASE db_name

##Creating tables
1. CREATE TABLE table_name (field DATA TYPE CONSTRAINT)
  1. Data types
    1. DATE
    2. TIME
    3. TIMESTAMP
    4. VARCHAR/CHARACTER
    5. BOOLEAN
    6. INTEGER
    7. DOUBLE PRECISION (FLOAT)
    8. XML  

  2. Constraints
    1. PRIMARY KEY
    2. FOREIGN KEY
    3. UNIQUE
    4. DEFAULT
    5. AUTOINCREMENT
    6. NOT NULL

##Querying the database
1. SELECT/FROM
2. INSERT INTO (VALUES)
3. INNER JOIN
4. WHERE (like a filter)
5. ORDER BY ASC/DESC
6. AS (alias for field name)
7. IN
8. AND
9. BETWEEN
10. LIKE (%..%)
11. OR
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

