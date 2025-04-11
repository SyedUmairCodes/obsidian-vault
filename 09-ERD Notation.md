# ERD Notation and Diagrams

Entity-Relationship Diagrams (ERDs) are a tool for conceptual database design. A popular one is the "Crow's Foot" notation. ERD'S are used to model the structure of data *before* building the actual database. They help visualize the data requirements of a system.

- Entity types are collections of similar things, like people, and objects.
- Attributes are the qualities that an entity has.
- A primary key is an attribute that uniquely identify an entity within an entity type.

## Relationships

- **One-to-One:** An employee is assigned a single role at a time.
- **One-to-Many:** Multiple employees can be in a single department.
- **Many-to-Many:** Multiple employees can access multiple resoruces at work.

>[!Note]
>ERD notation (including Crow's Foot) is *not* strictly standardized. Many variations exist. UML (Unified Modeling Language) has a data modeling component, but hasn't fully replaced traditional ERD notations for database design.

## Related Notes

- [[08-Integrity Rules]]


