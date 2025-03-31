# Introduction to SQLite

SQLite is a relational database solution like PostgreSQL but has a lot of differences and is essentially it's own thing. In database solutions like PostgreSQL you have the database running on a server and you connect to it using a client application to interact with the database but in SQLite this is not the case.

SQLite is just a C library that manages the database files for us. Each database is a single file that the SQLite library manages and this makes it extremely portable since I can copy the file on any computer I'm working on and it'll work as it did before.

> [!Note]
>  SQLite is also the preferred archival format for the American Congress Library.

SQLite being a C library has a lot of limitations and is not and ideal solution for many use-cases even if it feels like the right choice. This is due to the fact that it's just a file, the whole database is one single file so it doesn't provide much security or other features that database solutions like PostgreSQL do.

SQLite is an embedded relational database, it runs great on devices with limited storage and compute. The developers make sure that the database can run on any hardware in almost in condition.
## Opensource software

SQLite is an opensource project, the whole source code for the C library is available online on GitHub for anyone to look at. 

What makes SQLite different from other OSS projects is that they don't accept any kind of contributions due to the project being used in highly unstable environments that require the most stable database solution and to maintain backwards compatibility with previous versions and hardware on which the database solution runs.