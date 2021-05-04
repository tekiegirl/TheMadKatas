# Ticket-Management Domain


Date: 2021-05-01

## Status
Accepted


## Context
The Ticket-Management domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

Ticket-Management will be split into Ticket Management and Ticket Assignment components.

## Consequences

**Positive:**

- Functionality split with no overlap
- Volatility of code split, so deployment only of changed components
- Scalability managed separately
- Faults do not bring unrelated functionality down

**Negative:**

- Some data is shared, so consistency needs to be taken into account

**Risks:**

- Some data is shared so consistency of the data is important