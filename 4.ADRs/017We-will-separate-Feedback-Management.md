# Feedback-Management Domain


Date: 2021-05-15

## Status
Accepted


## Context
The Feedback-Management domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

Feedback-Management will be split into Survey Management (assign survey to customer) and Response Management (receive response from customer) components.

## Consequences

**Positive:**

- Functionality split with no overlap
- Scalability managed separately for varying usage (many survey assignments may be needed at once but responses may be received at different times)
- Faults in one component do not bring down the other component

**Risks:**

- Survey and Customer data is shared, so consistency needs to be taken into account. 
  - A survey will always be assigned before a response is received so the assignment workflow should not be affected. 
  - If a Survey is archived after being assigned to a customer then 
    - the customer should still be able to complete the survey OR
    - the process of archiving should require the admin to manually assign a new survey if they survey has not been started