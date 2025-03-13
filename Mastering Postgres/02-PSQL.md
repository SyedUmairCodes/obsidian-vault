# The PostgreSQL Command Line

PostgreSQL comes with `psql`, the command-line interface for PostgreSQL.For those who prefer using a command line interface to interact with their databases. 

To connect, you simply type `psql -d` followed by your database name, using default credentials if you've set it up with `Postgres.app`. Once inside, `\?` brings up the help menu that lists all the available commands. 

> You can describe the database, schema, or tables using `\d`, very useful for seeing the database structure. 

For example, `\d users` describes the "users" table, showing columns, types, and indexes. Lastly, to improve output, the instructor demonstrates setting the output format to "auto" with `\x auto`, which dynamically adjusts based on the terminal size.

## Related Notes