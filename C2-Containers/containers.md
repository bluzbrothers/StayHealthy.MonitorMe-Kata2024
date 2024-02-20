## Level 3 - Container 
### Vital Sign Recorder
Vital Sing Recorder is responsible for:
* storing received raw vital sign sensor data
* forward received data to kafka streaming platform


### Vital Sign Analyzer
Vital Sign Analyzer is responsible for:
* analysing vital signs for anomalies using global set of rules

To avoid unnecessary calls to the time-series database and to allow multi-parameter analysis, we decided in ADR-### that this component would use own internal cache for each sensor and patient, sensors configuration.

In case of detected anomaly, this component pushes new message to alert topic on kafka streaming platform with all details necessary to produce alarm.

### Vital Sign Alert
Vital Sign Alert component is responsible for sending alerts through configured channels. 

This components listens on the alerts topic and in case of new message pushes notification to 






