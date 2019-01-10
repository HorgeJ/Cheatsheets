# SQL Server Fundementals: Designing and Manipulating Data

Databses can be:
* Flat: 
* Hierarchical
* Relational

DB is stored in these files:
* mdf - Primary Data File (Data)
* ndf - (optional) Secondary data
* ldf - Transactional Log (logs changes)

### Datatype Catagories
* exact numbers
* Approx. numbers
* Date and Time
* Character Strings
* Binary Strings
* Spatial Data

### Data Types
Everytime you specify a new field, you must assign it a datatype

* Money
* Date and Time
* int
* Char
* Varchar
* Boolean
* Float
* Bit

### Data Integrity
includes:
 * Entity Integrity: uniqeuness of a row
 * Domain Integrity: ex: enforcing no duplicates or other restraints or rules
 * Referential Integrity: refers to a related record connected to another record (foreign key) 
 * User-defined Integrity: any ruled defined per our logic
 
### Constraints
Data Integrity can be enforced using these constraints:
* Primary Key : Not NULL
* Foreign Key : links tables (primary key from another table)
* Unique Key  : ensures index key has unique value and each row is unique 
* Indexes     : used for sorting 
* Triggers    : SQL statements to provide integrity during table modification

### Column Design
A Primary key can be auto generated
Identity Property: Used to auto increment

Can allow NULLS

Can enter default values to ensure consistancy and can be overwritten by a user

### Relationships
Should be mapped out and planned before we even get to creating the database 

Types of relationships 
* one-to-many
* many-to-many: usually resolved by adding an aditional table

