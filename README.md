# Flow-Rate-Calculation of AC Condensed Water using ESP32 and US-100
This project measures the flow rate of air conditioner condensed water using an ESP32 microcontroller and a US-100 ultrasonic sensor. The system calculates the water level inside a cylindrical container, converts it into volume, determines the flow rate, and wirelessly transmits the data to a laptop where it is logged into a CSV file using a Python Flask server.

Features
Non-contact water level measurement
Wireless communication using WiFi
Automatic flow rate calculation
Real-time monitoring
CSV data logging
Low-cost IoT implementation
Hardware
Component	Purpose
ESP32	Microcontroller
US-100 Ultrasonic Sensor	Distance measurement
Cylindrical Container	Water collection
Laptop	Data logging
WiFi	Communication
Software
Arduino IDE
Python
Flask
VS Code
Working Principle
AC produces condensed water.
Water is collected inside a cylindrical flask.
US100 measures the distance from sensor to water.
Water height is calculated.
Volume is computed.
Flow rate is calculated.
ESP32 sends data through HTTP.
Python Flask stores readings in CSV.

Volume
V=πr^2h

Flow Rate
Flow Rate=ΔV/Δt
	​

Water Height

Water Height = Container Height − Measured Distance

Applications
Smart buildings,
Water conservation,
HVAC monitoring,
IoT monitoring systems,

Future Improvements
Cloud storage,
OLED display,
Waterproof enclosure,
Mobile application,
Automatic alerts,

ESP32 Code:

The Arduino sketch performs:

Connects to WiFi>
Reads US100 >
Calculates distance >
Calculates water level >
Calculates volume >
Calculates flow rate >
Sends data via HTTP POST every 15 seconds >

Python Flask Server :

Create a web server>
Receive POST requests>
Store readings>
Save CSV>
