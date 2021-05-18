# Overall Architecture Style Analysis

## Identified Key Architectural Characteristics

The [key architectural characteristics](../1.ProblemBackground/ArchitectureAnalysis.md) that were identified help us to select and overall architecture style.

- Reliability
- Data Integrity  
- Workflow
- Scalability/Elasticity  
- Availability
- Maintainability  
- Testability

## Architecture Capabilities Comparison

The above characteristics are highlighted below in yellow, along with secondary characteristics of *Fault-Tolerance* (linked to reliability above) and *Agility* (linked to the problems with testing and deploying changes), with reliability and data integrity, above, not included in the matrix below.

![ArchitectureCapabilitiesComparisonOverlay](C:\Users\JRead\OneDrive - Ordnance Survey\Dev\TheMadKatas\2.SolutionBackground\images\ArchitectureCapabilitiesComparisonOverlay.png)

[original comparison matrix from Understand Architecture Styles (and when to use them) presentation, by Mark Richards]

## Architecture Capabilities Analysis

The above matrix gives us three candidates for our architecture:

### Microservices

- Scores highly on all but workflow, but workflow is key to the main area of ticketing in the Sysops System. This would be a big trade-off.
- Requires that the database be split along with each microservice. This would be very complex and another big trade-off.
- Also scores badly on cost and performance. Not key characteristics, but likely to be important to management and lead technologists respectively.
- Elasticity and scalability score highly, and these could be key to solving the freezing problems (although we aren't sure of the real reason).

### Service-Based

- Scores highly on Agility, Fault-Tolerance and Testability, all three important to development of a new system and the problems associated with making updates to the old system.
- Although it apparently scores low on elasticity and scalability, these low scores can be raised by using containerisation and a graph database that is fast and can also be scaled. So this trade-off is mitigated.
- The low score for workflow can also be mitigated by using orchestrator services and queues. So this trade-off is mitigated.

### Event-Driven

- Elasticity and scalability score highly, and these could be key to solving the freezing problems (although we aren't sure of the real reason).
- Fault-tolerance scores highly, but agility has a middling score. A medium trade-off.
- Workflow scores highly, which is important for the system, but testability has a low score. This would be a big trade-off considering the current problems with testing of deployments.

## Conclusion

All three options have trade-offs, but the trade-offs for the Service-Based architecture can be mitigated by using containerisation, a scalable graph database, orchestrator services, and employing queues where needed.

### Decision

ADR: [002 We-will-use-a-Service-Based-backend-architecture](../4.ADRs/002We-will-use-a-Service-Based-backend-architecture.md)

---

back to [Solution Overview](README.md)