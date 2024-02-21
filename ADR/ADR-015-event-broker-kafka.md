# ADR-015: Choosing Kafka as Event Broker for "MonitorMe" Project

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to select a suitable event broker for the "MonitorMe" project, a patient monitoring system, within the chosen event-driven architecture.

## Decision:
The decision is to adopt Apache Kafka as the event broker for efficient event distribution. This choice is driven by its compatibility with the event-driven architecture, providing low latency and high scalability, meeting the project's requirements effectively.

## Consequences:
### Pros:
- Kafka's robust features enhance real-time data processing and contribute to system performance.
- The decision aligns seamlessly with the event-driven architecture, ensuring scalability as the project evolves.
- Kafka's durability and fault-tolerance characteristics provide reliability in event processing.

### Cons:
- Implementation and maintenance complexities may arise compared to simpler event brokers.
- Effective monitoring and management are crucial for ensuring Kafka's optimal operation.
- Integration with Kafka requires careful coordination with other system components, demanding additional consideration.