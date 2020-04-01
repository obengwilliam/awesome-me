# Foundation of Data Systems

## Thinking about systems
- Data systems now ecompasses more than traditional databases and includes caches, queues, and message brokers.
- They might have varying ways of both storing and processing data because of their specific use cases but they are still data systems 
- A composite data systems involves combining mutlitple data systems glued together by some application code
- The three common concern among any software system are scalability, maintability and reliability.

 ## Fundamental building blocks of a data intensive application 
  - Store data so an application can find it later(databases)
  - remember the results of an expensive operation to speed up reads(caches)
  - Allow users to search data and filter different ways(search indexes)
  - Send a message to another process to be handled asynchronously(stream processing)
  - Periodically crunch large amount of accumulated data(batch processing)

## Reliability
 - A system is reliable if it does what the customer needs, tolerate the user making mistakes, handles load and data volume well without affecting results, prevents any unauthorized access
 - A fault tolerant system is a system that has anticipated possible faults and can cope with them.
 - A system can not have zero faults so the best you can do is make sure these faults dont become failures
 - Many critical bugs are due to poor error handling.
 - You can deliberately induce faults to see how other components behave
 - Sometimes tolerating is not enough you need to prevent it(Security)

###  Hardware Faults

### Software Faults

###  Human Faults


## Scalability
 - A system will not continue to work forever , there are common reasons for degradation.
 - Scalability can be considered as the ability to cope under increase load
 - The ability to cope under increasing load is just one label, are more general way to understand scalability is to ask that 
     if the system grow under a particular way, can we continue to cope ?

## Describing load
 - Discuss grow questions b4 discusinng how to grow
 - 
 -
 -

## Maintainability
 - Cost of software increases as we continue to keep it running. Ongoing maintenance, involves fixing bugs, adding new features, investigating failures, adapting to new platforms, and modifying it fornwew use cases, repaying technical debt and adding  new features. 
 - A legancy system ... 
 - Design priciples to maintability at a lower cost include: 
    - Operability - `Make it easy for operations team to keep the system running`
    - Simplicity - `Make it easy for new engineers to understand the system`
    - Evolvability - `Make it easy for engineers, to add more features, update existing ones to work with different use cases`
