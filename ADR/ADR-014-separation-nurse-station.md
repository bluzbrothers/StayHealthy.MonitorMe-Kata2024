# ADR-014: Separation of "Nurse Station" Application as External Display Component

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to define the role of the "Nurse Station" application within the architectural design for the "MonitorMe" project, a patient monitoring system.

## Decision:
The decision is that the "Nurse Station" application is not considered a core part of the architectural design. Instead, it is treated as a separate application utilizing the system for data display. The "Nurse Station" application will implement data visualization through a web socket, streaming real-time information.

## Consequences:
### Pros:
- The decision simplifies the architectural design by distinguishing between core components and auxiliary applications.
- Focusing on web socket implementation for data streaming in the "Nurse Station" application allows for specialized development and potential optimization.
- Separating the "Nurse Station" application facilitates independent development and updates without impacting the core system.

### Cons:
- Coordination is necessary to ensure seamless integration and communication between the core system and the "Nurse Station" application.
- There may be challenges in maintaining consistency and alignment between the core system's data format and the requirements of the "Nurse Station" application.
- Additional effort may be required to manage dependencies and potential impacts on the overall system due to changes in the "Nurse Station" application.