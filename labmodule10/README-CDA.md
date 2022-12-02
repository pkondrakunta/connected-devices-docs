# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-10-001 - Lab Module 10](https://github.com/orgs/programming-the-iot/projects/1#column-10488510).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

![labmodule10_cda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/labmodule10_cda.png?raw=true)


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
- 
- 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 


### CDA MQTT Client Performance Test Results
CDA: Execute the timing tests you recently created within the CDA's MqttClientPerformanceTest.
            
![cda_connect_disconnect](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_connect_disconnect.png?raw=true)

![cda_qos0](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_qos0.png?raw=true)

![cda_qos1](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_qos1.png?raw=true)

![cda_qos2](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_qos2.png?raw=true)


How long was the connect / disconnect?
> The connect/disconnect was 5006.4 ms.

For the QoS tests, include the percentage difference between each QoS level, with QoS 0 tests as the baseline. Which ran fastest? Which ran slowest?
> QOS 0 - 0.622s. QOS 1 - 0.963s. QOS 2 -  1.178s. QOS 0 ran the fastest and QOS 2 ran the slowest. The percentage difference for QOS 1 is 54.8% and for QOS 2 is 89.2%.

### 2. CDA CoAP Client Performance Test Results
CDA: Execute the timing tests you recently created within the CDA's CoapClientPerformanceTest.

![cda_coap1](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_coap1.png?raw=true)

![cda_coap2](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_coap2.png?raw=true)

![cda_coap3](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_coap3.png?raw=true)

![cda_coap4](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule10/log_outputs/cda_coap4.png?raw=true)


For the CON and NON tests, include the percentage difference between them, with the NON test as the baseline. Which ran fastest? Which ran slowest?

> For PUT, the percentage difference was 3.73%. (NON - 10428.15ms, CON - 10817.40 ms).  For POST, the percentage difference was 0.52%. (NON - 10702.74, CON - 10758.72 ms).  
NON was the fastest. CON was the slowest.



EOF.
