# User-Management Domain


Date: 2021-05-01

## Status
Accepted


## Context
The User-Management domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

User-Management will be split into Expert-Management, Sysops User-Management and Customer-Management components.

## Consequences

**Positive:**

- Functionality split with no overlap (seemingly overlapping functions, e.g. update profile, are on different data sources and structures)
- Scalability managed separately, likely only required for Customer component
- Faults do not bring unrelated functionality down

**Risks:**

- Admin and Manager users will have some differences, which will need to be taken into account in code structure.