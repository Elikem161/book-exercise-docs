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

    You first use Maven to generate a CSF zip file from within the python-components project. 
    Maven handles the dependencies and packaging for the Cloud Service Functions (CSF) that you will deploy on the cloud.

    Cloud Service Functions (CSF):

    You create a new Git branch specifically for Lab Module 11 within the python-components project. 
    The CSF code can reuse parts of the code from previous projects (CDA), such as common modules (e.g., data modules or helper functions), 
    because both share Python as the programming language.
    CSF code is responsible for the communication with IoT devices and handling the data in the cloud environment.

    IoT Data Communication:

    The implementation uses MQTT with TLS encryption to ensure secure communication. 
    The IoT devices (sensors) send their data over this protocol to the cloud platform. 
    The data transmission is encrypted to prevent unauthorized access.

    AWS Lambda Function:

    An AWS Lambda function is specifically created to process the SensorData messages. AWS Lambda is a serverless compute service that 
    automatically scales based on incoming data, 
    making it an ideal choice for processing data streams in an IoT system.
    The Lambda function listens for the incoming sensor data, processes it
     (e.g., stores, analyzes, or transforms the data), and takes necessary actions (e.g., saving the data to a database or triggering another service).

         Secure Authorization:
        The communication and authorization between the devices, MQTT broker, and cloud service are handled with TLS encryption and 
        authorization mechanisms to 
        ensure that only authorized devices and users can send and receive data.

In summary, the implementation creates a cloud service that connects IoT devices, 
securely processes sensor data using AWS Lambda functions, and 
ensures secure and authorized communication using MQTT with TLS encryption.


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
