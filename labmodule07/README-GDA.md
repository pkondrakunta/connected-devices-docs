# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-07-001 - Lab Module 07](https://github.com/orgs/programming-the-iot/projects/1#column-10488499).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

We use MQTT messaging protocol to exchange IoT messages between our applications and to communicate to cloud services. In labmodule07, we are setting up the MQTT infrastructure (for the GDA) to use it in future cloud integration parts. MQTT is a publish/subscribe protocol (or a pub/sub protocol) where one will publish a message to a destination using a specific name, which is usually called a topic (or a channel). The other will subscribe to the destination system using the same topic name as the publisher. Whenever the publisher sends a message, the subscriber is notified and forwarded that message. This process is handled by a broker application that can support multiple publishers and subscribers.

We install the mosquitto MQTT messaging broker and test using `mosquitto_pub` and `mosquitto_sub` to send messages. In this module we also explore the control packets of the MQTT message. Technically, there are 16 control packets but in this particular version we use 14 and all those are captured using wireshark in this module (and the next module). 

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/NU-Connected-Devices/gda-lab-modules-pkondrakunta/tree/labmodule07

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule07_gda_readme](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/labmodule07/labmodule07/labmodule07_gda.png?raw=true)


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
- MqttClientConnectorTest.java

EOF.
