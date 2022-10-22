# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488421).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

In lab module 5, we try to create a data exchange between the CDA and GDA. We try to make them communicate with each other. In order to do this, we need to have a common data format. We have chosen JSON, Javascript Object Notation to do this communication.

The DataUtil is where the conversion of data occurs. In the `DataUtil.java`, we convert SensorData, SystemPerformanceData, ActuatorData and SystemStateData to JSON and vice versa.The DeviceDataManager class is where the data moves from and to the CDA as well as to and from the cloud. All this is connected and integrated with the main application in `GatewayDeviceApp.java`.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/gda-lab-modules-pkondrakunta/tree/labmodule05

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule05_gda_readme](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule05/labmodule05/labmodule05_gda_readme.png?raw=true)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- BaseIotDataTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- SystemStateDataTest
- DataUtilTest

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SystemPerformanceManagerTest
- DataIntegrationTest
- DeviceDataManagerNoCommsTest.java
- GatewayDeviceAppTest

EOF.
