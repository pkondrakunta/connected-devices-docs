# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-03-001 - Lab Module 03](https://github.com/orgs/programming-the-iot/projects/1#column-10488379).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

In labmodule03, we simulate an environment with simple sensor data that trigger actuation events. The DeviceDataManager, SensorAdapterManager and ActuatorAdapterManager play a key role in this module. The SensorAdpaterManager internally generates scheduled sensor data that are seemingly realistic. These are passed on to the DeviceDataManager which processes them and calls ActuatorAdapterManager when triggered. The ActuatorAdapterManager handles the Actuator simulation task from there on. 

How does your implementation work?

We create a SensorDataGenerator to generate the data that represents sensor data in real world like temperature, pressure, and humidity. We extend the BaseIotData class (which is basically a container class for component data) to create SensorData and ActuatorData which handle corresponding data. Using the BaseSensorSimTask, we create an instance of SensorData instance as well as provide a public interface to generate a new instance and access its data (HumiditySensorSimTask, TemperatureSensorSimTask, PressureSensorSimTask). These tasks can be processed by their simple sensor threshold crossings within the DeviceDataManager orchestration engine. From there, the ActuatorAdapterManager handles the actuation event using similar simulations of HumidifierActuatorSimTask and HvacActuatorSimTask (which extend BaseActuatorSimTask).

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/cda-lab-modules-pkondrakunta/tree/labmodule03

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule03_cda_readme](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule03/labmodule03/labmodule03_cda_readme.png?raw=true)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py

- HumiditySensorSimTaskTest.py
- PressureSensorSimTaskTest.py
- TemperatureSensorSimTaskTest.py

- ActuatorDataTest.py
- SensorDataTest.py
- SystemPerformanceDataTest.py
- BaseIotDataTest.py

- HumidifierActuatorSimTaskTest.py
- HvacActuatorSimTaskTest.py

> All unit tests in part02 except `DataUtilTest.py` passed.

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DeviceDataManagerNoCommsTest.py

EOF.
