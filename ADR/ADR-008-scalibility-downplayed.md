# ADR-008: Scalability has been downplayed

## Date:
2024-02-21

## Status:
Accepted

## Context:
A decision is needed due to the outlined assumptions in the requirements, where nine characteristics have been specified in the characteristics document. The system, named "MonitorMe," is set to be installed on-premises, and additional sensors can be manually integrated by adding new nodes or hardware.
The decision is to prioritize the architectural characteristics outlined in the requirements document. Nine characteristics have been identified:

Availability
Evolvability
Elasticity
Security
Deployability
Fault-tolerance
Performance
Configurability
Scalability

[context link out](/ArchitectureCharacteristics/Characteristics.md#choosing-the-top-7-characteristics)

## Decision:
Scalability has been downplayed. The team has emphasized that all relevant obligations have been specified in the requirements. The system will be installed on-premises, and no significant increase in traffic is anticipated with the addition of new sensors. Manual intervention, such as adding a new node or hardware, is possible for system expansion.



## Consequences:
### Pros:
- The decision allows for a more efficient and tailored architecture to meet specific needs.
- Manual scalability and adaptability for adding new sensors.

### Cons:
- Limitation in easy migration to a cloud-based environment due to the on-premises installation.
