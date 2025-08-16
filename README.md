🔥 Heater Control System using Arduino Uno and DHT22

A temperature-based heater control simulation using Arduino Uno and a DHT22 sensor, implemented with a 5-state logic system. The project demonstrates how embedded systems can manage heating safely and intelligently, with state transitions, serial logging, and actuator control.

📌 Features

✅ 5-state control logic:

IDLE, HEATING, STABILIZING, TARGET REACHED, OVERHEAT

✅ Real-time temperature and humidity monitoring (DHT22)

✅ Heater simulation using LED

✅ Overheat alert via Buzzer

✅ Serial logging for debugging and status monitoring

⚙️ Fully simulated in Wokwi

🧠 State Logic Summary
State	Trigger	Heater (LED)	Buzzer
IDLE	System start or temp ≥ target	OFF	OFF
HEATING	Temp < 39 °C	ON	OFF
STABILIZING	Temp between 39–40 °C	ON	OFF
TARGET REACHED	Temp ≥ 40 °C and < 50 °C	OFF	OFF
OVERHEAT	Temp ≥ 50 °C	OFF	ON
🔧 Components Used
Component	Function	Pin Mapping (Wokwi)
Arduino Uno	Microcontroller	—
DHT22 Sensor	Temp & humidity input	DATA → D2
LED	Heater simulation	A → D4, C → GND
Buzzer	Overheat alert	+ → D5, – → GND
🚦 How It Works

DHT22 provides temperature and humidity readings.

Based on thresholds, Arduino determines current state.

Heater (LED) turns ON/OFF depending on heating state.

Buzzer activates when temperature exceeds 50 °C.

Serial Monitor logs:

Temp: 42.00 °C | Humidity: 45.00% | State: TARGET REACHED

🧪 Simulation Instructions

Open the project in Wokwi.

Press Run.

Click the DHT22 sensor and adjust temperature slider.

Observe:

LED turns ON during HEATING

Buzzer activates in OVERHEAT

Serial Monitor logs real-time data

📁 File Structure
heater-control-project/
├── heater_control.ino     # Arduino sketch
├── diagram.json           # Wokwi simulation wiring
├── wokwi.toml             # Library dependencies
├── README.md              # Project overview and instructions
├── system_design.docx     # Part 1 (System Design)
└── embedded_implementation.docx # Part 2 (Implementation)

🛠 Future Improvements

BLE communication (e.g., ESP32 + mobile app)

Multiple heating profiles

LCD/OLED display for real-time status

PID-based temperature control

Humidity-based safety shutoff
