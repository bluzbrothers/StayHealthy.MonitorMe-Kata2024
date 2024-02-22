# Use case - anomaly detection and alerting
In that scenario, the data is being analyzed, and if an anomaly is detected by applying a set of globally defined rules, an alert is triggered and simultaneously sent to the nurse station's Consolidated Screen and to the medical professionals' smartphones. 

## Involved containers
![US2.png](images%2FUS2.png)

Involved containers:
- Vital Sign Recorder
- Time series database
- Kafka Streaming Platform
- Vital Sign Streamer
- Patient and sensors register
- Patient database

## Sequence diagram
![alerting_sequence.jpg](images%2Falerting_sequence.jpg)

### Description
The sensor data is received by the Vital Sign Recorder from the sensor using a proprietary protocol. The received data is processed in parallel:

- It is stored in the time series database partitioned by sensor ID.
- Simultaneously, it is sent to the Kafka "Vital Sign Topic."

The sensor data from the mentioned topic is then received (pulled) by the Vital Sign Analyzer and analyzed by the globally defined set of rules used to detect anomalies.

In the case of anomaly detection, the alert is pushed to the "Alert" topic on the Kafka platform.

The Vital Signal Alert and Vital Sign Streamer containers subscribe to that topic.

The Vital Signal Alert pulls the message and sends it through a cloud-based push notification service to the medical professionals' smartphones.

The Vital Sign Streamer pulls that message and sends it through a secure socket connection to the consolidated screen in the nurse station.
