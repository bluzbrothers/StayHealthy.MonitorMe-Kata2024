## Use Case - Making snapshot of patient data

## Involved components
![US3_4.png](images%2FUS3_4.png)

## Sequence diagram
![snapshot_sequence.jpg](images%2Fsnapshot_sequence.jpg)

### Sequence description

The nurse presses the "Create snapshot" button on the consolidated screen. 
The consolidated screen sends a request to the Patient and Sensor Register container using REST API and receives a reply with status 200. 
In the background, the "Patient and Sensor Register" container queries the patient data from the Patient Relational database using sensor configuration assigned to the patient. 
It also queries for sensor data stored in the time-series database. 
The data is then sent to the MyMedicalData service using a secure HTTPS connection.
