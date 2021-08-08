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



### Reliability(Continuing to work correctly even when things go wrong)
 - A system is reliable if it does what the customer needs, tolerate the users making mistakes, handles load and data volume well without affecting results, prevents any unauthorized access
 - A fault tolerant system is a system that has anticipated possible faults and can cope with them.
 - A system can not have zero faults so the best you can do is make sure these faults dont become failures
 - Many critical bugs are due to poor error handling.
 - You can deliberately induce faults to see how other components behave.(Netflix Monkey patching)
 - Sometimes tolerating is not enough you need to prevent it(Security)
 
 A fault tolerant/resilient system is any system that anticipates possible faults and tries to cope with it. 
 A fault is refers to somehting wrong that happended to only one components of the system and failure is when the 
 system as a whole stop provides an entire service to a user. 
 
 The goal here is fundamentally to make sure FAULTS dont lead to failures. 
 

####  Hardware Faults
Usually uncorrelated errors in an hardware , for example a disk suddently stops working. 
 - use software tolerant techniques
 - hardware redundancy 

#### Software Faults
 Correlated systematic errors across nodes. 
 Examples
  - unexpected errors that causes an entire instance to crush
  - A runaway process that uses up some shared resource
  - A service that slows down, becomes unresponsive or start returning corrupted responses. 
  - Cascading failures

Common things that can help.
 - process isolation 
 - carefully thinking about assumptions and how systems interact
 - thorough testing
 - process isolation
 - allowing process to crush and restart. 
 - measuring, monitoring
 - analysizing system behaviour in production.

#### Human Errors
  - design systems in a way that minimizes opportunities for error
   -  well designed abstractions, API, admin interfaces
   -  dont se so strict with your interfaces
  - Decopule places where people make the most mistakes from the places where they can cause failures. 
  - Test thorougly at all levels.  Manual test, integration test 
  - Quick recovery for human errors
     - make it fast to rollback
     - roll out new code gradually
     - provide tools to recompute date ?
   - Set up telemetry
   - Good managment practices and training. 

 Sometimes you might to cut corners for various reasons but be very conscious of that action.
 
 

####  Human Faults


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

                 
