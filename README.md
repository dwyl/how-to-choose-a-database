# How to choose the right database

>This might sound obvious, but when it comes to choosing the right database it helps knowing what sort of data you will be
>dealing with in your application, how it will be structured and the amount of data that will be persisted.
>

Answering a few of these simple questions can help you in choosing the ideal database for your project:
- Do you want a hard fixed data structure (fixed schemas)?
- Do you want flexibility in the structure of the data persisted to the your database (schemaless)?
- Will you be handling large quantities of data?
- Will you be handling small quantities of data?
- Do you need to store your data indefinitely?
- Do you only need to store your data for a limited period of time?
- Will you need atomicity or not?
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
