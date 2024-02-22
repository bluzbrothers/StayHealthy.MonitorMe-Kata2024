# Use case - data review

## Involved components
![US3_4.png](images%2FUS3_4.png)

## Sequence diagram
![data_review_sequence.jpg](images%2Fdata_review_sequence.jpg)

### Sequence diagram description
The nurse presses the "Review data" button for the given patient on the consolidated screen. 
The consolidated screen sends a request to the Patient and Sensor Register container using the REST API. 
The API call contains the sensor data and the time range to return the data; it may include other data, but these details should be considered as implementation details. 
The "Patient and Sensor Register" container queries the sensor data stored in the time-series database and sends it back to the consolidated screen device for visualization purposes.
