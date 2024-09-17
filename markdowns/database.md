# Database
- Secure, removes redundancy, program-data independence, shares data multi user transactions, adheres to ACID concept, self describing, multiple view support, allows table formation, multi-user environment.
## Backups
- Performed by Relational Database Management System (RDMS) or database manager.
### Full
- All files typically on a preset schedule.
- May need large file support.

### Incremental
- Saves storage.

### Differential
- Requires last full backup.
- Includes last full and last differential backup.
### Virtual
- Uses database to track & maintain data.


## Commands
### Data Definition Language (DDL)
- Consists of SQL commands used to define the schema. 
- Can create modify, delete database structures but not the data.
- Create, alter, drop, truncate

### Data manipulation language (DML)
- Most of SQL commands for data manipulation, controls access to data and database.
- Insert, update, delete, select

### Data control language (DCL)
- Rights, permissions and other controls of the DB system, modify structures of objects.
- Grant, revoke

## Access
- Direct, using SQL commands (terminal ?)
- Programmatic, using a programming language, can do more safely.
- User interface, through a DB program (menu based (web), GUI (displays schema diagrammatically), DBMS, natural language interface, search engine)
- Query, using SELECT statement, included in software like Microsoft Access, Query Builder's GUI is designed for query tasks.
- Query can work with a graphical representation or SQL code. Automatically joins related tables, can query and update, (Chartio Visual SQL, dbForge Query Builder for SQL Server, Active Query Builder, FlySpeed SQL, QueryDbVis Query Builder) 

## Nonrelational
- Means a non-tabular form, and tends to be more flexible than traditional SQL based structures.
- Non-SQL (NoSQL DB)
- Wide range of different data can be stored using specialized formats or frameworks.
- Ideal for storing & combining big & unstructured data.
- MongoDB, Apache Cassandra & HBase, Redis, Couchbase

## Relational
- Rows called records, stores related data with a defined relationship, connects multiple tables of data with unique identifiers.
- Applies to structured data sources with relationship.
- MySQL, IBM DB2, Oracle, SQLite, Postgres, MS-SQL
- A table is 1 or more columns of data.
- Schema is a collection of tables, a db can have more than one.

### Most common types of data stores 
#### Document 
- handles objects, data values,
- Is named string fields in an entity referred to as a document.
- Generally store data in the form of JSON documents.

#### Key-value
- Uses unique key to correct hashing functions.
- Simple lookup functions using value of a range of keys.

#### Column-oriented databases
- Rows & cols divided into column families, with each set of columns consisting of logically-related entities that are generally retrieved as a unit.
#### Graph databases
- Edges (relationships) & nodes (the data).
- Be able to quickly traverse looking at relationships (edges)



## Permissions
- Only a DBA or object owner can provide or remove permissions.
- Public role is automatically assigned to user.

### Database
- Right to execute a specific SQL statement.
- Access second persons's object.
- Control computing resources.
- Does not apply to DBA.

### System
- Right to perform any activity.
- Ability to add or delete columns or rows.

### Object
- Right to perform specific actions.
- Allows users to UPDATE, DELETE, INSERT, or SELECT data.
- Object's owner has permissions for that object.

## Types of data
### Structured
- Tabular data, rows & cols.
- These are relational databases.
- Formed set of data.
### Semi-structured
- Like JSON, also contain graph databases.
### Unstructured
- Not in predefined model or data structure.
- Text heavy files, but may contain numbers and dates.
- Videos, images, audio, sensor data, server & website app logs, social media data, emails, and other types.

## Commands

``` sql
select column 1, column 2, FROM table 1, table 2, WHERE column2='value';

GRANT SELECT, INSERT, UPDATE, DELETE ON employees TO smithj;

REVOKE DELETE ON employees FROM anderson;

DENY DELETE ON employees TO jack;

```

``` python
import pyodbc

conn = pyodbc.connect('Driver={SQL Server};'
    'Server = server_name;'
    'Database = database_name;'
    'Trusted_Connection = yes;')
cursor = conn.cursor()
cursor.execute('SELECT * FROM table_name')

for i in cursor:
    print(i)
```

# Misc
- An uncompressed HD .png ~3.3 MB