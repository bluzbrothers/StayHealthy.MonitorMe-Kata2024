# ADR-018: High Availability Through Automated Instance Duplication

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to address the requirement for high availability in the "MonitorMe" project, a patient monitoring system.

[context link out](/Deployment/Deployment.md#app-on-kubernetes)
## Decision:
The decision is to ensure high availability through the duplication of application instances using an orchestrator such as Kubernetes. Additionally, instances will automatically scale up if any become unavailable, eliminating the need for manual intervention by administrators.

## Consequences:
### Pros:
- High availability is achieved through automated duplication of application instances.
- Instances automatically scale up in the event of unavailability, reducing downtime.
- The decision aligns with modern DevOps practices and enhances system reliability.

### Cons:
- Implementation and maintenance of a container orchestration system may introduce complexities.
- Resource utilization and costs may increase with the duplication of instances.
- The success of automated scaling relies on accurate configuration and monitoring, requiring ongoing attention.
