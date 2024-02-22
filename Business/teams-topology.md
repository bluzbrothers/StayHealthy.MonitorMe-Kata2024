# Team topology
Based on the Team Topologies and the structure of MonitorMe we designed a team composition that consists of two stream-aligned teams and one platform team. Here's how the teams can be structured:

<img src="./images/team-topology.png" />

## Stream-Aligned Teams

## - Team A - Vital Sign Monitoring Team

### Responsibilities:
- Develops and maintains components related to vital sign recording, streaming, and real-time monitoring.
- Implements features for collecting and analyzing patient vital sign data.

### Skills and Expertise:
- Software engineers with expertise in real-time data processing, streaming technologies, and data analysis.
- Domain knowledge in healthcare and medical monitoring systems.

## - Team B - Alerting and Notification Team

### Responsibilities:
- Develops and maintains components responsible for generating and delivering alerts to nurse stations and mobile devices.
- Implements features for detecting anomalies in vital sign data and triggering alerts.
- Implements and maintains features responsible for patient registration process and ensures accurate recording of patient information. 

### Skills and Expertise:
- Software engineers with expertise in event-driven architectures, notification systems, and alerting mechanisms.
- Proficiency in designing fault-tolerant and scalable systems.

## - Platform Team

### Responsibilities:
- Develops and maintains the core platform components shared across the system.
- Provides infrastructure, tooling, and support services for stream-aligned teams.
- Ensures architectural integrity, scalability, and reliability of the overall system.

### Skills and Expertise:
- Software architects with expertise in building distributed systems, microservices architecture, and cloud-native technologies.
- DevOps engineers proficient in automation, deployment, and monitoring of cloud infrastructure.


## Assumptions we made:
- Follow the principles of Conway's Law, ensuring that team structures reflect the system's architecture
- Teams are cross-functional, comprising members with diverse skills necessary for end-to-end delivery of features.
- Team autonomy is encouraged, allowing teams to make decisions independently within their respective domains while aligning with overall system goals.