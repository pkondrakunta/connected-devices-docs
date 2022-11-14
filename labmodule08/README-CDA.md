# Constrained Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-08-001 - Lab Module 08](https://github.com/orgs/programming-the-iot/projects/1#column-10488501).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?


In labmodule08, we learn about request/response protocols, how they work and how to implement a CoAP server to support our application

We first need to setup CoAP by installing the CoAPthon package to implement the CoAP protocol. We create the CoAP server abstraction and integrate it with DeviceDataManager. We need to create resource handlers to  support data update requests and data retrieval requests. We create these handlers `UpdateActuatorResourceHandler`, `GetSystemPerformanceResourceHandler` and `GetTelemetryResourceHandler`.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/cda-lab-modules-pkondrakunta/tree/labmodule08

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule08_cda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule08/labmodule08_cda.png?raw=true)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Part 01 and Part 02 tests  

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Part 01 and Part 02 tests
- CoapServerAdapterTest.py

EOF.
