Introduction
This RFID-Based Car Parking System integrates IoT and RFID technology to manage parking slots and track user information. It uses the Blynk App for real-time monitoring of parking slots and gate control. Additionally, the system logs the entry details (person's name, time, and date) into a Google Sheet each time an RFID cardholder enters the parking lot. This provides a smart and automated solution for parking management with real-time tracking and data logging.

Features
RFID-Based Detection: Automatic car detection using unique RFID tags/cards.
IoT Integration: Real-time slot status display in the Blynk app and remote gate control.
Google Sheets Logging: Uploads the RFID user's name, entry time, and date into a Google Sheet for record-keeping.
Real-Time Monitoring: Displays parking slot availability on a 20x4 LCD display and the Blynk app.
Entry Gate Control: Open and close the entry gate through the Blynk app.
Full Slot Notification: Displays "All slots booked" message when parking is full.
Technologies Used
Hardware:
Arduino/ESP microcontroller (e.g., NodeMCU for IoT capabilities)
MFRC522 RFID module
20x4 LCD display
Relay module for gate control
Buzzer (optional)
Software:
Arduino IDE
Blynk App (for real-time control and monitoring)
Google Sheets API (for logging user entry data)
MFRC522 library for RFID integration
LiquidCrystal_I2C library for LCD control
System Components
Microcontroller: ESP8266/NodeMCU or Arduino with IoT connectivity.
RFID Reader: MFRC522 module for detecting RFID tags/cards.
LCD Display: 20x4 I2C LCD for displaying available parking slots.
Relay Module: Controls the entry gate via the Blynk app.
Blynk App: Displays real-time slot status and provides remote control for the entry gate.
Google Sheets: Logs RFID cardholder details (name, time, date) for tracking purposes.
RFID Tags: Unique tags for each registered car/individual.
Blynk App Setup
Install Blynk: Download the Blynk app from the Play Store or App Store.
Create New Project: Set up a new project and choose the appropriate hardware (ESP8266/NodeMCU).
Widgets:
LCD Widget: Display parking slot availability in the app.
Button Widget: Add buttons to control the opening and closing of the entry gate.
Auth Token: Copy the auth token from the Blynk app and include it in your Arduino sketch for proper communication.
Google Sheets Integration
Google Cloud Console Setup:
Go to the Google Cloud Console, create a new project, and enable the Google Sheets API.
Download the API credentials as a .json file and include this in your project.
Logging User Data:
Each time an RFID card is scanned, the system records the user's name, entry time, and date.
This information is sent via the Google Sheets API and logged in a designated Google Sheet for future reference.
Usage
Hardware Operation:
Power the microcontroller and RFID module.
Place RFID cards near the RFID reader to simulate car entry.
Slot Status:
The available parking slots are displayed on both the 20x4 LCD display and in the Blynk app.
Gate Control:
Use the Blynk app to open and close the entry gate remotely.
Google Sheets:
When an RFID cardholder enters the parking lot, their name, entry time, and date are logged in real-time to a Google Sheet.
Parking Full Alert: The system will display a message when all parking slots are full.
Project Structure
bash
Copy code
car_parking_project/
│
├── src/
│   ├── car_parking.ino        # Main Arduino file with RFID and IoT integration
│   └── google_sheets.ino      # Script for Google Sheets API integration
├── README.md                  # Project documentation
├── libraries/
│   ├── MFRC522/               # RFID library
│   ├── LiquidCrystal_I2C/      # LCD library
│   ├── Blynk/                 # Blynk library for IoT
│   └── Google_Sheets_API/      # API for logging user data
└── ...
Future Enhancements
AI-based Number Plate Recognition: Add AI to detect number plates automatically instead of using RFID.
Automated Billing: Integrate payment systems for parking fee collection.
User Notifications: Send notifications to users when a parking slot becomes available.
Enhanced Security: Add additional security features like biometric verification.
Contributors
Avijit Biswas - Project Lead and Developer
