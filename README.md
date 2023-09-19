# pqopen-common-main
Welcome to the PQopen Projects Overview Repository. Here you will find all the information about the project and its parts.

## Project Goals
- Creation of knowledgebase around measurement, data processing and analysis of electrical networks
- Use simple equipment for complex tasks and processes
- Create measurement clouds with much simpler and cheeper hardware for deeper network inspection and research

## What is PQopen?
PQopen is the Open Source Power Quality and Energy Analyzer. It consists of a measurement device and a server application for data storage and visualisation.

### PQopen Device
It can be used in power systems with 230V and 120V nominal voltage and measures parameters according to IEC 61000-4-30 and additionally power and energy.
- **Voltage:** True RMS Value, Fundamental Value, Harmonics, Frequency, Unbalance, Phase, Flicker (Fluctuations), Dip, Swell
- **Current:** True RMS Value, Fundamental Value, Harmonics, Phase
- **Power:** Active, Reactive and Apparent Power, Fundamental Values
All aquired data can be stored with different storing plans with individual storage intervalls.

### PQopen Server
The PQopen server is the backend to one or many PQopen devices. It manages the incoming data and stores them to the set databases. It consists of the following parts:
- **MQTT-Gateway:** Endpoint for the PQopen device's data transmission, distributing the incoming data to the set databases and managing commands back to the device
- **Databases:** A Timeseries database is used for measurement data, a nosql database is used for metadata, configuration and device management
- **Dashboard:** A Grafana instance for visualisation of the measured data
- **Config-WebApp:** A Web-Frontend for configuring the Device, Gateway and Reporting system
- **Reporting-Service:** Service for creating scheduled PDF reporting for e.g. EN 50160 reports

## Project Parts
The project consists of different parts, each maintained in a separate repository:
- **pqopen-device-hardware:** Electrical design, mechanical drawings and firmware for the PQopen device
- **pqopen-device-software:** Software for the PQopen device for data acquisition, calculation, data transmission and management
- **pqopen-server-software:** Software for the PQopen server endpoint. Gateway, database, dashboard and reporting
- **pqopen-client-tools:** Mixed Hard- and Software tools for testing and adjusting the PQopen device
- **pqopen-common-docs:** Documentation for the whole project

## Main Components
- Raspberry Pi 3A or newer
- Arduino Due

## Environment
- Device: Raspberry OS (Kernel 6.1), Python 3.11
- Dev: Arduino IDE 1.8.19, Python 3.11
- Server: Ubuntu 22.04 LTS with Docker Compose
