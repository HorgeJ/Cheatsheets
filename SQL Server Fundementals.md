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
* Primary Key
* Foreign Key
* Unique Key
* Indexes
* Triggers
