# System Data Domain


Date: 2021-05-15

## Status
Accepted


## Context
The System-Data domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

System-Data will not be split into any smaller components as there is no clear reason to do so.

## Consequences

- **Positive:**

  - Easier management of the system-data domain as there is no unnecessary split in functionality.

  **Risks:**

  - All functionality will be within one service and may need to be split in the future if characteristics of the system-data domain change or new ones are identified.