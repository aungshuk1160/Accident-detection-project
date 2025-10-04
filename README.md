🚨 Accident Detection and Alert System

This project is a Computer Interfacing course project developed to detect bike/car accidents and send immediate alerts.
The system uses multiple sensors and communication modules to monitor vehicle orientation and motion, trigger alarms, and send emergency SMS with live GPS location.

📌 Features

Accident detection using Accelerometer and Tilt Sensor

Immediate local alerts → Buzzer, Laser, Servo Lock simulation

Remote emergency alerts via GSM (SMS + automatic call)

GPS Integration → Sends real-time latitude & longitude with a Google Maps link

Bluetooth Commands → STOP, RESET, TEST, TRIGGER, HELP

LCD Display → Shows system status (Ready, Crash Detected, GSM Connected, etc.)

Manual Reset Button to cancel false alarms

🔧 Hardware Components

Arduino UNO (controls tilt, buzzer, servo, Bluetooth, laser)

Arduino NANO (controls GPS, GSM, accelerometer, LCD)

Accelerometer (X, Y, Z motion sensing)

Tilt Sensor

GSM Module (SIM800)

GPS Module (Neo-6M)

Bluetooth Module (HC-05/06)

LCD Display (I2C 16x2)

Buzzer

Laser System

Servo Motor

Emergency Push Button

Power Supply, Crystal Oscillator, Resistors, Capacitors, Transistors

💻 Software & Libraries

Arduino IDE (programming in C)

Libraries used:

SoftwareSerial.h → GSM & Bluetooth communication

AltSoftSerial.h → GPS data reading

TinyGPS++.h → Parse GPS coordinates

LiquidCrystal_I2C.h → LCD display

Servo.h → Servo motor control

Wire.h → I2C communication

math.h → Acceleration magnitude calculation

⚡ System Workflow

Monitoring → Accelerometer + Tilt Sensor continuously track vehicle status.

Accident Detection → If tilt/fall detected OR acceleration > threshold → Accident mode activates.

Immediate Actions → Buzzer + Laser ON, Servo Lock engaged, Bluetooth alert sent.

Emergency Response →

GPS fetches live location

GSM sends SMS with Google Maps link

GSM makes an emergency call

Control → System can be reset via button or Bluetooth command.

📍 Example Emergency SMS
EMERGENCY - Accident detected!
Location: http://maps.google.com/maps?q=loc:23.810331,90.412521
Impact magnitude: 42
Please send help immediately!

🛠️ How to Run

Connect all components as per circuit diagram.

Upload the UNO and NANO codes separately.

Insert SIM card into GSM module.

Power the system (5V regulated).

Test using tilt or sudden impact → Monitor SMS & call alerts.


🤝 Contributions

This project was developed as part of my Computer Interfacing course.
Contributions and improvements are welcome — feel free to fork and pull request!

📜 License

This project is open-source under the MIT License.
