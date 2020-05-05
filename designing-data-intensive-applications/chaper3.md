# Storage and Retrieval
So this chapter is a sister to the previous chapter , the idea is just like we looked how we can store data and how we can retrieve
it from the application developers perspective, in this chapter we are doing the same just from the database
perspective.
Now some may wonder why this is important at all, well it important even though you might never have to build your storage
engine because sometimes you have to decide which storage of your choice to choose depending on the kind of 
data you will be storing and retrieving.
For example some storage engines are geared towards analytics and those geared towards transactional workloads.

We will examine to groups of data enginess `log structured` and `page oriented` storage engines.


## Log structured

```
#!/bin/bash

db_set () {
    echo "$1,$2" >> database
}

db_get () {
    grep "^$1," database | sed -e "s/^$1,//" | tail -n 1
```
The above is a simple key value database, which is also and append only/log kind of engine. 
Everything seems pretty much find but while this is a simple implementation of a key value db a normal db might have to worry 
making sure write are fast for large data, handling errors during retrieving and writing, make sure data storage
is handled properly enough to not exceed the storage ... 
