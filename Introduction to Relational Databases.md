# Introduction to Relational Databases and SQL

   Man has been keeping track of things since writing and numbers were a thing. We have gone from scratching symbols on leaves and clay 
tablets to keeping billions of lines of information in a seemingly infinite, invisible space. What would take days or weeks to retrieve 
now only takes a matter of seconds.

Databases, in essence, are organized collections of data. Data can be anything about a person, place, thing, or attributes about them. 
If you can describe it, there's data on it. That's why databases are such an asset to businesses, not just large corporations, but all 
businesses can benefit from using databases. 

Business data is often kept about inventory, information about those products, shipping, suppliers, you name it, there's probably a 
database for it. In the real world, databases are used by Google, Facebook, and several big companies to gather and logically store 
information on their clients. Practically every company uses a database of some sort, and to a further extent, SQL. In the case of 
social media companies: SQL would be used to insert, store, and present that data to members, friends and companies. 

## What is SQL?
SQL is a widely used _declarative_ language that lets you access and manipulate databases (DB) through managing and sorting stored content.
It is an ANSI (American National Standards Institute) standard, and one of the oldest languages in existence. There are different versions that are all ANSI compliant. The versions achieve compliancy through having all of the major commands in their design. These
commands are: SELECT, DELETE, INSERT, and WHERE.

## History
In 1970 Dr. E.F. Codd wrote a paper titled, "A Relational Model of Data for Large Shared Data Banks". This inspired Donald D. Chamberlain
and Raymond F. Boyce from IBM to develop SEQUEL (Structured English Query Language) based on the set theory and predicate logic presented in
the paper. Originally called SQUARE (Specifying Queries As Relational Expressions) the language focused on using predicate mathematics and Set theory in order to select 
data from the database.

By the mid-1970s, Chamberlin and Boyce published a paper called "SEQUEL: Structured English Query Language" and began their refinement 
of SQUARE and focused on exploring data retrieval. The vowels of SEQUEL were eventually dropped due to a trademark on the name by Hawker
Siddeley Aircraft Company. And the language quickly became popular due to its declarative nature. Its ease of use and linear notation
made it easier to maintain, unlike procedural languages.

In the 1980s, the American National Standards Institute (ANSI) endorsed SQL as allowed the ISO (International Standards Organization)
to take on SQL as a standard in 1987. 

Several versions of SQL (from SQL89 to SQL92) were developed, but, none have held out as long as SQL92. There have been several attempts
to update the language, usually every three years or so. Even with the revisions not all  vendor language comply with the latest 
standardizations. 

This is because vendors often use different versions of SQL to accommodate specific needs in their DBMS applications. Sometimes standard 
SQL may not function with a particular style argument . Microsoft, for example, employs the Transact-SQL (T-SQL) flavor for SQL Server, 
Access, and Azure; while companies like Oracle use PL-SQL.  There are also versions such as GRE-SQL, SQL Lite, and Post-GRE SQL. 

## #TLDR;

### SQL can:
  - Execute queries against a DB
  - Retrieve records
  - Insert records
  - Update records

### Structured Query Language 
  - Developed in the 1970's making it one of the oldest languages
  - Adopted as a standard by ANSI and ISO standards bodies 
	- Widely used in the industry
  - SQL is declarative, not procedural which means you need to describe what you want, don't specify steps.
	- BasedSet Theory and Predicate Logic/Predicate Calculus and Relational Algebra
  - Some dialects include
    - SQLite
    - MySQL
    - Transact-SQL (focus of this course)
     - Microsoft 
      - Query language for SQL Server (Local) and Azure SQL Database (virtual machine)
       - Can use .NET for CLR functionality within SQL Server
    - Post-GRE
    - PL/SQL
     - Oracle


