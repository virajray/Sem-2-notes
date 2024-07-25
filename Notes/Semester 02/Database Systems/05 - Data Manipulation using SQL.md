
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

# <font color="#00c3ff">SELECT</font>
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

### <font color="#00ffab">SELECT DISTINCT</font>
```sql
SELECT DISTINCT Country FROM Customers;
```
එක වගේ value තියන ඩේට නැතුව එකිනෙකට වෙනස් ඩේටා විතරක් පෙන්නනවා

ex: කස්ටමස්ල රටවල් කීයක ඉන්නවද බලාගන්ඩ ඕන නම්. එකම රටේ කස්මස්ල 5ක් ඉන්නවන්ම් ඒ වෙනුවට ඒ රටෙන් එකයි පෙන්නන්නෙ. එතකොට වෙනස් ටික විතරක් බලාගන්ඩ පුලුවන් ඩුප්ලිකේට් නැතුව


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

### <font color="#00c3ff">2. Altering Tables</font>

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

<span style="background:#ff4d4f">Note:</span> query එකේ අගට first කියල දැම්මොත්, table එකේ මුලටම ඒ column එක එනව
ex:
```sql
ALTER TABLE Customers  
ADD Email varchar(255) first;
```
<span style="background:#ff4d4f">Note:</span> query එකේ අගට after කියල දාල ඊට පස්සෙ column එකක නම(<font color="#ffc000">name in this case</font>) දුන්නොත්, ඒ දීපු column එකට(<font color="#ffc000">name</font>) පස්සෙ අපි අලුතින් හදන column එක එනව

```sql
ALTER TABLE Customers  
ADD Email varchar(255) after name;
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

### <font color="#ff6000">3. Deleting Tables</font>
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


## <font color="#00ffab">SQL Constraints</font>

SQL constraints are used to specify rules for the data in a table. 
• Constraints are used to limit the type of data that can go into a table.

##### Different constraints: 
 
- <span style="background:#d2cbff">NOT NULL</span> - Ensures that a column cannot have a NULL value
- <span style="background:#d2cbff">UNIQUE</span> - Ensures that all values in a column are different
- <span style="background:#d2cbff">PRIMARY KEY </span>- A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table
- <span style="background:#d2cbff">FOREIGN KEY</span> - Prevents actions that would destroy links between tables
- <span style="background:#d2cbff">CHECK</span> - Ensures that the values in a column satisfies a specific condition
- <span style="background:#d2cbff">DEFAULT</span> - Sets a default value for a column if no value is specified
- <span style="background:#d2cbff">CREATE INDEX</span> - Used to create and retrieve data from the database very quickly

##### Syntax

```sql
CREATE TABLE _table_name_ (  
    _column1 datatype_ _constraint_,  
    _column2 datatype_ _constraint_,  
    _column3 datatype_ _constraint_,  
    ....  
);
```

# Functions

| Function      | What it do                                                   |
| ------------- | ------------------------------------------------------------ |
| `COUNT()`     | Returns the number of rows that match a specified condition. |
| `SUM()`       | Adds up the values in a numeric column.                      |
| `AVG()`       | Calculates the average value of a numeric column.            |
| `MIN()`       | Returns the smallest value in a set of values.               |
| `MAX()`       | Returns the largest value in a set of values.                |
| `LENGTH()`    | Returns the length of a string.                              |
| floor()       | දශම අයින් කරල ආසන්නම සංක්‍යාවට වටයනව                         |
| `UPPER()`     | Converts a string to uppercase.                              |
| `LOWER()`     | Converts a string to lowercase.                              |
| `ROUND()`     | Rounds a numeric field to the number of decimals specified.  |
| `NOW()`       | Returns the current date and time.                           |
| `COALESCE()`  | Returns the first non-null value in a list.                  |
| `SUBSTRING()` | Extracts a substring from a string.                          |
| `TRIM()`      | Removes leading and trailing spaces from a string.           |
| `CONCAT()`    | Concatenates two or more strings.                            |
| `CAST()`      | Converts a value from one data type to another.              |
| `DATE()`      | Extracts the date part of a date or datetime expression.     |
|               |                                                              |
