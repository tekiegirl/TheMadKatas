# Data Store Interface


Date: 2021-05-01

## Status
Accepted


## Context
To achieve a DRY (Don't Repeat Yourself) system all services will need to talk to an interface to the database, rather than implementing database connections in each service (and hence repeating code).

Implementing a service as an interface to the database also has the advantage that it hides the type of data store and schema of the data from the other services in the system. This leads to schema changes only seriously affecting the database interface service, with changes filtering into backwards-compatible changes to the contract between the database interface service and other services. It is even possible to change the format of the database entirely or use polyglot persistence (multiple databases and database types) without any changes needing to be made to an services in the system but the data store interface.

## Decision

We will use a data store interface between other services and the data store for SysOps Squad.

## Consequences

**Positive:**

- Allows the system to be designed following the DRY principle.
- Schema changes only majorly affect the data store interface service.
- The type and number of data stores can be changed without changing any service but the data store interface.

**Risks:**

- Most of the other services in the Sysops system will use this interface service which creates a single point of failure. This can be mitigated by ensuring that availability is managed using containerisation, but internal testing of the interface service will need to be rigorous, along with ensuring all contracts with other services are back-compatible (see [ADR: 010 We-will-ensure-contracts-between-services-are-back-compatible](010We-will-ensure-contracts-between-services-are-back-compatible.md)).
