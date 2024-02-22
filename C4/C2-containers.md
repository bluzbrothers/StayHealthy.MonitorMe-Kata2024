# Container view (C2)
C2 in the C4 model, referred to as the Container view, delves deeper into the internal components of the system, showcasing the various containers or application modules and their relationships. It provides a detailed breakdown of how the system is structured internally, including the different types of containers such as services, databases, user interfaces, and external interfaces. This view allows stakeholders to understand the internal architecture of the system and how its components interact to fulfill its functionality.
<img src="images/c2.jpg">

## Vital Sign Recorder
Vital Sing Recorder is responsible for:
* storing received raw vital sign sensor data
* forward received data to Kafka streaming platform [ADR-015](/ADR/ADR-015-event-broker-kafka.md)


### Vital Sign Analyzer
Vital Sign Analyzer is responsible for:
* analysing vital signs for anomalies using global set of rules

To avoid unnecessary calls to the time-series database and to allow multi-parameter analysis, we decided in [ADR-019](/ADR/ADR-019-distributed-cache-analyzer.md) that this component would use own internal cache for each sensor and patient, sensors configuration.

In case of detected anomaly, this component pushes new message to alert topic on kafka streaming platform with all details necessary to produce alarm.

The Kafka has been chosen here in order to implement at least 2 ways of delivering alerts:
* by Push notification for mobile phone (see Vital Sign Alert component).
* through the Vital Sign Streamer which streams data to the Nurse station by using local LAN.
This idea implements the most important function in the system: **PROTECT HUMANS LIFE**.

## Component view (C3)
The team opted to create a [C3 component diagram](C3-components.md) for the Vital Sign Analyzer as it represents the most critical and intricate component.

## Vital Sign Alert
Vital Sign Alert component is responsible for sending alerts through configured channels. 

These components listen on the alerts topic and in case of new message pushes notification to mobile phone. [ADR-016](/ADR/ADR-016-separation-of-data-transmission-responsibilities.md)






