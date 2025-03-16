# Relational Data Model

The relational data model is based on the idea of using tables to organize data. A relational database is a collection of tables and each table has a heading and a body. The heading includes the table name and column names. The body contains the data in rows.

> Each row in a table represents a single record (e.g., one student), and each column represents a specific attribute (e.g., student's major)

It's not sufficient to understand tables individually; it's also important to understand how tables relate to each other. Relationships between tables are established through matching values in specific columns. For instance, a 'student' table and an 'enrollment' table might be linked by matching student numbers.

Relationships between rows in different tables are indicated by matching identical values in shared columns. Matching values allow combining data from multiple tables to extract meaningful information, an operation known as a "join".

The relational data model has been the dominant standard in the database industry for over 35 years due to its simplicity, strong theoretical foundation, many implementations, and the commercial standard SQL.

## Related Notes