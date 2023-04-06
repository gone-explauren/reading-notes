# Data Modeling

## SQL vs NoSQL
* What type of database is the best fit for the complex query intensive environment?
SQL

* What type of database is the best fit for hierarchical data storage?
NoSQL

* Describe the differences in scalability between a SQL and NoSQL database as though you were speaking to a non-technical friend.
  * SQL databases are typically *vertically scalable* 
    * When you want to expand your database, you can just add more and more processing power or storage space to make your server more powerful
  * NoSQL databases are *horizontally scalable*
    * When you want to expand your database, you must add another server to work alongside the existing one(s) to get more power from the server(s)

* How do we treat keywords and parameters differently in SQL syntax?
  * Keywords are called using "SELECT"
  * Parameters are called using "WHERE".

* Define normalization within the context of schemas and data.
  * Normalization is the process of organizing data in a database schema to *reduce data redundancy and improve data integrity.*
    * The goal of normalization is to eliminate data anomalies that can occur when data is stored in a denormalized or redundant manner.

* Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
  * *One to one* is where one table is linked to only one table and that table is only linked to it.
  * *One to many* is where many tables connect to one primary table.
  * *Many to many* is where multiple tables have multiple connections.

### References:
* <https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool>
* <https://www.youtube.com/watch?v=ZS_kXvOeQ5Y&ab_channel=Academind>

## SQL vs NoSQL
* Among data tables, what is a one-to-many relationship and how do we “relate” them?
One-to-many refers to*one table* having *many tables* related to it. Related tables are connected using a foreign key.

* Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
*design a diagram*

* Explain the difference between a primary and foreign key.
  * A primary key is *unique to it's table*
  * A foreign key belongs to another table, but is a *match to the primary key* so that they maintain a relation to each other.

### References:
* <https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/>
* <https://sequelize.org/docs/v6/>
