# Blob Storage

Azure Blob Storage provides a scalable and cost-effective solution for storing large amounts of unstructured data in the cloud. The key analogy is a massive digital warehouse where you can store any type of file (images, videos, documents, backups) without worrying about running out of space.

**Use Cases:**

- **Media Sharing Platforms:** Hosting high-resolution photos and videos without compression.
- **Data Backup and Disaster Recovery:** Protecting critical data from loss due to hardware failures or accidental deletions.
- **Archiving:** Storing older files that are not frequently accessed but need to be retained.
- **Static Website Hosting:** Serving static content like images, HTML, and JavaScript files for websites.

**Setting up Blob Storage:**

- **Storage Account:** The fundamental unit for managing Blob Storage. Think of it as your hard drive in the cloud.
- **Containers:** Logical groupings within a storage account used to organize blobs (files).

**Controlling Access to Data:**

- **Public Access:** Allows anyone to access the data. Suitable for publicly distributable content.
- **Private Access (using SAS Tokens):** Provides granular control over access by generating temporary, restricted access links.

**Lifecycle Management:**

- **Tiered Storage:** Move data between Hot (frequently accessed), Cool (less frequently accessed), and Archive (rarely accessed) tiers to optimize storage costs.
- **Automated Deletion:** Set up rules to automatically delete files that haven't been accessed for a specified period.

## Related Notes