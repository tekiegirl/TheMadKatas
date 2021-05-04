# Data Store Format


Date: 2021-05-01

## Status
Accepted


## Context
The current data store is a relational database, but this is not the only option. Analysis of the options against identified requirements of the data store is required. See [Datastore Solution Overview](../2.SolutionBackground/datastore/README.md) for the analysis.

## Decision

We will use a graph database as a data store for SysOps Squad.

## Consequences

**Positive:**

- Meets all the requirements specified in [Datastore Solution Overview](../2.SolutionBackground/datastore/README.md)

**Risks:**

- Likely requires training of current staff on this technology, or employment of staff already skilled

**Bonus Features:**

- Can model the database exactly how things are in the real world, with no joins or trying to fit data into a relational format