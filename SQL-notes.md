# To retrieve data from a SQL database, we need to write SELECT statements (queries). 
* A query in itself is just a statement which declares
  * what data we are looking for, 
  * where to find it in the database, and optionally, 
  * how to transform it before it is returned.

* You can think of a table in SQL as a type of an entity (ie. Dogs)
* Each row in that table would be a specific instance of that type (ie. A pug, a beagle, a different colored pug, etc). 
* The columns would then represent the common properties shared by all instances of that entity (ie. Color of fur, length of tail, etc).

* Given a table of data, the most basic query we could write would be one that selects for a couple columns (properties) of the table with all the rows (instances).
  **SELECT column, another_column, …
    FROM mytable;**
  * The result of this query will be a two-dimensional set of rows and columns, effectively a copy of the table, but only with the columns that we requested.

* To select all the columns, we would use an asterik
  **SELECT * 
    FROM mytable;**
* This query provides a simple way to inspect a table by dumping all the data at once.

# In order to filter certain results from being returned, we need to use a WHERE clause in the query. 
* The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

* Select query with constraints
  **SELECT column, another_column, …
    FROM mytable
    WHERE condition
    AND/OR another_condition
    AND/OR …;**
* More complex clauses can be constructed by joining numerous AND or OR logical keywords (ie. num_wheels >= 4 AND doors <= 2). 

## Operator Condition SQL Example
* Below are some useful operators that you can use for numerical data (ie. integer or floating point):
  * =, !=, < <=, >, >=	Standard numerical operators	col_name != 4
  * BETWEEN … AND …	Number is within range of two values (inclusive)	col_name BETWEEN 1.5 AND 10.5
  * NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	col_name NOT BETWEEN 1 AND 10
  * IN (…)	Number exists in a list	col_name IN (2, 4, 6)
  * NOT IN (…)	Number does not exist in a list	col_name NOT IN (1, 3, 5)
* Writing clauses makes the results more manageable and easier to understand
* Also, it constrains the set of rows returned
* This allows the query to run faster due to the reduction in unnecessary data being returned.

**SQL doesn't require you to write the keywords all capitalized**, but as a convention, it helps people distinguish *SQL keywords* from *column and tables names*, and makes the query easier to read.

## When writing WHERE clauses with columns containing text data...
* SQL supports a number of useful operators to do things like
  * case-insensitive string comparison
  * wildcard pattern matching.
  * etc.

* Operator Conditions
  * = Case sensitive exact string comparison *col_name = "abc"*
  * != or <> Case sensitive exact string inequality comparison *col_name != "abcd"*
  * LIKE Case insensitive exact string comparison	col_name *col_name LIKE "ABC"*
  * NOT LIKE Case insensitive exact string inequality comparison *col_name NOT LIKE "ABCD"*
  * %	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)
    *col_name LIKE "%AT%"* (matches "AT", "ATTIC", "CAT" or even "BATS")
  * _	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)
    *col_name LIKE "AN_"* (matches "AND", but not "AN")
  * IN (…)	String exists in a list	*col_name IN ("A", "B", "C")*
  * NOT IN (…)	String does not exist in a list	*col_name NOT IN ("D", "E", "F")*

**All strings must be quoted so that the query parser can distinguish words in the string from SQL keywords.**

**We should note that while most database implementations are quite efficient when using these operators,
* full-text search is best left to dedicated libraries like 
  * Apache,
  * Lucene,
  * or Sphinx. 
* These libraries are designed specifically to do full text search, and as a result:
  * are more efficient, and
  * can support a wider variety of search features including *internationalization and advanced queries.*

# Even though the data in a database may be unique, the results of any particular query may not be.
* SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
* This is helpful in cases such as the movie example, where multiple movies have been released in the same year

* Select query with unique results
  **SELECT DISTINCT column, another_column, …
    FROM mytable
    WHERE condition(s);**
* The *DISTINCT* keyword will blindly remove duplicate rows
* Discard duplicates based on specific columns using grouping and the *GROUP BY* clause.

## Ordering Results
* Most data in real databases are added in no particular column order.
* As a result, it can be difficult to read through and understand the results of a query as the size of a table increases to thousands or even millions rows.
* SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause.

* Select query with ordered results
  **SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC;**
* When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. 
* In some databases, you can also specify a collation to better sort data containing international text.

## Limiting results to a subset
* Another clause which is commonly used with the ORDER BY clause are the LIMIT and OFFSET clauses.
* These are useful for optimization to indicate to the database the subset of the results you care about.
* LIMIT will reduce the number of rows to return
* OFFSET will specify where to begin counting the number rows from. (offset is optional)

* Select query with limited rows
  **SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC
    LIMIT num_limit OFFSET num_offset;**
    
* If you think about websites like Reddit or Pinterest, the front page is a list of links sorted by popularity and time
* each subsequent page can be represented by sets of links at different offsets in the database. 
* Using these clauses, the database can then execute queries faster and more efficiently by processing and returning only the requested content.

**LIMIT and OFFSET are generally applied last after the other clauses have been applied.**

# Database normalization is useful because...
* it minimizes duplicate data in any single table
* allows for data in the database to grow independently of each other 
  * (ie. Types of car engines can grow independent of each type of car).
* As a trade-off, queries get slightly more complex since they have to be able to find data from different parts of the database
* performance issues can arise when working with many large tables.

**In order to answer questions about an entity that has data spanning multiple tables in a normalized database, we need to learn how to write a query that can combine all that data and pull out exactly the information we need.**

## Multi-table queries with JOINs
* Tables that share information about a single entity need to have a primary key that identifies that entity uniquely across the database. 
* One common primary key type is an auto-incrementing integer (because they are space efficient)
  * it can also be a string, hashed value, so long as it is unique.
* Using the JOIN clause in a query, we can combine row data across two separate tables using this unique key.

## Inner Join
* One type of JOIN clause
* a process that matches rows from the first table and the second table which have the same key (as defined by the ON constraint) to...
* create a result row with the combined columns from both tables. 
* After the tables are joined, the other clauses are then applied.

* Select query with INNER JOIN on multiple tables
  **SELECT column, another_table_column, …
    FROM mytable
    INNER JOIN another_table 
        ON mytable.id = another_table.id
    WHERE condition(s)
    ORDER BY column, … ASC/DESC
    LIMIT num_limit OFFSET num_offset;**
    
* You might see queries where the INNER JOIN is written simply as a JOIN. 
* These two are equivalent, but...
  * we will continue to refer to these joins as inner-joins 
  * this makes the query easier to read once you start using other types of joins

### References:
* <https://sqlbolt.com/>
* <https://cdn2.hubspot.net/hubfs/392937/Learn%20SQL.pdf>

### Completion:
![sql-queries-prep-complete](https://user-images.githubusercontent.com/123340286/228679345-474f2240-2ad9-4e21-8cd0-95379cdce4e7.jpg)

