# Introduction to Databases

A database is a collection of persistent, interrelated, and shared data. Database Management Systems (DBMS) are collections of components that support the creation, use, and maintenance of databases.

A database stores data on storage drives for repetitive use, if the current data is no longer relevant it can be archived. It is stored in separate units that are connected together, databases store data in the form of entities and their relations. Databases allow data to be simultaneously accessed by multiple users.

>[!Note]
> A DBMS Includes tools for defining entity types, relationships, integrity constraints, and authorization rights. It allows non-tech savvy users to easily interact with the database by providing a simple GUI for easy interactions.

- Enterprise databases are designed to support large quantities of data. They have strong reliability and performance requirements and typically run on powerful servers.
- Desktop databases support small work-groups with smaller data quantities,modest reliability, and can easily run on consumer hardware.
- Embedded databases are part of the application they came with and are optimized to run on low-power hardware since they only need to handle the data of the application they are included in.
## Evolution

- First-gen databases supported sequential and random searching, requiring detailed computer programs to access data.
- Second-gen is when true databases were available and they could easily manage multiple entities but still required programming to access to the data stored in them.
- Third-gen relational databases were based on mathematical relations, with optimization technology to enable efficient access using non-procedural language to access data.
- Fourth-gen databases added the ability to store more data types like, images and videos.

> [!Note]
> Cloud computing and NoSQL databases have further increased the availability of databases that can store traditional and non-traditional data to a more wider audience.

## Procedural and Non-procedural Access

Procedural access and non-procedural access are two different ways of interacting with a database. Procedural access requires a user to write detailed computer programs that specify how to navigate through the database to access the data. Non-procedural access allows users to specify what data to retrieve, rather than how to retrieve it.  It is done primarily with the SQL `SELECT` statement.

## Third-party tools

Third-party software provides additional features that extend the capabilities of Database Management Systems (DBMS). These features can enhance database functionality in various ways, sometimes competing directly with the tools provided by the DBMS vendor.

>[!Note]
>Many vendors offer advanced design tools that enhance the database definition and tuning capabilities.

Third-party software can offer features that go beyond the standard capabilities of a DBMS. This can include specialized tools for tasks like data integration, data quality, or data warehouse management.

## Related Notes