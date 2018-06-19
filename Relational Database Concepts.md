# Relational Database Concepts

Each table is designed to contain one type of thing.  Most are normalized with relationships defined between table through unique 
identifiers, or _constraints_ called primary and foreign keys.  Primary and foreign keys are links between tables, and ensures referential integrity.

## Normalization
>Process of reducing redundant data by organization.  This includes creating tables, and establishing relationships between them. 

Most databases are designed to three (3) forms of normalization. The last two aren't used as often, disregarding those two normalization rules may result in a less than perfect database, but shouldn’t effect functionality.
  
### Five Normalization Forms
**(1NF) Eliminate repeating groups**
- Do not use multiple fields in a single table to store similar data. The data is in an entity format, which means the following conditions have been met:
  - Eliminate repeating groups in individual tables
  - Create separate table for each set of related data
  - Identify each set of related data with \[primary key\]
    
**(2NF) Eliminate redundant data**
- Makes sure that each attribute describes the entity. Records should not depend on anything other than a table's primary key, including a compound key if necessary.
- Create separate tables for sets of values that apply to multiple records
- Relate these tables with a \[foreign key\]
  
**(3NF) Eliminate columns that do not depend on a key**
- Checks for transitive dependencies
- Values that are not part of the record's key do not belong in the table
- If contents of a group of fields apply to more than one single record, they go into a separate table
  
**(4NF) Boyce-Codd Normal Form (BCNF)**
- Isolate independent multiple relationships
  
**(5NF) Isolate semantically related multiple relationships**
- rarely considered in practical design

### Referential integrity (RI) 
>A database concept used to ensure that the relationships between database tables remain synchronized during data modifications.

- RI can be used to ensure data is clean. May be helpful in optimizing your database environment and can assist in early detection of errors.
- A combination of Primary Key/Foreign Key \[constraints\] can be used to help enforce referential integrity of your database. In addition to a foreign key referencing a primary key constraint a foreign key can also reference a UNIQUE constraint to help maintain referential integrity.
- \[Triggers\] can also be used to enforce referential integrity, however being that triggers require code, they don't execute as quickly as table properties such as a primary key constraint

## Relational Database Components
**Database Entitiy**
> A material or non-material structure which has its own attributes. An example of database entity could be a simple table that contains a set of data.

Entities are represented as _relations_, or tables in which their attributes are represented as _domains_, or columns.

### Schemas and Object Names

**Schema**
>The skeleton structure, or namespace, that logically groups objects such as tables, views and stored procedures, but doesn't actually contain any data itself. 

It does define how the data is organized and how the relations among them are associated. It formulates all the constraints that are to be applied to the data, and is designed when the database doesn't exist at all. Descriptively, it's the name of the source database that the tables are found in, or the source table that the columns are found in. Once the database is in operation, it is difficult to make any changes to the schema. 

Indicating what schema a column belongs to can also help with disambiguation. If we have joined multiple tables in a query, and two or more tables share the same column heading (ie. CustomerID is shared by both the Customer table and the SalesOrderHeader Table) defining the schema can tell SQL Server exactly which column to display from what table. 

>For example, if we wanted to pull information from the customers table, SalesLT.Customer, SalesLT is the schema the customer table is in. 

The schema may have an alias. When defining the schema in the SELECT statement, and an alias is used, the alias MUST be included in the definition or the query cannot be executed. It's the best practice to include the schema name.

