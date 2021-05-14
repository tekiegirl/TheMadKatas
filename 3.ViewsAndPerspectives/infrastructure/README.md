# C4 Infrastructure Models

A C4 model is a common set of abstractions to create used to describe the static structure of a software system; these abstractions having four levels: **software system**, **containers**, **components** and **code**. **People** use the software system.

The following diagrams use the standard C4 notation, with the addition of a different colour to highlight a UI Component, as opposed to a back-end component, in our micro front-end ([see ADR: 003 We-will-use-a-Micro-Frontend-architecture](../../4.ADRs/003We-will-use-a-Micro-Frontend-architecture.md)).

## C4 Model Key

![c4Key](../images/c4Key.png)

## Context Diagram (Level 1 - top level)

A **System Context** diagram provides a starting point, showing how the software system in scope fits into the world around it.[^](#expl) 
This diagram shows how the main users of Sysops Squad interact with the system, and the other systems that the Sysops Squad system interacts with.

![ContextDiagram](images/ContextDiagram.png)

------

## Container Diagram (Level 2)

A **Container** diagram zooms into the software system in scope, showing the high-level technical building blocks.[^](#expl)
The following diagram breaks down the Sysops Squad system into groups of related functionality, or domains, and shows how they interact with each other and how the users of the Sysops system interact with the functionality.

![ContainerDiagram](images/ContainerDiagram.png)

------

## Component Diagrams (Level 3)

A **Component** diagram zooms into an individual container, showing the components inside it.[^](#expl)
The following diagrams break down the containers/functionality shown above further, into components which represent individually deployable services ([see ADR: 002 We-will-use-a-Service-Based-backend-architecture](../../4.ADRs/002We-will-use-a-Service-Based-backend-architecture.md)).

### Ticket Management

The following diagram shows the individually deployable services in the Ticket Management domain, and how they interact with each other, users and other domains.

![TicketComponentDiagram](images/TicketComponentDiagram.png)

------

### User Management

The following diagram shows the individually deployable services in the User Management domain, and how they interact with each other, users and other domains.

![UserComponentDiagram](images/UserComponentDiagram.png)

------

### Notification Management

The following diagram shows the individually deployable services in the Notification Management domain, and how they interact with each other, users and other domains.

![NotificationComponentDiagram](images/NotificationComponentDiagram.png)

------

<a id="expl"></a>^explanations from https://c4model.com/

------

back to [Views & Perspectives](../README.md)