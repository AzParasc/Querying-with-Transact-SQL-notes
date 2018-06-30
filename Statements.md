## What is SQL?
>  SQL is a widely used _declarative_ language that lets you access and manipulate databases (DB) through managing and sorting stored content.
It is an ANSI (American National Standards Institute) standard, and one of the oldest languages in existence. There are different versions that are all ANSI compliant. The versions achieve compliancy through having all major commands in their design. These commands are: SELECT, DELETE, INSERT, and WHERE.

###	TLDR;

**SQL can:**
- Execute queries against a Database
- Retrieve records
- Insert records
- Update records

**Structured Query Language**
- Developed in the 1970's making it one of the oldest languages
- Adopted as a standard by ANSI and ISO standards bodies 
- Widely used in the industry
- SQL is declarative, not procedural which means you need to describe what you want, don't specify steps.
- Based on Set Theory and Predicate Logic/Predicate Calculus and Relational Algebra
- Some dialects include
  - SQLite
  - MySQL
  - Transact-SQL (focus of these notes)
    - Microsoft SQL Server
    - Query language for SQL Server (Local) and Azure SQL Database (virtual machine)
    - Can use .NET for CLR functionality within SQL Server
 - Post-GRE
 - PL/SQL
   - IBM Oracle

## Statement Types
**DML** _Data Manipulation Language_
>  Statements for querying and modifying data

- **SELECT**
- **INSERT**
- **UPDATE**
- **DELETE**

**DDL** _Data Definition Language_
>  Statements for object definitions

- **CREATE**
- **ALTER**
- **DROP**

**DCL** _Data Control Language_
>  Statements for security permissions

- **GRANT**
- **REVOKE**
- **DENY**

**Control of Flow**
>  Allows you to control the flow of execution within code, handle errors, and maintain transactions. Used in programmatic code objects stored procedures, triggers, and statement blocks

- **IF…Else**
- **WHILE**
- **BREAK**
- **CONTINUE**
- **BEGIN…END**

###	Error Handling
- **TRY…CATCH**

###	Transaction Control 
- **BEGIN TRANSACTION**
- **COMMIT TRANSACTION**
- **ROLLBACK TRANSACTION**

### Batch Separators 
> Batch jobs are "powerful" because it enables us to script content, and schedule it to run at a particular time. If we have multiple statements, we will have to separate them, most often with the GO statement \(not specific to SQL\).
 
 - **GO**
  
**Comments**
> Marks T-SQL code as a comment for a block. It is beneficial to "comment out" a line of code that is in the works so that it doesn't accidentally get executed and to document what you are doing in comments. Comments will appear in green.

\-\-comments a single line

\\* comments and entire block of text */

**Aliases**

>  _Nicknames_ a table or column. Handy when using lengthy table or column names.  Mandatory when using concatenated or aggregated columns, derived tables, or self joins.

- **AS**

##	Elements of Statements 

**The SELECT Statement**
-	All statements end with a semicolon \( ; \)
  - A SELECT statement looks like this:

```SQL
SELECT 	Alias.column_name, Alias.int_column
        , COUNT (table_name.column_name2) AS Aliased_Column
FROM	schema_name.table_name AS Alias
WHERE Alias.column_name IN ('this thing', 'that thing', 'something')
      AND Alias.int_column BETWEEN 1 AND 1000
GROUP BY Alias.ColumnName, Alias.int_column, Aliased_Column
```

**SELECT**
  - Select list
  - Defines which columns to return
  - Delimit if necessary

**FROM**
  -	Table/view source
  -	Defines table(s) or view to query
  -	Specify both schema and table names unless expressed otherwise

**WHERE**
  - Search condition
  - Filters rows using a predicate

**GROUP BY**
  -	Groups by list
  -	Arranges rows by groups

**HAVING**
  - Search condition
  - Filters rows using a predicate

**ORDER BY**
  - Order by list
  - Sorts the output



##	Logical Processing Order	

The following is the order in which a **basic** query is **_processed_** or evaluated in SQL Server. Optimizing, helps to understand what goes on under the surface. 

1. **FROM**
2. **WHERE**
3. **GROUP BY**
4. **HAVING**
5. **SELECT**
6. **ORDER BY**



##	Predicates and Operators

T-SQL enforces operator precedence. Used within the WHERE and/or HAVING clause


### Predicates

**IN**  Used to search in a specified list of values

```SQL
WHERE color IN (‘red’, ‘orange’, ‘yellow’)
```

**BETWEEN** Between specified criteria

```SQL
WHERE EmployeeID BETWEEN 000 AND 32
```

**LIKE**  Used to filter for a string

```SQL
WHERE Name LIKE ‘Ste%en’
```

**Wildcards** used within the LIKE predicate to represent missing letters

-	%string      
- string%
- Str%ng
-	\[escape\] 

**Comparison Operators**
- = equal to
- \>greater than
- <	less than
- \>=	greater than and equal to
- <= less than and equal to
- !=	not equal to
- !>	no greater than
- !<	no less than
- <>  not equal

**Logical Operators	**
-	AND
-	OR
-	NOT

**Arithmetic Operators**
- \-
- \*
- /
- %
- \+


