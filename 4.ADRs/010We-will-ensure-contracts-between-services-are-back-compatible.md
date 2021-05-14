# Service Contracts


Date: 2021-05-01

## Status
Accepted


## Context
Services within the Sysops system will communicate with each other using contracts. Each service is independently deployable and therefore if a contract is updated by a service communication must still work even if the contract has not been updated yet in another service.

Even if two services are updated at the same time, if they are being run in containers the container manager will not update all versions of that service at the same time and the services must continue to operate normally. This relates to the [non-functional requirement regarding reliability of the system](../1.ProblemBackground/BusinessGoal.md#rely).

## Decision

All changes to contracts between services in the Sysops Squad system will be back-compatible.

## Consequences

**Positive:**

- Increases reliability of the Sysops system.
- Decouples services in the Sysops system further, removing the need to update more than one service at a time or in a certain order.

**Risks:**

- Maintaining back-compatibility may add unnecessary complexity or increase time for maintenance. To mitigate this compatibility will only be maintained for a declared period of time, which will be communicated to teams maintaining services which have contracts that are affected.