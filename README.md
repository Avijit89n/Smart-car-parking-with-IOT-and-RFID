# Smart-car-parking-with-IOT-and-RFID

## Introduction
This RFID-Based Car Parking System integrates IoT and RFID technology to manage parking slots and track user information. It uses the Blynk App for real-time monitoring of parking slots and gate control. Additionally, the system logs the entry details (person's name, time, and date) into a Google Sheet each time an RFID cardholder enters the parking lot. This provides a smart and automated solution for parking management with real-time tracking and data logging.

## Features
- RFID-Based Detection: Automatic car detection using unique RFID tags/cards.
- IoT Integration: Real-time slot status display in the Blynk app and remote gate control.
- Google Sheets Logging: Uploads the RFID user's name, entry time, and date into a Google Sheet for record-keeping.
- Real-Time Monitoring: Displays parking slot availability on a 20x4 LCD display and the Blynk app.
- Entry Gate Control: Open and close the entry gate through the Blynk app.
- Full Slot Notification: Displays "All slots booked" message when parking is full.

## Technologies Used
### Hardware:
- ESP microcontroller 
- MFRC522 RFID module
- 20x4 LCD display
- Relay module for gate control
- Buzzer
- IR sensor
- lights
### Software:
- Arduino IDE
- Blynk App (for real-time control and monitoring)
- Google Sheets API (for logging user entry data)

## System Components
- Microcontroller: ESP32 
- RFID Reader: MFRC522 module for detecting RFID tags/cards.
- LCD Display: 20x4 I2C LCD for displaying available parking slots.
- Relay Module: Controls the entry gate via the Blynk app.
- Blynk App: Displays real-time slot status and provides remote control for the entry gate.
- Google Sheets: Logs RFID cardholder details (name, time, date) for tracking purposes.
- RFID Tags: Unique tags for each registered car/individual.
- IR Sensor Integration: Utilizes IR sensors to detect whether a parking slot is booked or empty.
