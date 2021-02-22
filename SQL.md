# SQL

**SQL** commands can be executed in two distinct contexts:

- Commands sent directly to a database.
- Commands executed from a Java application.

The syntax is slightly different in these two contexts.

Most databases have multiple tables. They frequently use foreign references to allow data from one table to be referenced from another table.

SQL has five important types of statements:

`CREATE TABLE` statements create database tables. These statements specify each of the columns in a table and specify table-level constraints such as foreign references.
`INSERT` _statements add rows to database tables._
`DELETE` _statements delete rows from database tables._
`UPDATE` _statements modify rows in database tables._
`SELECT` _statements are used to retrieve data from database tables. These statements return tables, often constructed from columns from multiple tables._

`DELETE`, `UPDATE,` and `SELECT` statements can use a WHERE clause to limit the rows that are affected or returned and to capture foreign reference relationships.
