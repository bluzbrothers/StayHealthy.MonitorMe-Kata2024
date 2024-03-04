# ADR-006: Sensor Bounded Context

## Date:
2024-02-21

## Status:
Accepted

## Context:
The "MonitorMe" project, focused on patient monitoring, encountered the need to address the bounded context of sensors after implementing event sourcing.

[context link out]([/EventStorming/EventStorming.md#summary)
## Decision:
Decision is to create a separate bounded context for sensors, responsible for delivering data to the system. In response to a client inquiry, it was clarified that the system does not handle the sensor context. The advantage of this decision is that hardware responsibilities are kept outside the scope of this system. However, a drawback is the lack of a known protocol, necessitating the assumption that data will be streamed to the MonitorMe system.

## Consequences:
### Pros:
- Clear separation of concerns, with hardware responsibilities external to the system.
- Avoidance of direct involvement with sensor context.

### Cons:
- Absence of a defined protocol, requiring the assumption of data streaming to the MonitorMe system.
