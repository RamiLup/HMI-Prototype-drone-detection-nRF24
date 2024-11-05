# Efficient, low-cost prototype drone detection system based on Elecrow HMI , 3 x 2.4GHz nRF24L01 modules, ESP32Wroom 

<br>

This document details the development and capabilities of a prototype drone proximity 
alert system, engineered as a POC to demonstrate the feasibility of rapid development 
for this technology.

The system is designed for cost-effective mass production and broad area coverage, 
prioritizing the utilization of readily available components and an efficient design.

<br>

<p align="center">
 
 ![System](https://github.com/user-attachments/assets/85bfa612-b3fe-44b3-82a2-0c31227e1318)

</p>
<br>

## TL;DR:

Built in just a week using readily available parts, this prototype drone 
detection system includes an intuitive HMI for easy setup and monitoring. 
Powered by an ESP32 microcontroller, it features nRF24L01+ transceivers 
and directional antennas to achieve a detection range of over 200 meters.

<br>

# Drone Proximity Alert System Prototype
This prototype showcases a fast-development approach for a drone proximity 
alert system. It is designed for cost-effective mass production and 
extensive area coverage, using readily available components and a 
straightforward design

<br>

## Hardware:

<p align="center">
 
![Visio](https://github.com/user-attachments/assets/7d347054-d3ab-441a-b8b5-690c273c44d0)

</p>
<br>

# Components
Each system utilizes the following components (multiple systems can be deployed):

HMI: 5" Elecrow HMI display (only one required)<br /> 
RF Module: Three or more Nordic Semiconductor nRF24L01+ 2.4GHz transceivers<br /> 
Microcontroller: ESP32 for managing RF modules and HMI communication<br /> 
Antennas: Directional (YAGI) and omnidirectional antennas<br /> 
Power Source: External battery<br /> 
Additional Materials: Case, RF cables , Decoupling Capacitors , Voltage Regulator<br /> 

![Prototype](https://github.com/user-attachments/assets/b6ed31d8-cd61-4bb5-befa-e3c6b8c72e3d)

<br>

# nRF24L01+

The system uses the nRF24L01+ transceiver module, which features a 
built-in power amplifier and offers 125 selectable channels within 
the globally license-free 2.4GHz ISM band

[NRF24L01 +PA.pdf](https://github.com/user-attachments/files/17596522/NRF24L01.%2BPA.pdf)

<br>

# Functional Description
This drone detection system leverages signal strength variations to identify 
approaching drones. The system employs a combination of directional and 
omnidirectional antennas to enhance detection accuracy and minimize false alarms.  
The integration of three nRF24 units provides operational flexibility, enabling customized 
configurations for range, channel selection, and scanning speed optimization.

<br>

# Development Stages

## Needs Assessment and Initial Testing: 
Initial drone flight tests were performed using a basic 
nRF24L01+ setup with various antennas to study signal 
behavior and optimize reception quality.

## Hardware Design: 
Based on these test results, the hardware was configured 
with three nRF24L01+ receivers and YAGI directional antennas 
to improve signal sensitivity and adding a direction-finding 
capabilities.

## Software Development: 
Code was developed for the ESP32 to control the nRF24L01+ 
receivers. The HMI was designed with a user-friendly interface, 
providing flexibility and options for future feature enhancements, 
with a focus on efficient field operation and clear alert displays.

## Software Implementation: 

The system software is developed using Arduino IDE for the ESP32, managing 
control of the three nRF24L01+ modules, I2C communication for the OLED 
display, and serial connectivity to the HMI. The HMI interface, created 
with the [LVGL library](https://lvgl.io/) in Visual Studio, enables rapid 
GUI development, providing an easy-to-use interface and clear visual 
feedback during field operations and experiments.

<br>

# HMI
The HMI includes two screens:
<br>
![Screen1-run](https://github.com/user-attachments/assets/b043b898-d329-4eb1-b6eb-5ae83eae1968)
![Screen2-settings](https://github.com/user-attachments/assets/68e6e1c3-a71e-4158-bfae-f970eb89b5e6)
<br>

## nRF Configuration and Activation: 
Individual control and parameter setting for each nRF24L01+ receiver.

<br>

## Channel Monitoring: 
Selection and monitoring of specific channels of interest within the 2.4GHz band.

<br>

## HMI Cost Optimization: 

* A single HMI unit is designed to connect to multiple drone detection systems,
reducing overall costs.

* Future Networked Deployment: Plans include connecting multiple systems within a closed network
for improved detection capabilities and operational efficiency.

<br>

# Conclusions & Key Notes

## Rapid Prototyping: 
The prototype was developed within a week, demonstrating the efficiency 
of the chosen approach.

<br>

## Enhanced Direction Finding: 
Adding more channels with dedicated directional antennas can significantly 
improve direction-finding accuracy.

<br>

## Environmental Considerations: 
Using a metallic enclosure and positioning antennas up to 2 meters away from 
the unit significantly improves system sensitivity and resilience to 
environmental noise. 

<br>

## Scanning Features:

* Full Spectrum Scanning: Scan all available frequencies using
  all nRF modules
* Selective Channel Monitoring: Monitor specific channels or a defined
  frequency range
* Individual nRF Configuration: Configure different scanning frequencies
* Dedicated channel for each nRF24L01+ receiver (up to 3 in total)
* Individual alerts can be configured for each nRF module

# Final Field Testing
Successful field tests were conducted with a drone flying at altitudes
between 15 and 25 meters. The system, equipped with two directional 
antennas and an omnidirectional antenna for ambient noise reference, 
detected the drone at distances over 200 meters

<br>

<p align="center">
 
![System](https://github.com/user-attachments/assets/59470f9b-9f4f-4d8e-aded-def212b6a98c)

</p>
