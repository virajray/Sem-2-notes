
- [x]  #DDL ✅ 2024-05-11
- [x]  #DML ✅ 2024-05-11
- [x] Procedural DML ✅ 2024-05-11
- [x] Non-Procedural DML ✅ 2024-05-11
- [x] Physical data independence ✅ 2024-05-11
- [x] Logical data independence ✅ 2024-05-11
- [x] ANSI/SPARC Architecture? ✅ 2024-05-11
- [ ] conceptual schema
- [ ] actors on a database system
- [ ] database constraints

### Database 📚
Database is collection of <font color="#ffff00">related</font> data

### DB Management system
Collection of programs that enables users to create and maintain the database.

### <font color="#92d050">Meta Data ℹ</font>

Data that describe the <font color="#92d050">properties or characteristics of other data</font>.
Metadata allow database designers and users to understand what data exist, what the data mean.

<span style="background:#40a9ff">Data  security</span> : refers to the <font color="#ff0000">protection of data against</font> unauthorized access
<span style="background:#affad1">Data integrity</span> : refers only to the <font color="#ff0000">validity and accuracy of data</font> rather than the act of protecting data


<span style="background:#ff4d4f">DDL</span> is used to define the structure of the database. It includes commands like <font color="#ffff00">CREATE, ALTER, DROP, and TRUNCATE</font>. Here's a brief overview of each:

<span style="background:#ff4d4f">DML</span> is used to manipulate data within the database. It includes commands like <font color="#ffff00">SELECT, INSERT, UPDATE, and DELETE</font>. Here's what they do:


| Aspect         | Procedural DML                                                             | Non-Procedural DML                                              |
| -------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Definition     | Specifies both what data is needed and how to get it.                      | Specifies what data is needed without specifying how to get it. |
| Implementation | Involves writing detailed procedural logic using programming constructs.   | Involves writing declarative queries using SQL.                 |
| Examples       | <font color="#92d050">PL/SQL (Oracle), T-SQL (Microsoft SQL Server)</font> | <font color="#92d050">SQL (Structured Query Language)</font>    |
| Flexibility    | High flexibility, allows detailed control over data manipulation logic.    | Less flexibility, abstracts away implementation details.        |
| Ease of Use    | Requires programming expertise, may be more complex.                       | More intuitive, easier to learn, especially for beginners.      |
| Performance    | May require manual optimization for performance tuning.                    | Allows DBMS optimization for better performance.                |
| Maintenance    | May be more challenging due to detailed procedural code.                   | Typically easier as changes in logic are abstracted away.       |



| Aspect                     | Physical Data Independence                                                                                                                              | Logical Data Independence                                                                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition                 | Ability to modify the <font color="#92d050">physical storage structures</font> <font color="#f79646">without affecting the logical view</font> of data. | Ability to modify the l<font color="#92d050">ogical structure (schema)</font> of the database <font color="#f79646">without affecting the application's access</font> to the data. |
| Focus                      | Concerned with changes to the physical storage mechanisms such as file organization, indexing methods, etc.                                             | Concerned with changes to the logical structure of the database schema such as adding, modifying, or removing tables, columns, etc.                   |
| Example                    | Changing the storage format from one file system to another.                                                                                            | Adding a new table or modifying the existing table structure (e.g., adding or removing columns) without affecting the application's queries.          |
| Importance                 | Allows optimization of storage systems without disrupting applications.                                                                                 | Facilitates changes in database schema design without requiring changes in application code.                                                          |
| Database System Adaptation | More relevant for database administrators and system architects.                                                                                        | More relevant for database designers and developers.                                                                                                  |
| Example of Usage           | Modifying disk storage configurations, changing database server hardware.                                                                               | Adding new entity-relationship mappings, modifying database normalization.                                                                            |
|                            |                                                                                                                                                         |                                                                                                                                                       |


The <font color="#92d050">ANSI/SPARC</font> Architecture, also known as the <font color="#92d050">ANSI/SPARC DBMS Model</font>, is a conceptual framework for designing database management systems (DBMS). It was proposed by the American National Standards Institute (ANSI) and the Standards Planning and Requirements Committee (SPARC) in the late 1970s. The architecture provides a theoretical foundation for understanding, designing, and implementing database systems.

Key components of the ANSI/SPARC Architecture include:

1. **Three-Level Architecture:** The ANSI/SPARC model proposes a three-level architecture, which separates the database system into three distinct levels: external, conceptual, and internal.
    
    - External Level: Represents the individual user's view of the database. It includes user-specific schemas, which define how each user perceives the data.
    - Conceptual Level: Represents the community view of the database. It provides a global, integrated view of the entire database, independent of any specific user's view.
    - Internal Level: Represents the physical storage of the database on the computer system. It includes details such as data structures, storage organization, and access methods.
2. **Data Independence:** The ANSI/SPARC model emphasizes data independence, which is the separation of data descriptions (schemas) from application programs. It distinguishes between two types of data independence:
    
    - Logical Data Independence: The ability to change the conceptual schema without affecting the external schemas or application programs. It allows modifications to the database structure without requiring changes to the applications that use the data.
    - Physical Data Independence: The ability to change the internal schema without affecting the conceptual schema or external schemas. It enables modifications to the physical storage structures without impacting the logical or external views of the data.
3. **Data Abstraction:** The ANSI/SPARC Architecture promotes data abstraction, which hides the complexity of the underlying data structures and operations from the users and applications. It provides a level of abstraction that allows users to interact with the database system without needing to understand the internal details.

