# Constrained Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-09-001 - Lab Module 09](https://github.com/orgs/programming-the-iot/projects/1#column-10488503).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

In labmodule09, we learn about the CoAP client setup for our application. This integration of CoAP client into your CDA will enable communication with the CoAP server (in my case the GDA is the server).

To get started, we first create an instance of the CoAP client and integrate it with our DeviceDataManager. Following this, we implement the request method implementations for `GET`, `PUT`, `POST` and `DELETE`. We also implement Observers which pre-process the request and delegate to the reponses to the respective routines.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/cda-lab-modules-pkondrakunta/tree/labmodule09


### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule09_cda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule09/labmodule09_cda.png?raw=true)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Part 01 & Part 02 tests

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Part 01 & Part 02 tests
- CoapClientConnectorTest.py

EOF.
