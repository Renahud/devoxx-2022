---
title: "App modernization"
alias: []
---

Sustaineing and maintaning old applications is hard.

How to send an elephant to the cloud ?

Definitions of modernization by companies :
- containers
- automating to reduce operation costs
- bring workload to the cloud
- ci/CD
- microservices

Reasons for modernization:
- scalability
- reliability
- decrease costs
- security
- customer experience
- employee productivity

Some challenges of migration :
- legacy code cant be changes
	- sometimes we don't even have access to it
- New services depend on data managed by legacy apps
	- data quality might be an issue
	- cannot change the structure to not break legacy code
		- you duplicate but then => data incnsistancies

##Modernizing and ogmenting with low to zero impact on legacy

- **rewrite/replace**
- **Lift&Shift** : modernize the platform / hardware to improve performence / release without touching the application
- Refactor/Augment- extend

## Refactoring strategies

- Data capture
- Event-drivent architecture