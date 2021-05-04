# Choosing suitable database technology for the system

Date: 2021-05-04

## Status

Accepted

## Context
System requires appropriate database technology which suits the needs around customer centric views, Product centtric and Expert centric views
Business critical functions knowledge base search or matching to right expert will need to be met elegantly.

Non-functional requirements around Availability, Flexibility to change also needs to be considered.


## Decision
It is agreed the graph databses are more suitable for the use cases identified within the scope of this system. This helps to solve the problems more reliably.




## Consequences

**Positive:**

Graph databases are more suitable for use cases under the scope. They include;

* Multi-criteria Search
* Recomendations from KB search results
* Availability
* Flexibility to change
* Traversing through relationships (Customer->Ticket->Product ..etc)


**Negative:**



**Risks:**



**Bonus Features:**

