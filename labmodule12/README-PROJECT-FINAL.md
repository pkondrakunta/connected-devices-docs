# Lab Module 12 - Semester Project - Final Write-up

NOTE: Be sure to implement all the Lab Module 12 requirements listed at [Lab Module 12](https://github.com/orgs/programming-the-iot/projects/1#column-10488565).


## Description

Describe your idea in 1 paragraph (at least 2 or 3 sentences).

An automated version of the typical water tank. Using a water level sensor we can monitor the level of water in the tank. ANy any given instant we can take a look at the water level. We can also automatically create events that will turn on the motor to fill up the tank and turn off the motor to stop filling it once it is full.


## What - The Problem 

What problem did you tackle and why does it matter? Write 1 to 2 paragraphs in response.

In India, the city's water department releases water supply on specific days of the week. Very limited communities receive 24 hours of water. The water that needs to be consumed by a house has to be accessed and stored during these timings. Each household has a water tank and corresponding motor that need to be manually turned on when there is supply (the supply timings and days are subject to change). 

While the water fills up the tank when the motors is turned on, there is no way a person can determine how measure the level of water without physically going to the tank and seeing the depth of water. The only indication of that the water is filled, is the sound of water overflow from the tank. If no one turns off the motor once the tank is full, the overflowing water is wasted turned turned off (in the household or from the city's supply).


## Why - Who Cares? 

Why do you care about this particular problem? Write 1 to 2 paragraphs in response.

Water shortage is real in India (and everywhere. Obviously we don't pay attention to this as much). It is extremely important to avoid any wastage of water resources. 

For the households, monitoring the water level in the tank and the schedule of the city's water supply is an important chore. If I missed consecutive water releases from the supply, I may not have water running from the taps until my water tank is filled! At the same time, it is a hassle to keep track of the water level in the tank (each time, I have to physically see the level or wait hear the overflowing sound of water from the tank's location). Tackling this problem statement, can significantly impact how we handle this important chore of water access in each household.

## How - Expected Technical Approach

Write 1 to 2 paragraphs describing the outcomes you achieved.

Using a water level sensor and a valve actuator to the water tank, we can automate the manual task of water tank filling. Not only can we monitor the water level without the need to physically access the tank, we can also trigger the turn off of the sensors remotely. Furthermore, we can automate the process using event triggers to turn off water supply after it touches 95% (for example). I am also using a temperature sensor and pressure sensor to monitor the corresponding parameters. The HVAC actuator is trigger when the temperature drops below 0. 


### System Diagram

Embed a block diagram depicting your overall design, including the CDA, GDA, and Cloud Services interactions.
Be sure to include arrows depicting data flow from one application / service to the next.

Write 1 to 2 paragraphs describing your design.

![project_architecture_final](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/project_architecture_final.png)

At the Edge Tier, the architecture diagram depicts constrained device’s measurement of water level in the tank. I am using the water level sensor, temperature sensor and the pressure sensor. The temperature change is handled locally in the CDA to trigger actuation of the HVAC when dropped below the threshold. All these sensor readings are passed to the gateway device for further processing and transmission to the Cloud Tier.

In the GDA, the water level is analysed. This analysis compares the received value to a range. If below a certain level it triggers the valve open to allow water flow into the tank. If above the threshold, it closes the valve to stop the water flow. 

When the city supply schedule is released, the person can trigger activating the valve motor to fill up the tank. For a future use case, we can also use a sensor in the pipe that releases city's water supply to indicate to the user that the supply is here! If the measured water level is above a threshold value, the gateway device instructs the constrained device to activate the valve motor to stop water flow into the tank.

All this data collected, can be referenced later to analyze the frequency of water fills, and using the time between turn on/off, we can measure water consumption of the house and analyze causes of more/less consumption. Maybe we can even detect invisible leaks if my consumption has been a lot lately without any reason!


### What THREE (3) sensors and ONE (1) actuator did you use (add more if you wish)?

- CDA Sensor 1: Water Level Sensor (Simulated)
- CDA Sensor 2: Temperature Sensor (Simulated, can use Emulator too)
- CDA Sensor 3: Pressure Sensor (Emulated)
- CDA Actuator 1: HVAC Actuator (Emulated)

### What ONE (1) CDA protocol and TWO (2) GDA protocols did you implement (add more if you wish)?

- CDA to GDA Protocol: MQTT over TLS
- GDA to CDA Protocol: MQTT over TLS
- GDA to Cloud Protocol: MQTT over TLS
- Cloud to GDA Protocol: MQTT over TLS


 
### What TWO (2) cloud services / capabilities did you use (add more if you wish)?

- Cloud Service 1 (data ingress - all inputs):
	- SensorData(Water Level Data, Temperature Data, Pressure Data)
	- SystemPerformanceData (CDA CPU Utilization, CDA Memory Utilization)
	- SystemPerformanceData (GDA CPU Utilization, GDA Memory Utilization)
- Cloud Service 2 (data egress - all actuation events):
	- Actuator Data (Valve Actuator, LED Actuator, HVAC Actuator)

## Screen Shots Representing Cloud Services

![cs_cda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/cs_gda.png)
![cs_gda](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/cs_gda.png)

### Screen Shots Representing Visualized Data

NOTE: Include (at least) TWO (2) screen shots - one showing at least 1 hour
of time-series data from the CDA, and one showing an event being triggered
that results in an actuation event sent to your GDA and then to your CDA.

![cloud_dashboard](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/cloud_dashboard.png)
![before_actuation](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/before_actuation.png)
![after_actuation](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/after_actuation.png)
![gda_cda_actuation](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/gda_cda_actuation.png)
![local_actuation](https://github.com/NU-Connected-Devices/lab-module-docs-pkondrakunta/blob/default/labmodule12/local_actuation.gif]

EOF.
