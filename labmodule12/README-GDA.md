# Gateway Device Application (Connected Devices)

## Lab Module 12 - Semester Project - GDA Components

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-12-001 - Lab Module 12](https://github.com/orgs/programming-the-iot/projects/1#column-10488565).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

Updated the GDA to communicate via MQTT to CDA for exchange of CDA SensorData and SystemPerformanceData. Handled Water level sensor analysis trigger the valve actuator when not in the nominal range. Retrieves cloud data and passes it on to the CDA if actuator command is valid.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/gda-lab-modules-pkondrakunta/tree/labmodule12

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule12_gda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/labmodule12_gda.png)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- Part01, Part 02, Part 03 and Part04 tests

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Part01, Part 02, Part 03 and Part04 tests

EOF.
