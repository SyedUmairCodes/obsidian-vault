# Database Architecture
Database architectures can be understood through two main frameworks: The Three Schema Architecture and architectures supporting parallel and distributed processing.

Three Schema Architecture

This architecture, depicted in , was proposed in the mid-1970s as a way to achieve data independence. Data independence means that a database should have an identity separate from the applications (computer programs, forms, and reports) that use it. This separation allows changes to the database definition without affecting related applications. The architecture includes three levels of database description, known as schemas:

●

External Level: This is the user level, where each group of users can have a separate external view (or view) of the database tailored to their specific needs. These views are often application-specific, representing the data required for a particular form or report.

●

Conceptual Level: This level defines the entity types and relationships for the entire database. It represents the logical meaning of the database and can be quite large for a business database.

●

Internal Level: This represents the storage view of the entire database, describing how the data is physically stored. This level defines the files and collections of data on a storage device, such as a hard disk.

The three schema levels ensure data independence through mappings between them. Applications typically access a database using a view. The DBMS transforms an application’s request from the external view to the conceptual schema, and then to the internal schema. Most changes to the conceptual or internal schema do not affect applications because they do not directly use the lower schema levels. The DBMS is responsible for using mappings to make transformations.

The Three Schema Architecture is an official standard of the American National Standards Institute (ANSI). However, the specific details of the standard were never widely adopted. Instead, the standard serves as a guideline about data independence. The spirit of the Three Schema Architecture is widely implemented in third- and fourth-generation DBMSs.

Other Architectures

●

Client-Server Architectures: These architectures divide processing capabilities between a client and a server. The client typically handles the user interface, while the server manages the database. There can be multiple tiers, where the client interacts with a middleware server, which then interacts with a database server. Web services extend these architectures for electronic business commerce.

●

Parallel Database Processing: These architectures utilize tightly-coupled computing resources to improve performance and availability. They can be implemented using shared disk or shared nothing approaches. In shared disk systems, the processors share all disks but nothing is shared across clusters. In shared nothing architectures, processors share no resources, but each cluster works in parallel to perform a task.

●

Distributed Database Processing: This approach allows geographically dispersed computers to cooperate when providing data access. Distributed databases provide local control and reduce communication costs by locating data where it is most frequently used. These architectures can be tightly or loosely integrated, depending on the homogeneity of the local DBMSs.

Cloud-Based Database Architecture

Cloud computing provides a new approach to database management without initial product licensing costs and hosting requirements. Using web-based interfaces, organizations can design and deploy databases with dynamic resource allocation provided by the cloud. The internal details of the cloud are invisible to organizations using the cloud service.

In summary, the Three Schema Architecture provides a framework for data independence through its separation of external, conceptual, and internal views. The other architectures like client-server, parallel, and distributed systems, address performance and access in networked environments. Cloud-based database architectures provide a new approach for managing databases by reducing licensing costs and hosting requirements.