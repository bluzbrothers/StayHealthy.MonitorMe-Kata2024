# ADR-010: Availability is not used for choosing system architecture 

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to determine the system architecture for the "MonitorMe" project, a patient monitoring system.

[context link out](/ArchitectureCharacteristics/Characteristics.md#elasticity)

## Decision:
The decision is to exclude availability as a criterion in the selection of the system architecture. The template does not include availability as a characteristic for consideration. The rationale is that availability should be addressed outside of the system architecture, ensuring it is maintained at the instance level, such as through the duplication of critical instances.

## Consequences:
### Pros:
- The decision allows for a simplified selection process without considering availability at the architectural level.
- Availability can be addressed and ensured through strategies at the application instance level.

### Cons:
- Excluding availability as an architectural criterion may overlook potential architectural optimizations related to ensuring system availability.
