# What is a Schema?
* a table in a database is a two-dimensional set of rows and columns with
  * the columns being the properties, and
  * the rows being instances of the entity in the table.
* In SQL, the database schema is what *describes the structure of each table*, and *defines the datatypes that each column of the table can contain*.

# Inserting new data
* When inserting data into a database, we need to use an INSERT statement
* an INSERT statement declares... 
  * which table to write into, 
  * the columns of data that we are filling, 
  * and one or more rows of data to insert.
* You can insert multiple rows at a time by just listing them sequentially.

* Insert statement with values for all columns
  **INSERT INTO mytable
    VALUES (value_or_expr, another_value_or_expr, …),
           (value_or_expr_2, another_value_or_expr_2, …),
           …;**
* If you have incomplete data and the table contains columns that support default values, you can insert rows with only the columns of data you have by specifying them explicitly.

* Insert statement with specific columns
  **INSERT INTO mytable
    (column, another_column, …)
    VALUES (value_or_expr, another_value_or_expr, …),
          (value_or_expr_2, another_value_or_expr_2, …),
          …;**
* In these cases, the number of values need to match the number of columns specified. 
  * Despite this being a more verbose statement to write, inserting values this way has the benefit of being forward compatible. 
  * ex: if you add a new column to the table with a default value, no hardcoded INSERT statements will have to change as a result to accommodate that change.

* In addition, you can use mathematical and string expressions with the values that you are inserting.
  * This can be useful to ensure that all data inserted is formatted a certain way.

* Example Insert statement with expressions
  **INSERT INTO boxoffice
    (movie_id, rating, sales_in_millions)
    VALUES (1, 9.9, 283742034 / 1000000);**
    
# Update existing data
* Use an UPDATE statement. 
* Similar to the INSERT statement, you have to specify exactly which table, columns, and rows to update. 
* In addition, the data you are updating has to match the data type of the columns in the table schema.

* Update statement with values
  **UPDATE mytable
     SET column = value_or_expr, 
        other_column = another_value_or_expr, 
        …
     WHERE condition;**
* The statement works by taking multiple column/value pairs, and applying those changes to each and every row that satisfies the constraint in the WHERE clause.

* One helpful tip is to always write the constraint first and test it in a SELECT query to make sure you are updating the right rows, and only then writing the column/value pairs to update.

# Delete data from a table in the database
* Use a DELETE statement
  * describes the table to act on, and the rows of the table to delete through the WHERE clause.

* Delete statement with condition
  **DELETE FROM mytable
    WHERE condition;**
* If you decide to leave out the WHERE constraint, then ***all rows are removed***, which is a quick and easy way to clear out a table completely (if intentional).

* it is highly recommended that you run the constraint in a SELECT query first to ensure that you are removing the right rows. 
* Without a proper backup or test database, it is easy to **irrevocably** remove data
* ***Always read your DELETE statements twice and execute once.***

# Creating Tables
* When you have new entities and relationships to store in your database, you can create a new database table using the CREATE TABLE statement.

* Create table statement w/ optional table constraint and default value
  **CREATE TABLE IF NOT EXISTS mytable (
     column DataType TableConstraint DEFAULT default_value,
     another_column DataType TableConstraint DEFAULT default_value,
     …
    );**
* The structure of the new table is defined by its table schema, which defines a series of columns.
* Each column has a name, the type of data allowed in that column, an optional table constraint on values being inserted, and an optional default value.

* If there already exists a table with the same name, the SQL implementation will usually throw an error
  * To suppress the error and skip creating a table if one exists, you can use the IF NOT EXISTS clause.

## Data Table Types
* The most commonly supported data types are:
  * INTEGER,
     * The integer datatypes can store whole integer values like the count of a number or an age.
  * BOOLEAN,
     * In some implementations, the boolean value is just represented as an integer value of just 0 or 1.
  * FLOAT, 
  * DOUBLE, 
  * REAL,
     * The floating point datatypes (prev, prev, prev) can store more precise numerical data like measurements or fractional values. 
     * Different types can be used depending on the floating point precision required for that value.
  * CHARACTER(num_chars), 
  * VARCHAR(num_chars), 
     * Both the CHARACTER and VARCHAR (variable character) types are specified with the max number of characters that they can store (longer values may be truncated)
     * this means they can be more efficient to store and query with big tables.
  * TEXT	
     * The text based datatypes can store strings and text in all sorts of locales. 
     * The distinction between the various types generally amount to underlaying efficiency of the database when working with these columns.
  * DATE, 
  * DATETIME,
     * SQL can also store date and time stamps to keep track of time series and event data. 
     * They can be tricky to work with especially when manipulating data across timezones.
  * BLOB	
     * Finally, SQL can store binary data in blobs right in the database. 
     * These values are often opaque to the database, so you usually have to store them with the right metadata to requery them.

## Table Constraints
* each column can have additional table constraints on it which limit what values can be inserted into that column.

* Common Contraints
  * PRIMARY KEY	
    * This means that the values in this column are unique, and each value can be used to identify a single row in this table.
  * AUTOINCREMENT	
    * For integer values, this means that the value is automatically filled in and incremented with each row insertion. 
    * Not supported in all databases.
  * UNIQUE	
    * This means that the values in this column have to be unique
    * you can't insert another row with the same value in this column as another row in the table. 
    * Differs from the `PRIMARY KEY` in that it doesn't have to be a key for a row in the table.
  * NOT NULL	
    * This means that the inserted value can not be `NULL`.
  * CHECK (expression)	
    * This allows you to run a more complex expression to test whether the values inserted are valid. 
    * ex, you can check that values are positive, or greater than a specific size, or start with a certain prefix, etc.
  * FOREIGN KEY	
    * This is a consistency check which ensures that each value in this column corresponds to another value in a column in another table.
    * For example, if there are two tables, one listing all Employees by ID, and another listing their payroll information, the `FOREIGN KEY` can ensure that every row in the payroll table corresponds to a valid employee in the master Employee list.

* Here's an example schema for a Movies table:
  **CREATE TABLE movies (
        id INTEGER PRIMARY KEY,
        title TEXT,
        director TEXT,
        year INTEGER, 
        length_minutes INTEGER
    );**
    
# Altering Tables
* Use the ALTER TABLE statement to add, remove, or modify columns and table constraints.

* Adding columns
  **ALTER TABLE mytable
      ADD column DataType OptionalTableConstraint 
      DEFAULT default_value;**
* In some databases like MySQL, you can even specify where to insert the new column using the FIRST or AFTER clauses
      
* Removing columns
  **ALTER TABLE mytable
      DROP column_to_be_deleted;**
* some databases (including SQLite) don't support this feature. 
* Instead you may have to create a new table and migrate the data over
      
* Renaming the table
  **ALTER TABLE mytable
      RENAME TO new_table_name;**
      
# Dropping Tables
* In some rare cases, you may want to remove an entire table including all of its data and metadata
* to do so, you can use the DROP TABLE statement
  * This differs from the DELETE statement in that it also removes the table schema from the database entirely.

**DROP TABLE IF EXISTS mytable;**

* Like the CREATE TABLE statement, the database may throw an error if the specified table does not exist
  * to suppress that error, you can use the IF EXISTS clause.

**if you have another table that is dependent on columns in table you are removing (for example, with a FOREIGN KEY dependency) then you will have to either update all dependent tables first to remove the dependent rows or to remove those tables entirely.**

### References:
* <https://sqlbolt.com/lesson/inserting_rows>
