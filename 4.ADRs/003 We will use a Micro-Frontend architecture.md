# Micro-Frontend Architecture

Date: 2021-04-29

## Status

Accepted

## Context

The backend architecture decision highlighted a negative consequence, in that the frontend (user interface) would not gain the same benefits of the backend being broken into smaller deployable chunks. If the benefit of replacing the old system piece by piece is to be realised efficiently then the frontend also needs to be replaced piece by piece.

## Decision

The user interface / front end will be architected as a Micro-Frontend, using the BFF (Backends for Frontends) pattern. Key references for this decision were [Micro Frontends @ MartinFowler.com](https://martinfowler.com/articles/micro-frontends.html) and [Pattern: Backends For Frontends](https://samnewman.io/patterns/architectural/bff/).

![micro-front-end](images/micro-front-end.png)

[Figure 2: Each micro frontend is deployed to production independently, from Micro Frontends @ MartinFowler.com]

## Consequences

**Positive:**

- Micro-frontends can be independently maintained and deployed, making it possible to reduce time-to-market.
- The BFF pattern maintains the vertical organisation of responsibility that using a Service-based architecture for the backend also promotes.

**Negative:**

- N/A

**Risks:**

- N/A

**Bonus Features:**

- Supports the need to move to a new system quickly in that micro-frontends can be developed in tandem with backend services/modules and then replace parts of the current front end (be embedded in current website pages) at the same time as the backend is replaced bit by bit.