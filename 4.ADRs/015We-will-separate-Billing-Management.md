# Billing-Management Domain


Date: 2021-05-15

## Status
Accepted


## Context
The Billing-Management domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

Billing-Management will be split into Customer Billing (add and update customer billing data) and Payment Processing (process payments using customer billing data and Penultimate Electronics payment system) components.

## Consequences

**Positive:**

- Functionality split with no overlap
- Scalability managed separately for varying usage
- Faults in Customer Billing do not bring down Payment Processing (most important part of billing) functionality

**Risks:**

- Customer billing data is shared, so consistency needs to be taken into account (e.g. billing data could be edited while a payment is being processed). This could be mitigated by preventing edits to customer billing data while a payment is processing (e.g. add property of lockedForProcessing: true to the customer billing data node(s))