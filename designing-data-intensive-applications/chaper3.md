# Storage and Retrieval
So this chapter is a sister to the previous chapter , the idea is just like  how we looked at storing  data and how we can retrieve it from the application developers perspective, in this chapter we are doing the same just from the database
perspective.

Now some may wonder why this is important at all, well it is important because that knowledget helps us decide on which storage engine to choose.

For example some storage engines are geared towards analytics while others towards transactional workloads.

We will examine to groups of data enginess/Storage engines `log structured` and `page oriented` storage engines.


## Log structured

```
#!/bin/bash

db_set () {
    echo "$1,$2" >> database
}

db_get () {
    grep "^$1," database | sed -e "s/^$1,//" | tail -n 1
```
The above is a simple key value database, which is also an append only/log kind of engine. 
Everything seems pretty much find but while this is a simple implementation of a key value db a normal db might have to worry 
making sure write are fast for large data, handling errors during retrieving and writing, make sure data storage
is handled properly enough to not exceed the storage and so on. 

### how to improve reads for the above ?
Now to do that we need to create some kind of signpost on how to easily find the key and value we are looking for. This additional data is what we call an index. While an index is all good it also affects writes, because anytime you writes you also need to update the index. 


