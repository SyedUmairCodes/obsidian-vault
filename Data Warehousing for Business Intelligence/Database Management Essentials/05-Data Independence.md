# Data Independence
Data independence refers to the idea that a database should have an identity that is separate from the applications that use it. This separation is crucial because it allows for changes to the database definition without requiring modifications to related applications.

- Data independence ensures that the conceptual meaning of a database is not mixed with its physical implementation or the programs that access it.
- By separating the database definition from applications, database specialists can experiment with performance tuning without impacting computer programs.
- It enables changes to the database structure or implementation without disrupting the applications that rely on the database. 

>[!Note]
>The DBMS uses mappings to transform application requests from the external view to the conceptual schema and then to the internal schema.

## Related Notes