# ADR-005: Patient Registration Out of Scope

## Date:
2024-02-21

## Status:
Accepted

## Context:
During the event storming session, a business need emerged for patient registration and linking sensors to patients. The decision is to keep this functionality as a supporting sub-domain. 

[context link out](/EventStorming/EventStorming.md#summary)

## Decision:
The decision is Patient registration is a supporting sub-domain. It will be a part of the system, but we won't be focusing on it

## Consequences:
### Pros:
- Seamless alignment with an existing solution.
- Avoidance of implementing additional features within the project scope.

### Cons:
- The need for the system to adapt to an external solution.
