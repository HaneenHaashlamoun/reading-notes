# Mongo and Mongoose

![sql](https://blog.couchbase.com/wp-content/uploads/2017/04/nosql-vs-sql-overview-1.png)

**SQL vs NoSQL Database Differences Explained with few Example DB:**

| SQL      | NoSQL |
| ----------- | ----------- |
| SQL databases are primarily called as Relational Databases (RDBMS) | NoSQL database are primarily called as non-relational or distributed database. |
| SQL databases are table based databases | NoSQL databases are document based, key-value pairs, graph databases or wide-column stores |
| SQL databases are vertically scalable  | NoSQL databases are horizontally scalable |
| SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful | NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language) |
| we can classify SQL databases as either open-source or close-sourced from commercial vendors | NoSQL databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases. |


![sql](https://www.scylladb.com/wp-content/uploads/differences-between-sql-databases-and-nosql-databases.png)

## What kind of data is a good fit for an SQL database?
SQL databases are good fit for the complex query intensive environment.
For the type of data to be stored: SQL databases are not best fit for hierarchical data storage.

### Give a real world example.
Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application

## What kind of data is a good fit a NoSQL database?
NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

### Give a real world example.
Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks.

## Which type of database is best for hierarchical data storage?
NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data.

 ## Which type of database is best for scalability?
 In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.

 ------------------------------

 # What does SQL stand for?
 SQL (pronounced "ess-que-el") stands for Structured Query Language. SQL is used to communicate with a database. According to ANSI (American National Standards Institute), it is the standard language for relational database management systems.

## What is a relational database?
A relational database is a digital database based on the relational model of data, as proposed by E. F. Codd in 1970. A system used to maintain relational databases is a relational database management system. Many relational database systems have an option of using the SQL for querying and maintaining the database.

## What type of structure does a relational database work with?
The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure.

## What is a ‘schema’?
The database schema is its structure described in a formal language supported by the database management system. The term "schema" refers to the organization of data as a blueprint of how the database is constructed.

## What is a NoSQL database?
NoSQL databases (aka "not only SQL") are non tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads.

## Howo does it work?
NoSQL databases (aka "not only SQL") are non tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. ... They provide flexible schemas and scale easily with large amounts of data and high user loads.

## What is inside of a Mongo database?
MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

## Which is more flexible - SQL or MongoDB? and why.
While MongoDB is more flexible and ensures high and diverse data availability, a SQL Database operates with the ACID (Atomicity, Consistency, Isolation, and Durability) properties and ensures greater reliability of transactions.

## What is the disadvantage of a NoSQL database?
Disadvantages. NoSQL databases don't have the reliability functions which Relational Databases have (basically don't support ACID). This also means that NoSQL databases offer consistency in performance and scalability.

![infographic](https://miro.medium.com/max/2000/1*SbI8FV6rKx2i3mHEVk-GGw.jpeg)