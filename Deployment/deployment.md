## Infrastructure sizing
### Throughput calculation 

Average throughput per second per patient:

| Sensor           | Signals per second   |
|------------------|----------------------|
| Heart rate       | 2                    |
| Blood pressure   | 0,000277777777777778 |
| Oxygen level     | 0,2                  |
| Blood sugar      | 0,00833333333333333  |
| Respiration      | 1                    |
| ECG              | 1                    |
| Body temperature | 0,00333333333333333  |
| Sleep status     | 0,00833333333333333  |
| **Total**        | **4,22027777777778** |

If we assume, that maximum patients number is 500 and the single signal can utilize 1kB, than:

| Throughput type | Value     | Total (req/s) | Throughput (MB/s) |
|-----------------|-----------|---------------|-------------------|
| AVERAGE         | 4,2 * 500 | 2100          | 2,1 MB/s          |
| PEAK            | 8 * 500   | 4000          | 4 MB/s            |

This values shows us, that system MUST be ready to process 4000 signals in one second and network must be prepared to transfer at least 4MB/s.

### Estimated database write time utilization.
Based on [following benchmark](https://medium.com/machbase/performance-testing-and-comparison-of-time-series-databases-influxdb-and-machbase-c35b2fa8d91a)
we can assume that:
* Influx DB can save at least 237871 events/s
* In our case, we need to store 4000 events/s, so the storing process shouldn't be longer than **16ms**

### Publishing to Kafka
Based on [AWS benchmark](https://aws.amazon.com/blogs/big-data/best-practices-for-right-sizing-your-apache-kafka-clusters-to-optimize-performance-and-cost/) 

<img src="images/kafka-benchmark.png"> 

considering the machine 16GB RAM, 4CPU and fast SSD disk (equivalent of m5.xlarge) the Kafka needs **4ms** to publish 4MB of data in second.

### LAN throughput
If we assume that the hospital has a 1Gb/s LAN, transmitting 4MB of data should take approximately **32 ms**.

### Recorder
TODO

### Streamer 
TODO


### Final calculation (from sensor to nurse station)

| Step          | Total Time |
|---------------|----------|
| Save tp DB    | 16 ms    |
| Send to Kafka | 5ms      |
| LAN           | 32ms |



# Deployment diagrams

## App on Kubernetes
The picture below shows the proposed deployment diagram.

<img src="images/kubernetes.png" />


In general, considering the critical importance of system availability and performance within our architecture, we have made the strategic decision to deploy Kubernetes on our on-premises infrastructure. Kubernetes offers a solution that aligns with our objectives of maintaining high availability and optimizing performance. 
One of the main benefits of Kubernetes is its advanced auto-scaling capabilities, which enable the system to dynamically adjust resource allocation based on demand fluctuations. This ensures that our application can efficiently handle varying workloads while minimizing resource wastage. 
Additionally, Kubernetes provides built-in mechanisms for achieving high availability, such as automated failover and load balancing, which help to mitigate the risk of downtime and ensure uninterrupted service delivery to our users. 
Overall, by leveraging Kubernetes, we can effectively manage and scale our infrastructure to meet the demands of our growing application while maintaining the highest standards of reliability and performance.

Detailed description:
* Sensors and Nurse station initiates connections to the K8s Ingress controller
* Each Service has defined proper auto-scaling policies (they are treated as an implementation details and doesn't important from architecture perspective)
* At least 2 Pods should be available all the time to keep system availability


**Important note!** The Kafka and databases are currently depicted as part of the Kubernetes deployment; however, it is possible to modify this configuration in subsequent steps to exclude them and instead install them directly on the Virtual Machines. 

## Kubernetes on-premise infrastructure

The diagram below illustrates the Kubernetes details installed on three separate operating systems (three virtual machines).

<img src="images/kubernetes-on-premise.png">

Our recommendation is to organize the hardware with three (or at least two) independent servers to safeguard against hardware failures.

**Important note!** the IT Administrator and Monitoring role is not a part of this architectural proposal, but it should be implemented when system is ready.

