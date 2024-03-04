# ADR-016: Separation of Data Transmission Responsibilities for "MonitorMe" System

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to define the responsibilities for transmitting data in the "MonitorMe" project, a patient monitoring system.

[context link out](/C4/C2-containers.md#vital-sign-alert)

## Decision:
The decision is to separate the data transmission responsibilities in the system. Alerts will be sent to the mobile application through HTTP, while data for the Nurse Station will be transmitted via a web socket streamer. In the context of prioritizing human life, the unavailability of one data receiver will trigger notifications on the other.

## Consequences:
### Pros:
- Clear separation of responsibilities simplifies the data transmission architecture.
- Utilizing HTTP for mobile alerts and web sockets for Nurse Station enhances efficiency in data delivery.
- Redundancy in alerting mechanisms ensures a fail-safe system for critical notifications.

### Cons:
- Managing two different communication protocols may introduce additional complexity.
- Ensuring consistent data formatting for both HTTP and web socket transmissions requires careful consideration.
- Continuous monitoring and maintenance are essential to guarantee the reliability of both data transmission channels.
