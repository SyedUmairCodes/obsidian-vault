# Key Features of PostgreSQL

PostgreSQL's procedural language allows you to create custom functions and stored procedures, extending the database's functionality and improving performance by executing logic directly within the database.

Triggers automatically execute predefined actions before or after specific events, such as inserting, updating, or deleting data.

Views provide customized perspectives of the underlying data without actually storing the data separately. Materialized views, on the other hand, store a pre-computed result set, improving query performance for complex queries but requiring updates when the underlying data changes.

PostgreSQL supports various programming languages beyond its built-in PL/pgSQL. This allows developers to use their preferred language (Perl, Python, Java, etc.) for creating custom functions and stored procedures.

PostgreSQL's extension system allows you to add new features and capabilities without recompiling the core database. This modular approach makes it easy to customize PostgreSQL to meet specific needs.

> PostgreSQL runs on a wide variety of operating systems, from Linux and Unix servers to macOS and Windows desktops, and even on resource-constrained devices like Raspberry Pi.

Before modifying data on disk, PostgreSQL writes a record of the intended change to the Write-Ahead logs. This ensures data durability even in the event of a crash (power failure, hardware failure, etc.). The WAL acts as a safety net, allowing the database to recover to a consistent state after an unexpected interruption.

## Related Notes
