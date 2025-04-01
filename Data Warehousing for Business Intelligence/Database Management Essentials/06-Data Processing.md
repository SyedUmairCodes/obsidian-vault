# Data Processing
Parallel and distributed processing are two methods of utilizing multiple computing resources to improve performance and availability, but they differ significantly in their approach and goals.

 - Parallel database processing divides a large task into smaller tasks and distributes these among interconnected computers to improve performance.
 - Distributed processing involves the distribution of tasks and data among computers connected by a network. It focuses on enabling different sites to cooperate in providing access to data. 

Parallel processing focuses on performing a task faster and getting more work done in the same time while distributed processing provide local control of data, reduces communication costs by locating data closer to where it’s used, and improve performance by allowing multiple sites to work concurrently.

## Architectures

**Common Parallel processing architectures:**

- Shared Disk (SD): Each processor has its own memory, but the processors share access to all disks.
- Shared Nothing (SN): Each processor has its own memory and disks. Data must be partitioned among the processors.
- Clustered Disk (CD): Processors in each cluster share all disks, but nothing is shared across clusters.
- Clustered Nothing (CN): Processors in each cluster share no resources, but each cluster can be manipulated to work in parallel.

A distributed database has a component architecture composed of local data managers (LDM) at each site, and a distributed data manager (DDM) that manages global requests. The schema architecture includes a global conceptual schema and local schemas for each site.

## Related Notes