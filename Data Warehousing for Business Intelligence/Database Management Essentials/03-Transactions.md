# Transaction Processing

Transaction processing is a critical function of a DBMS that ensures the reliable and efficient processing of large volumes of repetitive work. It involves a collection of operations that must be processed as one unit of work. The DBMS provides services to ensure that transactions are processed correctly without interference from concurrent users and without loss of data due to failures.

>[!Note]
>A transaction is a user-defined concept, meaning that the user specifies which operations are part of a transaction.

  A transaction is a single unit of work that should be processed reliably. It can include any number of reads and writes to a database. Transactions are defined using SQL statements such as `START TRANSACTION, COMMIT`, and `ROLLBACK`.

- A transaction is indivisible; either all operations succeed, or none do. If any part of the transaction fails, the entire transaction is rolled back to its previous state.
- A transaction must maintain the database's integrity. If the database is in a consistent state before the transaction, it must also be in a consistent state after the transaction.
- Transactions must operate independently of each other. Concurrent transactions should not interfere with each other.
- Once a transaction is committed, its changes are permanent and will survive system failures.
## Concurrency
Concurrency control is essential to manage multiple users accessing and modifying the same data concurrently. It prevents interference among concurrent transactions. Concurrency control maximizes transaction throughput while ensuring data integrity. It uses techniques such as locking to manage concurrent access and prevent issues like lost updates, uncommitted dependencies, and non-repeatable reads.

>[!Note]
> A transaction should be designed in such way that it performs its task in the least amount of time.

## Related Notes