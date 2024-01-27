

## Description

This document proposes a semester project centered on a Hydroponics Farming System Application within the Internet of Things (IoT) framework. The project's objective is to monitor and control environmental factors in hydroponic systems, ensuring optimal plant growth and resource efficiency, particularly suited for urban farming environments.

## What - The Problem 

The project aims to address the challenge of maintaining optimal environmental conditions in hydroponic farming systems. The need stems from the complexity of controlling factors like nutrient levels, pH, temperature, and humidity in a confined urban farming space. Efficient monitoring and control can lead to enhanced plant growth and resource conservation.

## Why - Who Cares? 

Importance of the Problem:

This system is crucial for the advancement and sustainability of urban agriculture. It provides a solution to manage the growing environment effectively, thereby maximizing plant yield, reducing resource wastage, and supporting the scalability of urban hydroponics farming.

## How - Expected Technical Approach

The approach encompasses:

The approach encompasses:
- **Constrained Device Application (CDA):** Sensors for monitoring temperature, humidity, pressure levels.
- **Gateway Device Application (GDA):**:  Decision Making for actuators
- **Cloud Services:** For advanced data analysis, storage, and generating actionable insights.


### System Diagram
![MicrosoftTeams-image (1)](https://github.com/RKSanjit/piot-python-components/assets/144634185/0bb03570-4897-4da8-8226-f995856303f7)


In the Edge Tier of my hydroponics IoT monitoring system, the architecture diagram illustrates the use of a pressure sensor, humidity sensor, and temperature sensor on a constrained device. These sensors are crucial for maintaining the optimal environment for hydroponics. The temperature is managed locally by the Cloud Data Analytics (CDA), triggering the actuation of the HVAC system when it deviates from the desired range. The readings from all these sensors are then sent to the gateway device for further processing and transmission to the Cloud Tier.

In the Gateway Device Application (GDA), the pressure data is analyzed. This analysis involves comparing the received pressure values against a predefined range. If the pressure falls below a certain level, indicating potential issues in water circulation or nutrient delivery, the system triggers corrective actions, such as adjusting pumps or valves. Conversely, if the pressure is too high, the system will take measures to reduce it, ensuring the delicate balance in the hydroponics system is maintained.

Additionally, the humidity levels are closely monitored. If the humidity drops below a certain threshold, the system could activate humidifiers to maintain the optimal moisture level for plant growth. Conversely, if the humidity is too high, dehumidifiers might be activated to prevent mold growth and other humidity-related issues.



### Sensors and Actuators

- CDA Sensor 1: Humidity Sensor 
- CDA Sensor 2: Temperature Sensor 
- CDA Sensor 3: Pressure Sensor 
- CDA Actuator 1: HVAC Actuator

###  CDA protocol and GDA protocols

- CDA to GDA Protocol: MQTT over TLS
- GDA to CDA Protocol: MQTT over TLS
- GDA to Cloud Protocol: MQTT over TLS
- Cloud to GDA Protocol: MQTT over TLS


 
### Cloud services / capabilities used

- Cloud Service 1 (data ingress - all inputs):
	- SensorData(Water Level Data, Temperature Data, Pressure Data)
	- SystemPerformanceData (CDA CPU Utilization, CDA Memory Utilization)
	- SystemPerformanceData (GDA CPU Utilization, GDA Memory Utilization)
- Cloud Service 2 (data egress - all actuation events):
	- Actuator Data (LED Actuator, HVAC Actuator)


![image](https://github.com/RKSanjit/piot-python-components/assets/144634185/d780dde1-c46d-4944-9fba-93c6d0975031)
![image](https://github.com/RKSanjit/piot-python-components/assets/144634185/7016ca8e-04bd-46f9-b6ad-37f6c9f5ebf2)
![image](https://github.com/RKSanjit/piot-python-components/assets/144634185/d63327af-2ea8-4625-aaef-2054dc1082bd)
![image](https://github.com/RKSanjit/piot-python-components/assets/144634185/2634fcac-3fae-4ce5-a642-cea663118729)







EOF.
