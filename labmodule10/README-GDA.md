# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-10-001 - Lab Module 10](https://github.com/orgs/programming-the-iot/projects/1#column-10488510).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

By combining the MQTT and CoAP protocols, my implementation aims to improve the Gateway Device Application's (GDA) communication and data processing capabilities. To enable real-time data transfer and remote device control, both protocols must be configured to allow message exchange between devices. In order to make sure the system can effectively manage various Quality of Service (QoS) levels, it also includes performance testing for MQTT message transmission. Additionally, it tests CoAP requests (CON and NON) for dependable, low-latency communication. With support for interaction with MQTT brokers and CoAP servers in both encrypted and unencrypted settings, the objective is to offer safe, effective, and scalable message processing between devices in an Internet of Things system.

How does your implementation work?

Setting up and configuring GDA with MQTT and CoAP clients to carry out communication duties is how the implementation operates. Through MQTT, the CDA and GDA apps are connected, with the GDA functioning as the broker and the CDA as the client. A sequence of timed connect/disconnect cycles and message transfers across various QoS levels (0, 1, 2), both with and without TLS encryption, are used to assess MQTT's performance. Furthermore, the CoAP clients are set up to transmit both confirmed (CON) and non-confirmed (NON) messages in POST or PUT requests. In addition to monitoring response times, the system makes sure that the communication stays within the predetermined reliability and latency standards. In order to provide smooth, safe, and effective device interaction, this configuration is made to offer real-time device monitoring, control, and performance metrics.


### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/Elikem161/java-components/tree/lab10

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

-  SensorData Tests: Verify that sensor data is created, stored, and retrieved correctly.

- ActuatorData Tests: Verify precise actuator handling and state transitions.


- DeviceDataManager Tests: Confirm that the GDA handles events, data flow, and lifecycle management.

- SystemPerformanceData Tests: Verify the gathering and processing of CPU and memory use statistics.

- RedisPersistenceAdapter Tests: Examine the functionality of data retrieval and persistence.



### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Sensor-Actuator Interaction: Use sensor input and actuator response validation to replicate real-world situations.

-  CoapServerAdapter Tests: Verify the communication and data exchange capabilities of CoAP server endpoints.

- MQTT Client-Server Interaction: Examine MQTT communications for actuator commands and sensor changes.

- Persistence Layer Integration: Make sure that data processing and persistence technologies are seamlessly integrated.

- Finish the GDA Lifecycle Test: Examine all aspects of functioning, including shutdown, data flow, and startup.
 

EOF.
