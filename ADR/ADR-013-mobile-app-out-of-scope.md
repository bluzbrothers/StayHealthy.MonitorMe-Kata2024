# ADR-013: Mobile app out of scope

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to clarify the role of the mobile application in the architectural design for the "MonitorMe" project, a patient monitoring system.

[context link out](/C4/C1-context.md#context-view-c1)

## Decision:
The decision is that the mobile application will not be considered part of the architectural design. Instead, it will receive push notifications and subscribe to a notification system, such as Firebase. The design and development of the mobile application will be handled by a separate team, guided by client requirements.

## Consequences:
### Pros:
- Streamlining the architectural design by excluding the mobile application allows for a clearer focus on core system components.
- Decoupling the mobile application design facilitates independent development, potentially accelerating the overall project timeline.

### Cons:
- Coordination and communication between the teams responsible for the core system and the mobile application may require additional effort.
- Ensuring seamless integration between the core system and the mobile application may pose challenges, especially if the teams operate independently.
- There is a potential risk of misalignment between the architectural decisions made for the core system and the requirements and design choices of the mobile application team.
