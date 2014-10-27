# How to choose the right database

>This might sound obvious, but when it comes to choosing the right database it helps knowing what sort of data you will be
>dealing with in your application, how it will be structured and the amount of data that will be persisted.
>

Answering a few of these simple questions can help you in choosing the ideal database for your project:
- Do you want a hard fixed data structure (fixed schemas, like an accounting sheet)?
- Do you want flexibility in the structure of the data persisted to the your database (schemaless, multi-level nesting)?
- Will you be handling large quantities of data?
- Will you be handling small quantities of data?
- The volatility of your data ()
- Will you need atomicity or not? ([Atomicity](http://en.wikipedia.org/wiki/Atomicity_(database_systems)) is is one of the ACID transaction properties. In an atomic transaction, a series of database operations either all occur, or nothing occurs.)
- How strict are you with invalid data being sent to your database? (Ideally you are very strict and do server side data validation before persisting it to your database)

Consider these few guiding questions and then read on about some of the databases available and the services they provide.

### RDBMS or NoSQL?



> “The first consideration that needs to be made when selecting a database is the characteristics of the data you are looking to leverage. If the data has a simple tabular structure,
>like an accounting spreadsheet, then the relational model could be adequate. Data such as geo-spatial, engineering parts,
>or molecular modeling, on the other hand, tends to be very complex. It may have multiple levels of nesting and the complete
>data model can be complicated. Such data has, in the past, been modeled into relational tables, but has not fit into
>that two-dimensional row-column structure naturally. In similar cases today, one should consider NoSQL databases as an option.  
>Multi-level nesting and hierarchies are very easily represented in the JavaScript Object Notation (JSON) format used
>by some NoSQL products.”
Source: http://www.zdnet.com/rdbms-vs-nosql-how-do-you-pick-7000020803/

The first downside of RDBMS is that not all the facts about the data model are known at design time, so
some flexibility is needed. This presents issues to the RDBMS users. This means that when defining the schema, you must get it
right or if changes need to be made down the line, these must be minimal, because any revision made later can slow or stop
the database form operating. Getting it right might have been true for the "old" world of static schema, but today, where changes need
to be made daily,  a flexible schema is more appropriate.

>As a database grows in size or the number of users multiplies, many RDBMS-based sites suffer serious performance issues.

Today developers require high coding velocity and great agility in the application building process. NoSQL databases have proven to be a
much better choice in that regard, using object focused technologies, such as JSON, for example.

>The learning curve on JSON, for example, is quite fast and programmers can build a prototype in days and weeks. Since many NoSQL offerings
>include an open system, the community provides many productivity tools, another big advantage over single-vendor proprietary
>products. Some organizations, such as MongoDB, even offer free courses online that train employees and interested users
>in how to use the technology.

#### SQL Vs NoSQL - Performance

Performance depends on various factors:
>The overall performance depends to a very large degree on choosing the right implementation for your use case. Key/Value stores are very simple,
>but you can still use them wrong. Column Family Stores are very interesting and also very different from a table based design.
>Due to this it is easy to have a bad data model design and this will kill your performance.

>Besides the obvious factors of disk I/O, network and caching (which you must of course take into consideration), both application performance and
>scalability depend heavily on the data itself; more specifically on the distribution across the database cluster.
Source: http://apmblog.compuware.com/2011/10/05/nosql-or-rdbms-are-we-asking-the-right-questions/

Another issue regarding performance and where SQL falls short is scaling. As a database grows in size and numbers, RDBMS seek solutions
in vertical scaling. This however comes at a great cost, mainly financial, for RDBMS can only scale vertically up to a point where more
limitations creep-up and horizontal scaling is needed. Although many comercial RDBMS products offer horizontal scaling, these come as
bolted-on solutions and can be very expensive and complex to implement.

If you predict you will face such an issue, then NoSQL is to be considered, as many of them were designed specifically to tackle these scale and
performance issues.

Also NoSQL databases, in general, avoid RDBMS functions like multi-table joins that can be the cause of high latency.

>In the new world of big data, NoSQL offers choices of strict to relaxed consistency that need to be looked at on a case-by-case basis.

>Real time analytics for operational data is better suited to a NoSQL setting. Further, in cases where data is brought together
>from many upstream systems to build an application (not just reporting), NoSQL is a must.

#### Learning curve

Another thing to consider is the learning curve for each database type. While both are straightforward enough to learn, as a developer
the learning curve for a NoSQL database might be smaller than having to learn how to use RDBMS's.

### Short list of databases

RDBMS:
- Ingres
- MySQL
- Oracle
- PostegreSQL
- SAP
- SQL Azure
- SQLBase

For a more extended list, click [here](http://en.wikipedia.org/wiki/List_of_relational_database_management_systems)

NoSQL:
- CouchDB
- Couchbase
- LevelDb
- MemcacheDB
- MongoDb
- Riak
- Redis

For a more extended list, click [here](http://en.wikipedia.org/wiki/NoSQL)
