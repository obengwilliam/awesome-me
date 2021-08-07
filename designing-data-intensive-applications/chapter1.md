# Foundation of Data Systems
A data intensive application is an application dealing with the challenges around 
 - complexity of it data
 - the speed at which data is coming in
 - the amount of data 

Every application basically does four things
 - store data, so an application or the same application can find it later.
 - Search by keyword or filter in various ways.(Search Indexes)
 - save an expensive operation for use later.(Cache)
 - send messages asynchronously for later processing.(Stream processing)
 - crunch some details from large amount of accumalated data.(Batch processing)

 All of these data systems have become such successful abstractions we hardly have to build anything from scratch
 when building applications. Now, that is not so simple we still have to decide which of this tools to use and which 
 approaches because there is a plethora of these systems. 
 
 The book is simple about the principles and practicalities around these data systems and by knowing them we get to 
 
## Reliable,Scalable and Maintanable Applications

### Thinking about systems
- Data systems now ecompasses more than traditional databases and includes caches, queues, and message brokers.
- They might have varying ways of both storing and processing data because of their specific use cases but they are still data systems 
- A composite data systems involves combining mutlitple data systems glued together by some application code
- The three common concern among the design data system are scalability, maintability and reliability.

 ### Fundamental building blocks of a data intensive application 
  - Store data so an application can find it later(databases)
  - remember the results of an expensive operation to speed up reads(caches)
  - Allow users to search data and filter different ways(search indexes)
  - Send a message to another process to be handled asynchronously(stream processing)
  - Periodically crunch large amount of accumulated data(batch processing)

### Reliability
 - A system is reliable if it does what the customer needs, tolerate the user making mistakes, handles load and data volume well without affecting results, prevents any unauthorized access
 - A fault tolerant system is a system that has anticipated possible faults and can cope with them.
 - A system can not have zero faults so the best you can do is make sure these faults dont become failures
 - Many critical bugs are due to poor error handling.
 - You can deliberately induce faults to see how other components behave
 - Sometimes tolerating is not enough you need to prevent it(Security)

###  Hardware Faults

### Software Faults

###  Human Faults


### Scalability
 - A system will not continue to work forever , there are common reasons for degradation.
 - Scalability can be considered as the ability to cope under increase load
 - The ability to cope under increasing load is just one label, are more general way to understand scalability is to ask that 
     if the system grow under a particular way, can we continue to cope ?

### Describing load
 - Discuss grow questions b4 discusinng how to grow
 - 
 -
 -

### Maintainability
 - Cost of software increases as we continue to keep it running. Ongoing maintenance, involves fixing bugs, adding new features, investigating failures, adapting to new platforms, and modifying it for new use cases, repaying technical debt. 
 - A legacy system is outdated system that no one really likes to work with mostly because it hard to maintain.
- Because of the above we should build systems that will minimize the cost of maintaining it. 
- To do this we will focus Operatability, simplicity , evovalbility/Extensibility/Plasticity.
 - Design priciples to maintability: 
    - Operability - `Make it easy for operations team to keep the system running`
    - Simplicity - `Make it easy for new engineers to understand the system`
    - Evolvability - `Make it easy for engineers, to add more features, update existing ones to work with different use cases`

#### Operability
 It means making routine task easy 
 it means even bad software get to work well for sometime. 
 
 Responsibilities of an operations team:
- Keep track systems and quickly restore them from a bad state.
- Double down on root causes of problems and performance degradation.
- Software should be updated , including security patches.
- Keeping tabs how systems affect each other so a problementic change can be avoided before it causes damage.
- Anticipate future problems before they occur - Capicity planning.
- Set up best practices for deployment, configuration management ....
- Preserving organisation knowledge as people come and go.


 Making routine task easy.
  - provide good default behaviour but also giving administrators the freedom to override those defaults.
  - Self healing but it should easy for administrators to quickly get state when needed. 
  - good documentation
  - dont depend on any machine. It should still work in one new system while the old is under maintenance.
  - provide visibility into runtime behaviour. 
  - provide good support for automation and integration with standard toolss. 
  - should be predictable


#### Evolvability(agility on a data system level)
Systems dont remain the same forever, overtime a data system will be bombarded with new requirements. These requirements can include:
regulatory requirements, growth requirments , unacticpated use cases and problems, user request, new  platforms ... 

 - Practice TDD.(small surface area)
 - Refactoring patterns.(small surface area)

How do increase agility in a large data system.
 - it all relies on building systems that are simple and easy to understand making them easier to modify.


#### Simplicity
Symtoms of a complex system
 - Tight coupling of modules
 - explosion of state spaces
 - tangled dependencies
 - inconsistent naming and terminology
 - hacks aimed at solving performance problems
 
How
 - Having good abstractions that help extract parts of a large system into reusable components.

                 
