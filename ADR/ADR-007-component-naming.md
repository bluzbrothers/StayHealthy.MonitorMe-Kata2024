# ADR-007: Naming Convention for Components

## Date:
2024-02-21

## Status:
Accepted

## Context:
The "MonitorMe" project, focused on patient monitoring, encountered the need to address four bounded contexts after an event storming session: Recorder, Monitor, Analyzer, and Alert.

## Decision:
The decision is to refine the component naming convention by introducing "Vital Sign" as a prefix, e.g., "Vital Sign Recorder." Additionally, for better clarity of the Monitor's responsibility, its name is changed to "Stremer."

## Consequences:
### Pros:
- Improved understanding of component responsibilities at the system level.
- Enhanced clarity in communicating the purpose of each component.

### Cons:
- No identified drawbacks at this time.