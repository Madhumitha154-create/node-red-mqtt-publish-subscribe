**Node-RED MQTT Publish–Subscribe System**



**Project Overview:**



This project implements a publish–subscribe messaging system using \*\*Node-RED\*\* and an \*\*MQTT broker (Mosquitto)\*\*. The system simulates a smart monitoring environment where temperature and humidity data are published by sensor nodes and received by subscribers.



**System Components:**



**1.Publishers:**



Two publisher nodes simulate sensor data:



\* Temperature Sensor → publishes data to `campus/room1/temperature`

\* Humidity Sensor → publishes data to `campus/room1/humidity`



**2.MQTT Broker:**



The Mosquitto MQTT broker routes messages from publishers to subscribers.



**3.Wildcard Subscriber:**



A wildcard subscriber listens to:

`campus/room1/#`



This allows the subscriber to receive messages from multiple topics such as:



\* `campus/room1/temperature`

\* `campus/room1/humidity`



**Dashboard Visualization:**



A Node-RED dashboard displays live data using:



\* Temperature Gauge

\* Humidity Chart



**Quality of Service (QoS):**



The system uses \*\*QoS level 1\*\*, ensuring that messages are delivered \*\*at least once\*\* between publisher and subscriber.



**Retained Messages:**



Retained messages allow the MQTT broker to store the most recent message so that new subscribers receive the latest sensor data immediately.



**Architecture:**



Publisher → MQTT Broker → Subscriber → Dashboard



**Technologies** **Used:**



\* Node-RED

\* MQTT Protocol

\* Mosquitto Broker

\* Node-RED Dashboard



**Output Screenshots:**



The repository includes screenshots of:



\* Node-RED flow

\* Debug message log

\* Live dashboard visualization



