# Event-driven architecture
- complex businesses reflect their complexity in the technical solutions we develop
- the mission is to model the complexity in a way that enables businesses to grow
- starts with a small team then team grows

## Microservices vs Monolith
## Fundamentally different challenges


# Event driven Microservice
- provide streaming of data with history and meaning
- provide an immutable sequence of events
  - understand the purpose and evolution of data
  - interpret the business process
- the ability to provide high volumes of messages to distributed components sustainably in real time
- access to history of data

## Problems of micro services synchronous communication with REST
- inherent coupling
- changes in a service effects the underlying system
- complex web of synchronous calls in hard to track
  - cascading failures
- hinders scalability of the system


# Monolith
- new businesses start with software
- new functionality spawls inside the application
- old and removed functionality leaves a foot-print due to design choices or technical debt

## Modular Monolith
- divided into modules with clear boundaries
- modules should be able to evolve without effecting the other modules
- easy to remove a module
  - dependencies are explicit
  - domain is contained
- How to ensure modularity
  - API for each boundary
- automated tests for explicit dependensdcy validation

## The good thing about Monolith

### Business flow is visible
we can:
- inspect the end to end flow
- find any feature
- see the dependency flow
- see the impact of new development

### No network overhead
- no limited external dependencies
- no need to deal with API or event versioning
- breaking changes can publish in on release
- no need to support two version of an event until consumers
- creates development overhead

### Local Validation
we can:
- locally run the entire environment
- add and validate a feature

in a microservice each service has its own config and dependencies

#### Code Reuse 
- in a microservice you can't share code
- some teams build a custom framework
  - introduces coupling hard to manage
  - reusing code makes it less useful because it needs to deal with every possible use-case
