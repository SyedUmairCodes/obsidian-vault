# Connections and Templates

You don't connect directly to the entire PostgreSQL cluster. Instead, you connect to a specific database within the cluster. This ensures that users only access the data they are authorized to see.

When a cluster is initialized using `initdb`, PostgreSQL creates two template databases: `template0` and `template1`. These databases serve as blueprints for creating new databases.

- template0 is a pristine template and shouldn't be modified or touched by any other user.
- template1 can be modified according to the needs of the user for creating databases using the template config.
- A standard installation also typically includes a `postgres` database, intended for use by the `postgres` administrator user.

PostgreSQL provides a command-line utility called `psql` that allows you to connect to your database from the terminal but there are also other libraries and programs available if you don't prefer the command-line.

Applications need a way to connect to the database programmatically.  This is achieved using a *connection string*, a URI-formatted string containing all the necessary parameters for establishing a connection.  This acts as the address that the application uses to find and connect to the correct database.

``` SQL
postgresql://user:password@host:port/database  
```

## Related Notes

- [[02-PSQL]]