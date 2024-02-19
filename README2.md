# StayHealthy.MonitorMe | Architectural Kata (Winter 2024)

## The BluzBrothers Team
<img src="resources/images/Kata.png" />

* Artur Kruszewski &nbsp;[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/artur-kruszewski/)
* Wojciech Kasa &nbsp;[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/wojciech-kasa-b271b0141/)
* Piotr Filipowicz &nbsp;[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/piotr-filipowicz-402b062a/)
* Sebastian Dąbkowski &nbsp;[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/sebastiandabkowski/)

## Introduction
Welcome to the architectural story of MonitorMe - the O'Reilly Winter 2024 Architectural Kata. MonitorMe is an advanced medical patient monitoring system created by StayHealthy, Inc. As the healthcare industry continues to evolve, the demand for sophisticated monitoring solutions becomes increasingly important. MonitorMe meets this demand by providing a comprehensive platform that continuously monitors patients' vital signs, analyzes data for potential issues, and notifies medical professionals when necessary. This architectural narrative offers a detailed exploration of MonitorMe's system architecture, emphasizing its main components, data flow, communication methods, and adherence to non-functional requirements. By understanding MonitorMe's architecture, stakeholders and the development team can gain insight into how the system functions, its alignment with business objectives, and its potential to improve patient care in healthcare environments. Let's explore the architectural complexities of MonitorMe to reveal its innovative design and capabilities. 


## *MonitorMe* Overview

StayHealthy, Inc. is a large and highly successful medical software company located in San Francisco, California, US. They currently have 2 popular cloud-based SAAS products: MonitorThem and MyMedicalData.
MonitorThem a comprehensive data analytics platform that is used for hospital trend and performance analytics-alert response times, patient health problem analytics, patient recovery analysis, and so on.
MyMedicalData is a comprehensive cloud-based patient medical records system used by doctors, nurses, and other health professionals to record and track a patient's health records with guaranteed partitioning between patient records.
StayHealthy, Inc. is now expanding into the medical monitoring market and is in need of a new medical patient monitoring system for hospitals that monitors a patient's vital signs using proprietary medical monitoring devices built by StayHealthy, Inc.

Upon receiving the [requirements](requirements.md) from the stakeholders, our team proceeded to analyze and distill the information provided. This involved a thorough examination and refinement process to extract the essential elements and key details. 
By conducting this requirements distillation, we aimed to ensure a clear understanding of the project scope and objectives, enabling us to proceed with the development process effectively and efficiently. 
We came up with [distilled requirements](./resources/distilled-requirements.md)