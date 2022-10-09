# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-04-001 - Lab Module 04](https://github.com/orgs/programming-the-iot/projects/1#column-10488386).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
In lab module 04, the main focus is to use the LED screen on the emulator as the actuator. We modified the SensorAdapterManager() and ActuatorAdapterManager() to support the emulated task as opposed to the simulated tasks in the previous modules. 

How does your implementation work?

We first setup and configure the sense-Emu Sense HAT Emulator. We create sensor emulator tasks like HumiditySensorEmulatorTask, PressureSensorEmulatorTask, TemperatureSensorEmulatorTask. These are managed using SensorAdapterManager. We also create actuator emulator tasks like HumidifierEmulatorTask, HvacEmulatorTask, LedDisplayEmulatorTask. These are managed using the ActuatorAdapterManager. We communicate with the Pi I2C using the Sense HAT board to emulate these tasks.


### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/cda-lab-modules-pkondrakunta/tree/labmodule04

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule04_cda_readme](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule04/labmodule04/labmodule04_cda_readme.png?raw=true)


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

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DeviceDataManagerNoCommsTest.py

- SenseHatEmulatorQuickTest.py
- HumidityEmulatorTaskTest.py
- PressureEmulatorTaskTest.py
- TemperatureEmulatorTaskTest.py
- HumidifierEmulatorTaskTest.py
- HvacEmulatorTaskTest.py
- LedDisplayEmulatorTaskTest.py
- SensorEmulatorManagerTest.py
- ActuatorEmulatorManagerTest.py
- EmbeddedSensorAdapterTest.py

EOF.
