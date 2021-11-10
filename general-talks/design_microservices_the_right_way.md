# Design microservices the right way
## Characteristics of a great architecture
 - delivers quality
 - high perforamance / low cost
 - Support future features naturally. 
 - Scale development teams
 
## Not so great Architecture
 - near term velocity for (trade taking ) future paralysis(takes too long to get things done)

## Myths
## Microservices helps us to choose different programming languages
 -  one language is ok 
## Code Generation is evil 
 - code generation is fine
## Event log must be the source of truth 
 - resources can saved into the database
 - gurantee that events will end up in the event stream. 

## Developers cannot maintain more than 3 services each
 - you can go above and encourage alot of automation to decrease maintenance


## Api Definition
 - api definition must be language agnostic
 - it should feel like one person wrote the api 
 - add automated linters
 - build a process to review your api if it breaks anything.
 ---- reflection dynamically,  code generation 
### Code Generation: Routes
 - Gurantee operations are actually defined
 - User friendly path 
 - consistent naming for methods

### Code Generation: Clients
 - No value writing this all the time 
 
### Code Generation: Mock Client
 - Fast Testing
 - Write unit test and integration test against the mocks 


## - Implementation
 - Should be simple and consistent 

### Database Architecture 
 - Only use the service interface api + events 


### Create cli for common development tasks

### Code generation of Data Access Object

### Test Resource Operations
 - increase confidence

### Standard Health Check all microservices
 - Make sure they have access to access to environement variables
 - Database connection exist



 
 
