# Hibernate

Hibernate is a framework for ORM (Object Relational Mapping) developed in Java and .Net. The objective is map the **traditional relational database** to **application object model** using XML files or annotations. 

With the Hibernate the developer don't need to care about the SQL implementations, just to the application object model. When a new object should be added, Hibernate will take care of SQL script to add it on database, it is an amazing abstraction for developers.

Let's take a look in the traditional Java database connectivity

### JDBC (Java Database Connectivity)

The JDBC provides APIs to connect Java programs to relational databases as Oracle, DB2, MySQL, etc. Using JDBC you talk with database tables/objects using SQL statements. Let's see another approach, using object relational mapping

### ORM (Object Relational Mapping)

The relational database model is not compatible with object oriented model systems, the objects in the application layer is not directly compatible to relational databases tables and relationships, then the costs and effort to implement the communication between them are high, at leats in complex applications.

Take a look below some mismatchs betweem ORM and Relationa Database:

| Point | Description |
| :---  | :--- |
| Granularity | The number of java objects may be not compatible with the number of tables |
| Inherintance | Java objects has inheritance, but relational tables do not have |
| Identity | Java objects have its owned ID, tables can have customized/composed ids |

There are others...

ORM technique hides SQL implementations and create a mapping between these two words and will manage the transactions automatically.

There are many ORM options as:

* Enterprise JavaBeans
* Java Data Objects
* Spring DAO
* Hibernate
* etc

### Architecture

![](../images/hibernate.png)
