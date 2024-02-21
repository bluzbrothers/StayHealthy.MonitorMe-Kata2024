# ADR-017: Centralized Patient Data for Improved Security

## Date:
2024-02-21

## Status:
Accepted

## Context:
The decision is needed to determine the scope of patient data transmission within the "MonitorMe" project, a patient monitoring system.

## Decision:
The decision is that patient data will not be transmitted throughout the entire ecosystem. Information for nursing staff will be sourced exclusively from the patient registration system with sensors. This decision prioritizes data security by centralizing patient information in one location.

## Consequences:
### Pros:
- Enhanced data security by consolidating patient information in a single location.
- Reduces the risk of data duplication or inconsistency across the ecosystem.
- Simplifies data access and retrieval for nursing staff, potentially improving efficiency.

### Cons:
- Limited accessibility to patient data may pose challenges in scenarios where real-time, comprehensive information is required.
- The decision necessitates robust security measures for the centralized patient registration system.
- Integration and synchronization challenges may arise when connecting the patient registration system with other components of the ecosystem.