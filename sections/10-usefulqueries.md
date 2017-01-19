[<<< Back](9-importcsv.md) - [Next >>>](11-queries_challenge.md)  

# Querying to summarize your data  

Let's see what the nypl_items table looks like:  

1. How many records are in the table?  

```sql
SELECT COUNT(*) FROM nypl_items;  
```  

2. What do the records look like?  

```sql
SELECT * FROM nypl_items LIMIT 3;
```  

3. How many different languages do you have items in?  

```sql
SELECT DISTINCT language FROM nypl_items;
```  

## Take 5 minutes to explore the nyply_items--what can you tell us about it?  

- How many publishers? Unique publishers?  

- What is the oldest item?  

- How many items are in the genre "Engravings"?  

- Where is the greatest number of items from?  


[<<< Back](9-importcsv.md) - [Next >>>](11-queries_challenge.md)