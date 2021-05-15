# Knowledge Domain


Date: 2021-05-01

## Status
Accepted


## Context
The Knowledge-Management domain is responsible for various processes. Granularity analysis is required to decide if this domain needs to be broken down further. See [Architecture Analysis](../1.ProblemBackground/ArchitectureAnalysis.md) for more information.

## Decision

Knowledge-Management will be split into Article Management (create, archive and delete article), Article Retrieval (retrieve and search for article) and Article Updater (edit article content, edit article tags and edit article keywords) components.

## Consequences

**Positive:**

- Functionality split with no overlap
- Scalability managed separately for varying usage
- Faults in creation or editing do not bring article retrieval (most important part of knowledge) functionality down

**Risks:**

- Article is shared, so consistency needs to be taken into account (e.g. article could be deleted/archived while also being edited), though consistency of data in these scenarios is not critical to the business.