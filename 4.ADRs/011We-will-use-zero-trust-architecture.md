# Zero Trust Architecture

Date: 2021-05-01

## Status
Accepted


## Context
Zero-trust architecture is the concept of not trusting anything inside the system, as well as outside of the system. It assumes that the system has been hacked or penetrated and checks the validity and authorisation of all actions and requests.

This means that although a malicious actor may gain access to the system they then cannot travers the system laterally and can only access the resource they have gained entry to.

## Decision

We will use zero-trust architecture in the software and infrastructure of the Sysops system, with an authentication domain acting as gatekeeper.

## Consequences

**Positive:**

- Any malicious actor that gains access tot he system cannot then traverse the system laterally and has only gained access to one resource.

**Risks:**

- With all or most of the services in the system using an authentication domain it presents a single point of failure. This can be mitigated by using containerisation to ensure high availability, creating watch-dog systems to check that there are not problems with this domain, and vigorous internal testing before release.
- If services have to poll to check the validity of a request this adds time to the whole transaction. This can be mitigated by sending the request to the authentication domain as soon as it is received and then processing everything that can be done without receiving the authentication confirmation, only sending the response back when authenticated. e.g. a request for data would read the data from the data store and then only send it when authenticated, a write request would only be written once authenticated but a response of 'received' could be sent back to the requesting service before the request is authenticated and the write preformed and a response of 'written' sent when authenticated. Lag would need to be monitored and this decision reviewed if needed.