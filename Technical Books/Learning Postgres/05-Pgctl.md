# PG_CTL

`pg_ctl` is a command-line utility specifically designed for managing a PostgreSQL instance.  It provides a consistent way to interact with the database regardless of the underlying operating system.  Think of it as a Swiss Army knife for managing your PostgreSQL cluster.

- Starting,stopping, and restarting the cluster.
- Checking the status of the cluster.
- Performing various other administrative tasks.
- Create new clusters.
- Manage primary and standby servers.

`pg_ctl` primarily interacts with the postmaster process, which acts as the central control point for the cluster.  `pg_ctl` sends signals to the postmaster, instructing it to perform specific actions.

## Related Notes

- [[02-PSQL]]
