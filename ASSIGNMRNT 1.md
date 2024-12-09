# SQL Assignment Week 1


## *What You'll Need*
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).
- MySQL Workbench or another SQL database environment.

---



## *Submission Instructions*
1. Answer every question below and put your responses in a file named `answers.md`
2. Push your completed `answers.md` file to your GitHub repository.
3. Submit the GitHub link for review.

---

## **Assignment Questions**

1. State and Explain the components of a DBMS(Database Management System)

A Database Management System (DBMS) is a software system that allows users to create, manage, and manipulate databases. It provides an efficient way to store, retrieve, and manage data in a structured form. A DBMS consists of several key components that work together to provide data management and ensure data integrity, security, and accessibility. The main components of a DBMS are:

1. Database Engine
Definition: The database engine is the core component of the DBMS. It is responsible for accessing, storing, and processing the data. It manages the physical storage of data and ensures that data is retrieved and updated efficiently.
Functions:
Data storage management (files and data structures).
Query processing and optimization.
Data retrieval and update operations.
Transaction management (ensuring atomicity, consistency, isolation, and durability — ACID properties).
2. Database Schema
Definition: A schema is the logical structure or blueprint of the database, describing how the data is organized and how the relationships among data are managed. It defines the tables, fields, and the relationships between them.
Functions:
Describes the organization of data in the database (e.g., tables, views, and indexes).
Defines constraints like primary keys, foreign keys, and other rules for data integrity.
Specifies the structure and data types of each field in the database.
3. Query Processor
Definition: The query processor interprets and executes the queries issued by users or applications. It translates high-level queries (usually written in SQL) into a series of low-level instructions that the database engine can execute.
Functions:
Parsing the query and checking its syntax.
Query optimization to enhance performance (choosing the most efficient way to execute the query).
Query execution by interacting with the database engine to retrieve or manipulate data.
4. Database Management Interface
Definition: The interface allows users, administrators, or applications to interact with the DBMS. It could be a command-line interface, graphical user interface (GUI), or API (Application Programming Interface).
Functions:
Allows users to enter SQL queries and manage the database (adding, updating, deleting, and retrieving data).
Provides access control, monitoring, and administrative tools.
Enables integration with other software applications.
5. Transaction Management
Definition: This component ensures that database operations are completed successfully and consistently, even in cases of system failure. It handles transactions, ensuring they follow the ACID properties (Atomicity, Consistency, Isolation, Durability).
Functions:
Managing and tracking transactions.
Ensuring data consistency and integrity by handling errors, rollbacks, and recovery from crashes.
Enforcing isolation between concurrent transactions to prevent data anomalies.
6. Storage Manager
Definition: The storage manager is responsible for managing the physical storage of data. It manages how data is stored on disk, the organization of files, and retrieval techniques.
Functions:
Data storage and indexing (e.g., managing files and data structures like B-trees or hash tables).
Buffer management (keeping frequently accessed data in memory).
File organization and space management on storage devices (disk).
7. Security Management
Definition: Security management ensures that the database is protected from unauthorized access and misuse. It controls user permissions and access levels to the data.
Functions:
Authentication of users (verifying user identity).
Authorization to control what operations users can perform on the database (read, write, update, delete).
Encryption of sensitive data to protect it from unauthorized access.
8. Backup and Recovery Management
Definition: This component ensures that data is regularly backed up and can be recovered in case of failure, corruption, or loss.
Functions:
Backup of the entire database or parts of it at regular intervals.
Mechanisms for recovering data from backups in case of data loss or system failure.
Log-based recovery, which allows rollback and recovery of transactions.
9. Data Dictionary (Metadata Repository)
Definition: The data dictionary, also called the metadata repository, stores information about the structure of the database (e.g., tables, columns, data types, constraints, relationships).
Functions:
Maintains metadata that describes the structure, constraints, and relationships within the database.
Provides information about tables, indexes, views, and users.
Assists in query optimization and ensures consistency across the database.


2. A relational database is a type of database that organizes data into tables (also called relations), which are linked to each other based on predefined relationships. These relationships are typically established using primary keys and foreign keys. Data is stored in rows and columns within these tables, where each column represents an attribute of the data, and each row represents a record (or instance) of data.

In a relational database:

Tables store data.
Primary keys uniquely identify each record in a table.
Foreign keys link records in one table to records in another, establishing relationships between the tables.
SQL (Structured Query Language) is used for querying and managing the data.
Examples of Relational Databases:
MySQL

MySQL is an open-source relational database management system (RDBMS) that is widely used in web applications and for storing structured data.
It supports SQL and is known for its speed and reliability.
PostgreSQL

PostgreSQL is another open-source RDBMS that supports advanced SQL features and is highly extensible. It is known for its robustness, ACID compliance, and support for complex queries and transactions.
Oracle Database

Oracle Database is a commercial relational database system used by large enterprises. It is known for its scalability, security, and high performance in handling large-scale databases and complex transactions.
Microsoft SQL Server

Microsoft SQL Server is a relational database management system developed by Microsoft. It is commonly used in business environments, and it supports both SQL and a range of tools for managing and analyzing data.


3. State and Explain three classifications of SQL?

SQL (Structured Query Language) is the standard language used for managing and manipulating relational databases. SQL can be classified into three main categories based on the operations they perform. These classifications are:

1. Data Definition Language (DDL)
Definition: DDL is used to define the structure of the database, including tables, schemas, and relationships. It focuses on database objects and their properties, allowing users to create, alter, and delete them.

Common DDL Commands:

CREATE: Defines a new database object (e.g., a table, index, or view).
Example: CREATE TABLE Employees (ID INT, Name VARCHAR(50), Age INT);
ALTER: Modifies an existing database object, such as adding or removing columns from a table.
Example: ALTER TABLE Employees ADD Salary DECIMAL(10, 2);
DROP: Deletes an existing database object (e.g., a table or index).
Example: DROP TABLE Employees;
TRUNCATE: Removes all records from a table but keeps the structure intact.
Example: TRUNCATE TABLE Employees;
Explanation: DDL operations affect the schema and structure of the database but do not manipulate data itself. They are crucial for defining and managing the physical structure of a database.

2. Data Manipulation Language (DML)
Definition: DML is used for manipulating the data stored in the database. It allows users to perform operations such as inserting, updating, deleting, and querying data.

Common DML Commands:

SELECT: Retrieves data from one or more tables.
Example: SELECT Name, Age FROM Employees;
INSERT: Adds new records (rows) into a table.
Example: INSERT INTO Employees (ID, Name, Age) VALUES (1, 'John Doe', 30);
UPDATE: Modifies existing data in a table.
Example: UPDATE Employees SET Age = 31 WHERE ID = 1;
DELETE: Removes data from a table.
Example: DELETE FROM Employees WHERE ID = 1;
Explanation: DML operations deal with the data in the database and allow users to query, add, modify, and remove data records. They are essential for day-to-day database operations.

3. Data Control Language (DCL)
Definition: DCL is used to control access to data in the database. It includes commands that manage user permissions and access rights, determining who can perform certain operations on the data.

Common DCL Commands:

GRANT: Gives a user specific privileges or rights to perform actions on a database object (e.g., SELECT, INSERT, UPDATE).
Example: GRANT SELECT, INSERT ON Employees TO user1;
REVOKE: Removes specific privileges or rights from a user.
Example: REVOKE INSERT ON Employees FROM user1;
Explanation: DCL commands are essential for database security, as they regulate the permissions for users or roles within the database system. They ensure that only authorized users can perform specific operations on the data.


4. Definition: A Primary Key is a field (or a combination of fields) in a table that uniquely identifies each record (row) in that table. It ensures that every record in the table is unique and cannot be duplicated.

Properties:

Uniqueness: Every value in the primary key column(s) must be unique.
Non-null: A primary key column cannot contain NULL values. Each record must have a value for the primary key.
Single Table: A primary key is defined within a single table and cannot span multiple tables.
Purpose: It is used to uniquely identify records within a table, ensuring there are no duplicates and every row can be uniquely accessed.

Example: In a table Employees, the EmployeeID column can be the primary key since it uniquely identifies each employee.

sql
Copy code
CREATE TABLE Employees (

Definition: A Foreign Key is a field (or a combination of fields) in one table that points to the Primary Key in another table. It establishes a relationship between the two tables and ensures referential integrity.

Properties:

Reference to Primary Key: A foreign key in one table refers to the primary key of another table.
Allows Duplicates: Unlike the primary key, a foreign key column can contain duplicate values. It may have multiple rows with the same foreign key value.
Nullable: Foreign key columns can contain NULL values, meaning a record may or may not have a corresponding entry in the referenced table.
Cross-table Relationship: A foreign key is used to create relationships between two tables (parent-child relationship).
Purpose: The foreign key enforces referential integrity by ensuring that the value in the foreign key column matches a valid primary key value in another table, or it may be NULL.

Example: In a Orders table, the EmployeeID might be a foreign key referencing the EmployeeID primary key in the Employees table.

sql
Copy code



5. What is an Entity-Relationship Diagram?


An Entity-Relationship Diagram (ERD) is a visual representation of the relationships between entities (objects or concepts) in a database. It is used to design and model the structure of a database by illustrating how different entities relate to one another and the attributes associated with each entity.

ERDs are widely used in database design to map out data requirements and serve as a blueprint for constructing a relational database system


6. What are the advantages of relational databases?


Data Integrity and Accuracy
ACID Compliance: Relational databases adhere to ACID properties (Atomicity, Consistency, Isolation, Durability), ensuring that transactions are processed reliably, and data integrity is maintained. This guarantees that data remains accurate, consistent, and isolated during concurrent access.
Referential Integrity: Through primary keys and foreign keys, relational databases enforce referential integrity, ensuring that relationships between tables are consistent and valid.
2. Structured Data Storage
Tables with Rows and Columns: Relational databases organize data in tables that consist of rows and columns. This structure is easy to understand, making it simple to store, retrieve, and manipulate data.
Normalization: Data can be normalized to eliminate redundancy and ensure that data is stored efficiently. This helps in organizing data in a way that minimizes duplication and promotes better consistency.
3. Flexibility in Querying
SQL (Structured Query Language): Relational databases use SQL, a powerful and standardized language, for querying and manipulating data. SQL allows users to perform complex queries, filter, join, and aggregate data efficiently.
Advanced Querying: SQL provides a rich set of commands and operations, such as JOINs, subqueries, and grouping, allowing complex queries to be executed with ease.
4. Data Security
Access Control: Relational databases offer strong security features that allow database administrators to define and enforce user permissions. Role-based access control (RBAC) can restrict users to only the data and operations they are authorized to access.
Encryption: Sensitive data can be encrypted to protect it from unauthorized access, ensuring that confidentiality is maintained.
5. Data Redundancy Reduction
Normalization: By organizing data into separate tables and reducing redundant data, relational databases help in minimizing duplication. This leads to more efficient data storage and prevents the issues associated with data redundancy (like inconsistency).
Efficient Updates: When data is normalized, any update to the data is made in just one location, ensuring consistency and reducing the chances of data anomalies.
6. Consistency and Reliability
Transaction Management: Relational databases ensure consistency even in the event of system crashes or failures by using transaction logs and providing mechanisms for rollback and recovery.
Durability: Once a transaction is committed, the changes are permanent, ensuring that data is reliably stored and accessible.





7. State four types of data type used to store data in tables?
   



 Integer (INT)
Description: The INTEGER data type is used to store whole numbers (both positive and negative) without any decimal points.
Examples: 1, -100, 42
Usage: Often used for numeric identifiers, counts, or quantities.
Example:
sql
Copy code
CREATE TABLE Employees (
    EmployeeID INT,
    Age INT
);
2. Varchar (VARCHAR)
Description: The VARCHAR (Variable Character) data type is used to store variable-length strings of text. It allows the storage of alphanumeric characters, and the length of the string can vary.
Examples: 'John Doe', 'New York', 'ABC123'
Usage: Typically used to store names, addresses, or descriptions.
Example:
sql
Copy code
CREATE TABLE Customers (
    CustomerName VARCHAR(100),
    Email VARCHAR(255)
);
3. Date (DATE)
Description: The DATE data type is used to store date values in the format YYYY-MM-DD. It stores only the date part (year, month, day) and does not include time.
Examples: '2024-12-09', '1990-01-01'
Usage: Used for storing birthdates, order dates, or event dates.
Example:
sql
Copy code
CREATE TABLE Orders (
    OrderID INT,
    OrderDate DATE
);
4. Decimal (DECIMAL)
Description: The DECIMAL (or NUMERIC) data type is used to store fixed-point numbers, including decimals. It allows for precise representation of numbers, which is especially important for financial and monetary data.
Examples: 123.45, -99.99, 50.00
Usage: Commonly used for storing prices, salary figures, or financial amounts.


8. What is the purpose of a database management system (DBMS)?  



Data Organization and Storage:

A DBMS stores data in a structured format (e.g., tables) to facilitate easy access, organization, and modification.
Data Access and Retrieval:

It allows users and applications to query and retrieve data quickly and accurately using query languages like SQL.
Data Manipulation:

Supports operations such as insertion, deletion, and updating of data while maintaining consistency.
Data Security and Integrity:

Provides mechanisms to ensure data accuracy, consistency, and protection against unauthorized access.
Multi-User Access:

Enables multiple users to access and manipulate the database simultaneously without conflicts.
Data Redundancy Minimization:

Reduces duplication by centralizing data storage and using normalization techniques.
Data Backup and Recovery:

Ensures data is backed up regularly and can be recovered in case of system failure or corruption.
Support for Transactions:

Allows for the execution of transactions that follow ACID properties (Atomicity, Consistency, Isolation, Durability) to maintain database reliability.
Scalability and Flexibility:

Supports the growth of data and adapts to changing user and application requirements.
Ease of Data Sharing:

Facilitates data sharing across multiple applications and users through well-defined access mechanis
















*How to edit a [markdownfile](https://www.markdownguide.org/basic-syntax/#headings)*

###  NOTE: You should not fork the repository
