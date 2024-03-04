# ADR-009: Deployability downplayed

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to define the architectural principles for the "MonitorMe" project, a patient monitoring system.

[context link out](/ArchitectureCharacteristics/Characteristics.md#choosing-the-top-7-characteristics)

## Decision:
The decision is to exclude deployability as a critical characteristic. The context specifies that the system will be installed locally, serving as a single solution for a hospital.

## Consequences:
### Pros:
- The chosen decision allows for a more finely tuned system architecture, aligned with the local installation requirements.

### Cons:
- Excluding deployability may pose challenges in migrating the solution to a cloud environment if needed in the future.
