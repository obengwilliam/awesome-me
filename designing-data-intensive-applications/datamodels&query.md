
This chapter is mostly about helping you deciding on which data model, data query to choose in your application precisely when making a decision on how to store them.

## Data model
- An application can be considered as layers of data model representations.
- For example as a developer you will initially model ur problem solutions into objects or data structures and an  api that will manipulate these.
- When it comes to storing these data models, you will now consider which database, the developers of these database also 
have to provide a model to represent the data u want to store, which can tables or json in some nosql databases or a grpah model.
- The engineers who built these data storage decided on how to represent your json or tables in terms of bytes in memory or disk or a network. 
The way the DS represents determines how the data can be queried, search or manipulated and processed in various ways. 
- The hardware developer also helps the database developer by providing a way to model the data provided as electric pulses. 




# Why is this so important ?
Because the choice of the data model when storing comes with some set of assumptions which determines how fast you can query your data, how easily you can perform transformations and so on. 
So deciding on the wrong data model for application can have serious consequences.

Another thing is in a more complex application, the data model you choose can affect how different systems can interact with you. The data model serves as an abstraction for other people to interact with you, so it important you consider all the possible assumptions sorrounding it.


# Relational Model and Document Data Model
Relation Models are basically modelled as tables(relations) which individual tuples(rows). This model is widely the mostly
popular and used model of our time.  The main goal of the relation dbs was to hide the internal details around a very intuitive interface.

## Why nosql then if it was all good ?
 - high scalability than relation databases can easily archieve including for large datasets and high write throughput.
 - They were made too commercial they wanted more open sourced versions of dbs
 - Specialized query operations not supported by sql dbs
 - A desire for dynamic and expressive data  instead of the restrictive schema provided by sql dbs.
 
 Inspite of all this reasons, sql dbs are not going anymore since there specific use cases that makes them ideal inspite of all the problems, we have also seen a trend that involves what we now call POLYGLOT persistence. Polyglot persistence encourages you to use many more dbs in ur application instead of just sticking to one by they taking advantage of the different opportunities each db brings. 
 
### Object Relational Mismatch
 
 
 
 
## Quick Summary - Data models and Data query languages
Abstraction is just information hiding: it coverys enough information to give an idea of what is probably going without too many details.

Data abstractions - 
Data model  -  Relatonal Model , Document based Model, Graph based Model
Data Model(Data Storage)- > Data Query(Data Retrieval)

Data Storage
 -  Relational
 -  Document Database
 -  Graph Database 
 
Data Query 
 -  Declarative, imperative, mapReduce





