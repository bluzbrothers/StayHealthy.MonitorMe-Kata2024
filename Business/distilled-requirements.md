### Functional Requirements

Functional requirements are determined based on the input from stakeholders. [requirements](requirements.md).

| #    | Requirement   |                                                                                                                                        
|----|-------------|
| FR1 | **Data Acquisition and Transmission**: <br> - Monitor vital sign data from eight patient-monitoring equipment sources, including heart rate, blood pressure, oxygen level, blood sugar, respiration rate, electrocardiogram (ECG), body temperature, and sleep status. <br> - Ensure timely reception of data from each device according to its transmission rate. <br> - Maintain continuous data transmission and reception, even in the event of device failures. |
| FR2 | **Consolidated Monitoring Screen**: <br> - Display vital signs of up to 20 patients per nurses station. <br> - Rotate between patients every 5 seconds on the consolidated monitoring screen. <br> - Achieve an average response time of 1 second or less for displaying vital signs. |
| FR3 | **Data Recording and Storage**: <br> - Record and store the past 24 hours of all vital sign readings for each patient. <br> - Provide medical professionals with the ability to review historical data, allowing filtering by time range and vital sign. |
| FR4 | **Data Analysis and Alerting**: <br> - Analyze vital signs for abnormalities or threshold breaches for each patient. <br> - Adjust analysis based on the patient's sleep status, detecting trends and thresholds accordingly. <br> - Notify medical professionals via push notifications to the StayHealthy mobile app and nurses station screen in case of potential issues. |
| FR5 | **Holistic Snapshots and Data Upload**: <br> - Enable medical staff to generate holistic snapshots of a patient's vital signs. <br> - Allow uploading of patient snapshots to MyMedicalData through a secure HTTP API call. |
| FR6 | **Scalability and Future Expansion**: <br> - Support integration of additional vital sign monitoring devices in the future. <br> - Ensure scalability to accommodate up to 500 patients per physical MonitorMe instance. |
| FR7 | **System Deployment and Reliability**: <br> - Deploy MonitorMe as an on-premises system at each hospital location. <br> - Ensure system reliability and continuous operation, even during device failures. |
| FR8 | **Data Accuracy and Confidentiality**: <br> - Maintain high accuracy of vital sign data analysis and recording. <br> - Uphold patient confidentiality and data security standards set by StayHealthy, Inc., without the need for compliance with external regulatory requirements (e.g., HIPAA). |
| FR9 | **Adaptability to Change**: <br> - Be adaptable to changes in the healthcare market and requirements as StayHealthy, Inc. gains more insights. |
| FR10 | **Integration**: <br> - Integrate with StayHealthy's comprehensive hardware and software platform, including data stores, databases, and other technical tools and products. |
