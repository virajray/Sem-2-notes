
#### <span style="background:#d3f8b6">basic fundamental SQL commands and their functions:</span>

# DDL

1. <span style="background:#fdbfff">CREATE</span> - Creates new database objects (tables, views, indexes, etc.)
2. <span style="background:#fdbfff">ALTER</span> - Modifies the structure of an existing database object
3. <span style="background:#fdbfff">DROP</span> - Deletes an entire table or other database object
4. <span style="background:#fdbfff">TRUNCATE</span> - Removes all data from a table, but keeps the table structure
5. <span style="background:#fdbfff">COMMENTS</span> - Describes a table or column
6. <span style="background:#fdbfff">LABEL</span> - Defines a title for a table or column

# DML
1. <span style="background:#fdbfff">SELECT</span> - Retrieves data from one or more tables
2. <span style="background:#fdbfff">INSERT</span> - Adds new data into a table
3. <span style="background:#fdbfff">UPDATE</span> - Modifies existing data in a table
4. <span style="background:#fdbfff">DELETE</span> - Removes data from a table

14. <span style="background:#fdbfff">WHERE</span> - Filters data based on specified conditions (used with SELECT, UPDATE, DELETE)
15. <span style="background:#fdbfff">JOIN</span> - Combines rows from two or more tables based on a related column
16. <span style="background:#fdbfff">GROUP BY</span> - Groups rows that have the same values in specified columns
17. <span style="background:#fdbfff">HAVING</span> - Specifies a search condition for a group or aggregate
18. <span style="background:#fdbfff">ORDER BY</span> - Sorts the result set in ascending or descending order

![[Pasted image 20240720110252.png]]

- SQL keywords are NOT case sensitive: `select` is the same as `SELECT`

## <font color="#00c3ff">SELECT</font>
The `SELECT` statement is used to select data from a database.

#### <font color="#92d050">Syntax</font>

```sql
SELECT column1, column2, ...
FROM tablename_;
```

<font color="#ffff00">example:</font>
`SELECT CustomerName, City FROM Customers;`

<font color="#ffff00">example:</font>
Return all the columns from the Customers table:
`SELECT * FROM Customers;`

# <font color="#00c3ff">WHERE</font>
The `WHERE` clause is used to filter records.

Select all customers from Mexico:

```sql
`SELECT * FROM Customers  
`WHERE Country='Mexico';`
```

#### Syntax

```sql
SELECT column1, column2, ...
FROM tablename
WHERE condition_;
```

<font color="#ffff00">example:</font>
Select all customers with a CustomerID greater than 80:
```sql
SELECT * FROM Customers  
WHERE CustomerID > 80;
```

# <font color="#00c3ff">1. Creating Database</font>
##### <font color="#92d050">Syntax</font>
```sql
CREATE DATABASE _databasename_;
```

<font color="#ffff00">example:</font>
```sql
CREATE DATABASE testDB;
```

# <font color="#ff6000">2. Deleting Database</font>
`DROP DATABASE` used to drop an existing SQL database.

##### <font color="#92d050">Syntax</font>
```sql
DROP DATABASE _databasename_;
```

<font color="#ffff00">example:</font>
```sql
DROP DATABASE testDB;
```

# <font color="#ffc000">Working with Tables 💻</font>
### <font color="#00c3ff">1. Creating Tables</font>

`CREATE TABLE` statement is used to create a new table in a database.

##### <font color="#92d050">Syntax</font>

```sql
CREATE TABLE _table_name_ (  
    _column1 datatype_,  
    _column2 datatype_,  
    _column3 datatype_,  
   ....  
);
```

<font color="#ffff00">example:</font>
```SQL
CREATE TABLE Persons (  
    PersonID int,  
    LastName varchar(255),  
    FirstName varchar(255),  
    Address varchar(255),  
    City varchar(255)  
);
```

### 2. Altering Tables

`ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

##### To <font color="#ffff00">add a column in a table</font>, use the following syntax:

```sql
ALTER TABLE _table_name_  
ADD _column_name datatype_;
```

<font color="#ffff00">example:</font>
```sql
ALTER TABLE Customers  
ADD Email varchar(255);
```

##### To <font color="#ff6000">delete a column in a table</font>, use the following syntax
```sql
ALTER TABLE _table_name_  
DROP COLUMN _column_name_;
```
<font color="#ffff00">example:</font>
```sql
ALTER TABLE Customers  
DROP COLUMN Email;
```

##### To <font color="#92d050">rename a column in a table</font>, use the following syntax:
```sql
ALTER TABLE _table_name_  
RENAME COLUMN _old_name_ to _new_name_;
```

### 3. Deleting Tables
 `DROP TABLE` statement is used to drop an existing table in a database.

#### <font color="#00ffab">Syntax</font>

```sql
DROP TABLE _table_name_;
```

<font color="#ffff00">example:</font>
```sql
DROP TABLE Shippers;
```

---
`TRUNCATE TABLE` statement is used to delete the data inside a table, but not the table itself.

#### <font color="#00ffab">Syntax</font>

```sql
TRUNCATE TABLE _table_name_;
```


## SQL Constraints

SQL constraints are used to specify rules for the data in a table. 
• Constraints are used to limit the type of data that can go into a table.

Different constraints: 
• Required Data (<span style="background:#d2cbff">NOT NULL</span>) 
• Validity Checking <span style="background:#d2cbff">(CHECK</span>) 
• Entity Integrity (<span style="background:#d2cbff">PRIMARY KEY</span> & <span style="background:#d2cbff">NOT NULL</span>) 
• Referential Integrity (<span style="background:#d2cbff">FOREIGN KEY</span>) 
• Business Rules (<span style="background:#d2cbff">ASSERTION</span>, <span style="background:#d2cbff">TRIGGER</span>) 
• Consistency (<span style="background:#d2cbff">CASCADE</span>, <span style="background:#d2cbff">RESTRICT</span>, <span style="background:#d2cbff">SET NULL</span>)