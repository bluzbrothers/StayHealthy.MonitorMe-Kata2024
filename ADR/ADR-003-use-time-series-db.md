# ADR-003: Selection of a Time Series Database
## Date:
2024-02-17

## Status:
Accepted

## Context:
Our project requires the efficient handling and analysis of large volumes of time-stamped data. The nature of this data is predominantly time series, characterized by its sequential order and the critical need for high-performance read/write operations, as well as advanced analytical capabilities. The choice of database technology is pivotal to meet these requirements and ensure the scalability, performance, and reliability of our system.

[context link out](/EventStorming/EventStorming.md#3-backward-validation-and-removal-of-unnecessary-events)

## Decision:
After thorough evaluation of various database technologies, we have decided to select a Time Series Database (TSDB) as our primary data storage solution. This decision was made based on the following considerations:

Performance: TSDBs are optimized for time-stamped data, offering superior performance for time-series data ingestion, querying, and analysis.
Scalability: The selected TSDB provides robust scalability options, both vertically and horizontally, accommodating our expected data growth seamlessly.
Built-in Time Series Functions: It offers extensive built-in functionalities specifically designed for time-series data, such as time-based aggregation, downsampling, and retention policies.
Community and Support: The chosen TSDB has a strong community and comprehensive documentation, ensuring access to support and best practices.
## Consequences:
### PROS:
- Enhanced performance for time-series data operations, ensuring faster data ingestion and query response times.
- Improved scalability to manage increasing volumes of data efficiently without significant degradation in performance.
- Access to specialized time-series functions and analytics, enabling more effective data analysis and insights extraction directly within the database.
- Strong community support and extensive documentation, facilitating easier implementation and troubleshooting.
### CONS:
- Potential learning curve for the development team not familiar with the specific TSDB chosen.
- Possible limitations in integrating with existing systems if they are not compatible with time series databases.
- The need for potential additional investments in infrastructure and training to fully leverage the capabilities of the TSDB.
- Selecting a Time Series Database aligns with our project's requirements for handling time-stamped data efficiently and enables us to build a robust, scalable system. This decision will be continuously reviewed as the project progresses and as new technologies emerge.
