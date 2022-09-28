# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
In lab module 02, we try to get our IoT solution up and running. We try to capture system performance like memory utilization and CPU utilization. The ConstrainedDeviceApp is where the application starts and creates the instance of SystemPerformanceManager. There are two system performance task components: SystemCpuUtilTask (collects CPU utilization) and SystemMemUtilTask (system memory utilization). Both these task components are extended from the BaseSystemUtilTask. 

How does your implementation work?
We start by creating the SystemPerformanceManager and the BaseSystemUtilTask. The two task modules SystemCpuUtilTask (collects CPU utilization) and SystemMemUtilTask (system memory utilization) are extended from the BaseSystemUtilTask. We use the scheduler to check for new data at a regular intervals.

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/cda-lab-modules-pkondrakunta/tree/labmodule02

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule02_cda_readme](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule02/labmodule02/labmodule02_cda_readme.png?raw=true)

### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py
- SystemPerformanceManagerTest.py

EOF.
