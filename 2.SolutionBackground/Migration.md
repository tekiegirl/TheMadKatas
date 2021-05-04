# Migration Overview

The service-based backend and micro frontend design meets the need to fairly quickly migrate and/or fix the current major problems with the Sysops Squad system, due to the severity of the impact on the Penultimate Electronics business and bottom line.

## Example Gradual Migration

### Problem

The ticketing system is not reliable: "Customers are complaining that consultants are never showing up due to lost tickets, and often times the wrong consultant shows up to fix something they know nothing about."

### Migration Process in brief

1. Develop, deploy and test the new Ticket Management 

   a. back end services (which store new data in the new data store and migrate old data from the old data store when it is accessed)

   b. micro front end

   c. data store

2. Embed new Ticket Management front end into current admin and customer front ends, which uses the new back end

3. Point current Expert app to use new Ticket Management back end

4. Repeat the above process for other problem parts of the system and eventually replace the whole system.

------

back to [Solution Overview](README.md)