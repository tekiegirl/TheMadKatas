# Clarifications



The following are clarifications given at the Kata Kick-Off webinar:

- Migration plan / road map is optional
- Don't go too small with services/components - document decisions on this
- Pay attention to data!
- How is visit time determined? Customer gives times when booking.
- Geographical? Only one country at the moment. Don't want to care about the complexity of boarders, etc.
- Technology preference? No. No prejudice. But sensitive to budget and value. Document decision(s) on this.
- Constraints with current tech? No, not specified. Could be a .Net project.
- Gradual approach to migration? Up to us.
- How often is ticket allocation done (for the experts)? On creation of ticket.
- Do we need to identify tech? Only if it can only be done by that tool or if there are significant trade offs. e.g. we can specify sync or async, but not specific tech unless really need an aspect only one tech can provide.
- On-prem, hybrid, cloud? Up to us. Can give multiple options.
- Data is a bounded context - think transactions / CRUD
- Does the system need to be online during migration? No.
- How many customers? Thousands, not hundreds of thousands.
- Volume of incoming requests per day? 10s-100s, not 1000s
- Migration to cloud? If you want.
- Payment is upfront for the subscription, monthly.
- Single IT team supporting current monolith
- Code reuse? Assume we don't need to reuse as it actually slow things down. Slower rate of change means asset is more valuable.
- Same user experience required? No, it is currently not good!
- Specify language? Only if a particular capability is required, as with tech.
- How many experts? Enough to manage workload.
- Can expert deny a ticket? Yes, e.g. unavailable for some reason.
- Prior knowledge in the Knowledge Base - experts consult and update

------

[Home](README.md)