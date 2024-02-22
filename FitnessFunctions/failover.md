# Fitness function to examine if one of the sensor fails

## Going through the data flow
* The Recorder will neither store nor publish data from failed sensors because it won't receive any messages.
* The Streamer will not receive these signals and therefore will not display them. In other words, nothing happens; only some signals are lost, and no data appears on the screen if the situation persists.
* The Analyzer will not receive certain signals, such as heartbeats, which is a critical concern. Let's examine each component individually:
  * The Cache will retain the last signals from the Heartbeat sensor with a timestamp, for example, from 1 hour ago.
  * The Logic Processor can be configured with rules that dictate actions if the data doesn't exist or if it's outdated (too old); in such cases, the rule will not be executed, or an alert will be sent.
  * This approach demonstrates that depending on the configuration of the Logic Processor, the system will remain stable and operational even if some data is missing.
