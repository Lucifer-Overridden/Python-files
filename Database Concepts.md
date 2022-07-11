# Database Introduction
- Database is a method to store and manage data electronically
- To overcome the hassles faced in manual record keeping, it is desirable to store and record on a computerised system

## File System
- A file can be understood as a container to store data in a computer, files can be stored on the storage device of a computer system
- Files stored on a computer can be accessed directly and searched for desired data, but to access data of a file through a software one has to write computer programs to access data from files

## Limitations of a file system
- File system becomes difficult to handle when numbers of file increases and volume of data grows
- **Difficulty in access :** Files themselves do not provide any mechanism to retrieve data, data maintained in a file system is accessed through application programs and while writing these programs the developer may not consider all the use cases. Hence sometimes it can be difficult to access these files in thses cases and one has to design a custom application to read this data
- **Data Redundancy :** Redundancy means same data are duplicated in different places (files). Redundancy leads to excess storage use and may cause data inconsistency also.
- **Data Inconsistency :** Data inconsistency occurs when same data maintained in differnt places do not match 
- **Data Isolation :** When the application program has no support for data mapping and leads to data isolation, In such case it is very difficult to write new applications to retrieve data from different files maintained at multiple places, as one has to understand the underlying structure of each file as well
- **Data Dependence :** Data are stored in specific format or structure in a file and if the structure or format itself is changed, all the existing application programs accessing that file also need to be changed, otherwise the programs may not work efficintly and thais is called data dependency
- **Controlled Data Sharing :** There can be different category ot hierarchy of users accessing the files in the systemand ideally not every person should be able to access all the data, and is it a difficult task to enforce this kind of access control in a file system while accessing files through application programs

## Database Management System
- Limitations faced in a file system can be overcome by storing the data in a database where data is logically related. We can organise related data in a database so that it can be managed in an efficient and easy way.
- A database management system is a software that can be used to create and manage databases. DBMS lets users to create a database, store , manage and update/ modify and retrieve data from that databas by users or application programs.
- A database system hides ceertain details about how data are actually stored and maintained. Thus, it provides users with an abstract view of data. A database system has a set of programs through which users or other programs can access, modify and retrieve the stored data
- The DBMS serves as an interface between the database and end users or application programs, retrieving data from a database through a special type of commands is called querying the database and users can modify the structure of database itself through a DBMS

## Key concepts in DBMS

- **Database Schema :** Database Schema is the design of a database, it is the skeleton of the databse that represents the structure , the type of data each column can hold, constraints on the data to be stored, and the relationships among the tables. Databse Schema is also called the visula or logical architecture as it tells us how the data are organised in a database.
- **Data Constraint :** Sometimes we put certain restrictions or limitations on the type of data that can be inserted in one or more columns of the table which is done by specifying one or more constraints on that column while creating the tables
- **Meta-data or data dictionary :** The database schema along with various constraints on the data is stored by DBMS in a databse catalog or dictionary, called meta-data. A meta-data is data about data
-  **Database Instance :** When we define our database structure or schema, state of database is empty. After loading data, the state or snapshot of the database is known as the database instance. We may then retrieve data through queries or manipulate data through updation, modification or deletion. Thus as the database changes so it can have different instances at different interval of time
-  **Query :** A query is a request to database for obtaining information in a desired way. to retrieve or manipulate data, the user needs to write query using a query language 
-  **Data Manipulation :** Modification of the database consists of three operations viz. Insertion, Deletion or Update
-  **Database Engine :** Database engine is the underlying component or set of programs used by a DBMS to create Database and handle various queries for data manipulation and retrieval

## Relational Database Model
In relational model, tables are called relation that store data for different columns. Each table can have multiple columns where each column name should be unique. Thus a teble consists of collection of relationships

It is important to note here that relations in a databse are not independent tables but are associated with each other. If linking attributes are not there in apt relations, it will not be possible to keep the databse in correct state nd retrieve valid info from the database

Each tuple(row ) in a relation (table) corresponds to data of a real world entity

- **Attribute :** Characterstics or parameters for wich data are to be stored in a relation
- **Tuple :** Each row of data in a relation is called a tuple, in a table with n columns  a tuple is a relationship between the n related values
- **Domain :** It is a set of values from which an attribute can take a value in each row. Usuaaly a datatype is used to specify an attribute for a domain
- **Degree :** The number of attributes in a relation is called the degree of the relation
- **Cardinality :** The number of tuples in a relation is called the cardinality of a relation
