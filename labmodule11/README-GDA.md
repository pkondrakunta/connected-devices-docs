# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-11-001 - Lab Module 11](https://github.com/orgs/programming-the-iot/projects/1#column-10488514).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

Labmodule11 focuses on connecting our GDA to the cloud. We are using Ubidots as a Cloud Service Provider. We can optionally connect to AWS as well. We use MQTT with TLS encryption to connect to the CSP.

In our tests for this lab module, we generate sensorData that is analyzed in the cloud and an Actuation event is triggered from the cloud to the GDA. 

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/gda-lab-modules-pkondrakunta/tree/labmodule11

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule11_gda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule11/labmodule11_gda.png?raw=true)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Part01, Part02 & Part 03 Unit tests 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Part01, Part02 & Part 03 Integration tests 
- MqttClientConnectorTest.java
- CloudClientConnectorTest.java

EOF.
