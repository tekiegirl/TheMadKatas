# Data Store Format


Date: 2021-05-01

## Status
Accepted


## Context
System requires appropriate database technology which suits the needs around Customer centric views, Product centric and Expert centric views
Business critical functions knowledge base search or matching to right expert will need to be met elegantly.

Non-functional requirements around Availability, Flexibility to change also needs to be considered. 

See [Datastore Solution Overview](../2.SolutionBackground/datastore/README.md) for the analysis.

## Decision

We will use a graph database as a data store for SysOps Squad.

## Consequences

**Positive:**

- Meets all the requirements specified in [Datastore Solution Overview](../2.SolutionBackground/datastore/README.md), some of the most critical being:
  - Fast multi-criteria search via relationship transversal
  - Availability
  - Flexibility to change
  - Efficient recommendation algorithms

**Risks:**

- Likely requires training of current staff on this technology, or employment of staff already skilled

**Bonus Features:**

- Can model the database exactly how things are in the real world, with no joins or trying to fit data into a relational format