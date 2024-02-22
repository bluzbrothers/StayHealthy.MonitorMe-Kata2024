# Alerts flow
Ensuring that alerts are promptly delivered to medical professionals is of utmost importance, especially when anomalies are detected. 
To achieve a high level of availability, we have implemented a redundant alert delivery system using two channels:
* **Push notifications:** Alerts are sent directly to medical professionals' mobile devices via an internet connection. This ensures immediate notification and allows for quick response, regardless of their location.
* **Streamer process:** Alerts are also processed by the Streamer and displayed on the Nurse Station within the local infrastructure. This provides an additional layer of redundancy, ensuring that alerts are accessible even if internet connectivity is disrupted.

Our redundant infrastructure, based on Kubernetes, further enhances reliability. All components are duplicated, and Kubernetes agents are installed on separate hardware to minimize single points of failure. Additionally, auto-scaling mechanisms are in place to dynamically adjust resources in response to any incidents or increased demand. These measures collectively provide an assurance of stability, with a near 100% uptime guarantee for the system.