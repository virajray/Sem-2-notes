[[Important Shites]] <--- Short note

<font color="#ffc000">constraints</font> 
	ex: age should be above than 0 (age > 0)

#### Components of DBMS Environment

![[Pasted image 20240721001455.png]]

1. Hardware
2. Software
3. Data 
4. Procedurees
5. People

**<span style="background:#b1ffff">Procedures</span>** Instructions and rules that should be applied to the design and use of the database and DBMS.

**<span style="background:#fdbfff">People</span>** Data Administrator (DA), Database Administrator (DBA), 
Database Designers (Logical and Physical), Application Programmers, 
End Users (naive and sophisticated)

**<span style="background:#ff4d4f">Data Abstraction:</span>** A **data model** is used to hide storage details and present the users with a **conceptual view** of the database.


###  3 Level ANSI/SPARC Architecture

1. External level
2. Conceptual level / Logical level
3. Internal / Physical level


#### External level <font color="#ffc000">(many views)</font>
- **User's view of the database**
    - Describes the part of the database that is relevant to the user.
    - The external view includes only the entities, attributes, or relationships in the 'real world' that the user is interested in.
    - Different views have different representations of the same data.

#### Conceptual level / Logical level <font color="#ffc000">(One view)</font>

- Describes what data is stored in the database and the relationships among the data.
- This level contains the logical structure of the entire database. Provides a complete view of the data requirements of the organization that is independent of any storage considerations.

#### Internal / Physical level <font color="#ffc000">(One view)</font>
- Describes how the data is stored in the database. 
- Managed by the operating system under the direction of the DBMS. 
- Consist of items only the OS knows.


#### Data Independence (Contd.) 
• <span style="background:#d3f8b6">Logical Data Independence:</span> The capacity to change the conceptual schema without having to change the external schemas and their application programs. 

• <span style="background:#affad1">Physical Data Independence:</span> The capacity to change the internal schema without having to change the conceptual schema.