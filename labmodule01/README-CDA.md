# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-01-001 - Lab Module 01](https://github.com/orgs/programming-the-iot/projects/1#column-9974937).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
THe ConstrainedDeviceApp CDA is initialized. It starts the CDA, prints it to console on a successful start. The CDA runs for 60 seconds and then stops. It prints to the console when successfully stopped.


How does your implementation work?

We use `logging` for logging facilities and the `sleep` from `time` for the delay of 60 seconds. In the main Python function, we create an instance of the ConstrainedDeviceApp and call the startApp method. We then create a delay for 60 seconds using `sleep`, following which we call the stopApp(). We keep logging throughout the methods so that the user knows what's happening.

![cda-output](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule01/labmodule01/cda.png?raw=true)


### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/gda-lab-modules-pkondrakunta/tree/labmodule01

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule01-cda-uml](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule01/labmodule01_cda_readme.png?raw=true)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions. 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

EOF.
