# ADR-012: Choosing system architecture event-driven

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to select the architectural style for the "MonitorMe" project, a patient monitoring system.

## Decision:
Based on the evaluation criteria of elasticity, evolvability, and performance, an event-driven architecture is chosen. The decision is supported by a rating of 14 stars according to the selection schema for architectural styles.

## Consequences:
### Pros:
- The chosen event-driven architecture is expected to provide high performance, scalability, and adaptability.
- Event-driven systems often exhibit excellent evolvability, making it easier to incorporate changes and updates.
- The decision aligns with the identified priorities and criteria for the "MonitorMe" project.

### Cons:
- Implementing an event-driven architecture may introduce additional complexity to the system design and development.
- The team needs to ensure proper handling of events, messaging, and potential event-driven pitfalls.
- The success of the decision relies on accurate evaluation criteria and the suitability of the chosen architectural style for the specific needs of the "MonitorMe" project.