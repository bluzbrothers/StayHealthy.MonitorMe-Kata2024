# Use case - Patient monitoring

This use case is about gathering sensor data and streaming it to the nurse consolidated screen.



## Involved components
![US1.jpg](images%2FUS1.jpg)

Involved containers:
- Vital Sign Recorder
- Kafka Streaming Platform
- Vital Sign Streamer
- Patient and sensors register
- Patient database

Here is the corrected version of the text:

The Vital Sign Recorder, Kafka, and Streamer are used to store data in the database for further analysis by medical professionals and to near-realtime monitor the patient's status using the Consolidated Screens in nurse stations. 

The Consolidated screen, during startup/handshaking with the system, requests the list of patient details (the consolidated screen has the ability to display patient data, add/remove monitored patients, show different sensors per patient, and rotate data shown at different intervals) and sends requests to start streaming of the sensor data.

A new Streamer is then created. The Streamer is an object that represents the consolidated screen device on the system side. It contains information about which patients are being monitored, subscribes to the Kafka Streaming Platform to receive the latest Vital Sign Data, and streams it using an encrypted socket connection to the consolidated screen.
## Sequence diagram
![monitoring_sequence.jpg](images%2Fmonitoring_sequence.jpg)

### Sequence diagram description
The sensor data is received by the Vital Sign Recorder from the sensor using a proprietary protocol. The received data is processed in parallel:

- It is stored in the time series database partitioned by sensor ID.
- Simultaneously, it is sent to the Kafka "Vital Sign Topic."

The sensor data from the mentioned topic is then received (pulled) by the Vital Sign Streamer, which subscribes to the sensors assigned to monitored patients. Subsequently, this data is sent to the Consolidated Screen using a secure socket connection.
