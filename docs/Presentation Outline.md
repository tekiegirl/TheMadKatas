## Sysops Squad
## Redesign and Migration

### A design and plan.

#### The Mad Katas
#### May 2021

---

>Not only is a solution for the current problems with the Sysops Squad system needed, the solution needs to be enacted quickly to save this arm of the Penuntimate Electronics business.

---

## Sysops Squad

> supporting electronic products bought from Penultimate Systems via a network of experts

---

## Problems

---

### Customer
- the wrong expert turns up and cannot fix the item covered by the contract
- the expert never shows up
- the website is unavailable when they need to create a ticket

---

### Expert
- not being able to fix an item as they don't have the skills, embarrasing and a waste of time and fuel
- ticket information not available when needed

---

### Owner
- the brand image of Penultimate Electronics and Sysops Squad are being tranished by these problems
- money is being wasted when the wrong expert turns up
- customers maybe lost to competitors or cancel contracts due to bad service 

---

### Developers
- change is difficult and risky in this large monolith system - whenever a change is made, it takes too long and something else usually breaks.
- Due to reliability issues, the monolithic system frequently “freezes up” or crashes, and we aren't sure why but think it may be the number of customer users.

(could be speech bubbles and people saying)

---

# Tickets are a problem.

---

## Scenarios for Tickets

---

### Customer creates a Ticket
![[ScenarioCustomerCreateTicket.png]]

---

### ## Ticket created for Expert
![[ScenarioTicketCreatedForExpert.png]]

---

### Expert acts on Ticket
![[ScenarioExpertActsOnTicket.png]]

---

## Key Architecture Characteristics
| Characteristic         | Source                                                       |
| ---------------------- | ------------------------------------------------------------ |
| Reliability            | - lost tickets<br />- ticket assigned to wrong expert (incorrect skills) |
| Data Integrity         | - lost tickets<br />- ticket assigned to wrong expert (incorrect skills) |
| Workflow               | - lost tickets<br />- ticket assigned to wrong expert (incorrect skills) |
| Scalability/Elasticity | - system frequently freezes up / crashes<br />- thought to be because of a spike in usage |
| Availability           | - the system is not always available for web-based and call-based ticket management |
| Maintainability        | - change is difficult and risky<br />- change take a long time and usually breaks something else |
| Testability            | - change is difficult and risky<br />- change take a long time and usually breaks something else |

---

![[ArchitecturalCharacteristics.png]]
---

## System Granularity
---

### Tickets
![[TicketComponentDiagram.png]]

#### ADR: we will spearate Ticket Management into an orchestrator, ticket management and ticket assignment.

---

### Users
![[UserComponentDiagram.png]]

#### ADR: we will spearate User Management into an orchestrator, customer management, expert management and Sysops user management.

---

### Notification
![[NotificationComponentDiagram.png]]

#### ADR: we will spearate Notofication Management into an orchestrator, sms management and email management.

---

## Data Store
![[GraphDatabaseDesign.png]]
### ADR: We will use a graph database as a data store for SysOps Squad

---

## Roadmap

---

### First Iteration
![[MigrationFirstIteration.png]]

---

## Deployment
![[Containerisation.png]]
---

## Overall Solution View

---

## Questions?
#### The Mad Katas
#### https://github.com/tekiegirl/TheMadKatas/