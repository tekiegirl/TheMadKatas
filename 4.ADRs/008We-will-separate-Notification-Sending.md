# Notification Domain


Date: 2021-05-01

## Status
Accepted


## Context
The Notification domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

Notification-Sending will be split into SMS, Email and a Notification Orchestrator (Notification Preference)

## Consequences

**Positive:**

- Functionality split with no overlap
- Scalability managed separately
- Faults in SMS and Email do not bring unrelated functionality down

**Risks:**

- SMS and Email depend on the orchestrator and would be taken down by a fault in the orchestrator. This would be mitigated by having multiple instances of the orchestrator (scalability is managed independently) and so faults would be managed by e.g. Kubernetes.

**Bonus Features:**

- If another method of notification were added in the future the SMS and Email components would not need to be updated