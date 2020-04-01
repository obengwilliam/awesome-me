#### Functional Programming
Is based on lambda calculus invented by alonzo church

### Squares of integers
I the java example you can clearly see how i both initialized and mutated where as
the clojure example never has that.

### Imuttability and architecture
Race conditions, deadlocks  and concurrent update problems goes away when variables are no longer mutated.

You cannot have deadlocks without mutable locks

Immutability are pratical if certain nuances are made.


Segregation of Mutability
 - Seprate mutable components into non mutable components.
 The mutable components perform thier task in a pure functional way while the immutable parts communicate to other components
 that are not purely functional

 it is common practice to protect the mutable variables from concurrent updates issues by using or imploring transactional memory strategies



 Event Sourcing
  - Nothing get deleted
  - We keep adding 
  - We process all additions when we have to 
  - We need infinite amount of storage and memory

  This is precisely how source controls works


  
