# Cloud Service Functions (Connected Devices)

## Lab Module 11

These optional components may be included in your assignment, but are not required. If you choose to implement them, be sure to complete this README and review all the PIOT-CSF-* issues (requirements) listed at [PIOT-INF-11-001 - Lab Module 11](https://github.com/orgs/programming-the-iot/projects/1#column-10488514).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

The implementation described is a process where you integrate a cloud service function (CSF) for handling IoT sensor data with a cloud platform using 
MQTT (Message Queuing Telemetry Transport) protocol. The system is configured to support secure communication with TLS encryption and authorization enabled. This setup is likely part of a broader IoT system where devices (e.g., sensors) send data to a cloud platform. 
Additionally, AWS-specific Lambda functions are used to process this data.

The primary function of this setup is to:

Gather sensor data from Internet of Things devices.
Use MQTT with TLS encryption to safely send this data, making sure that device-to-cloud connectivity is both allowed and secure.
Utilize AWS Lambda functions and cloud service functions (CSF) to process the data. The Lambda function manipulates the incoming data and is used to handle particular message kinds (such as SensorData).


How does your implementation work?

Maven and Python Project Setup:

    First, you create a CSF zip file inside the Python-Components project using Maven. 
    The dependencies and packaging for the Cloud Service Functions (CSF) that you plan to implement on the cloud are managed by Maven.

    Functions of Cloud Services (CSF):

    You make a new Git branch in the python-components project just for Lab Module 11. 
    Because both utilize Python as its programming language, the CSF code can reuse portions of the code from earlier projects (CDA), such as common modules (such data modules or auxiliary functions).
    The CSF code is in charge of managing the data in the cloud environment and interacting with IoT devices.



    Data Communication in the Internet of Things:

    To provide safe communication, the solution combines MQTT with TLS encryption. 
    This protocol is used by the IoT devices (sensors) to transmit their data to the cloud platform. 
    To guard against unwanted access, the data transmission is encrypted.

    Lambda Function on AWS:

    The SensorData packets are particularly processed by an AWS Lambda function. An excellent option for processing data streams in an Internet of Things system is AWS Lambda, a serverless computation service that automatically grows in response to incoming data.
    After listening for incoming sensor data, the Lambda function processes it (storing, analyzing, or transforming it, for example) and performs any necessary actions (saving the data to a database or starting another service, for example).

        Secure Authorization: To guarantee that only authorized users and devices are able to transmit and receive data, TLS encryption and authorization methods manage communication and authorization between the devices, MQTT broker, and cloud service.

In conclusion, the solution establishes a cloud service that links Internet of Things devices, 
uses AWS Lambda functions to safely handle sensor data, and uses MQTT with TLS encryption to provide safe and allowed communication.


### High-Level Design Diagram

Include a simple box diagram that represents your cloud services functionality. It only has to include the cloud-specific components.


### Code Documentation (only applies if you wrote CSF-specific code, otherwise, ignore)

#### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

#### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


#### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Part 01
- Part 02 
- Part 03 

#### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Part 01 
- Part 02 
- Part 03 

EOF.
