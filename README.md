# ESP01 Ultimate Programmer & Adapter (DIY)

This project provides a complete schematic and guide to building a custom, reliable programmer for the **ESP-01 (ESP8266)** module. 

### 🚀 Why this project?
Standard USB-to-ESP01 adapters often lack physical buttons for **Reset** and **Flash mode**, making the programming process tedious. This DIY board replaces the need for expensive dedicated adapters and works perfectly with any generic **USB to TTL (UART)** converter.

### 🛠 Hardware Features:
- **Auto-Stable Power:** Includes a 100uF capacitor to prevent voltage spikes during WiFi initialization.
- **Dedicated Buttons:** Hardware buttons for `Reset` and `GPIO0` (Flash) for easy mode switching.
- **Pull-up Resistor:** A 10k ohm resistor on the `RST` pin ensures system stability and prevents random reboots.
- **Universal Compatibility:** Can be used with CP2102, FTDI, or any USB-to-TTL module.

### 📋 Connection Diagram:

<div align="center">
  <a href="ESP01_adapter.png">
    <img src="circuit_TEST_1.png" width="400" alt="Circuit Test Image">
  </a>
</div>
<div align="center">
  <a href="ESP01_Adapter.jpg">
    <img src="circuit_TEST_1.png" width="800" alt="Circuit Test Image">
  </a>
</div>


### 🔌 Pinout Configuration:
| ESP-01 Pin | Connection | Component |
|------------|------------|-----------|
| **VCC** | 3.3V       | 100uF Capacitor (+) |
| **GND** | GND        | 100uF Capacitor (-) |
| **CH_PD** | 3.3V       | Direct Jump (Enable) |
| **RST** | 3.3V & GND | 10k Resistor (to 3.3V) & Push Button (to GND) |
| **GPIO 0** | GND        | Push Button (to GND for Flash Mode) |
| **TX/RX** | RX/TX      | To USB-TTL Adapter |

### 📟 How to Program:
1. Connect your **USB to TTL** (3.3V Level!).
2. Hold the **Flash Button** (GPIO0).
3. Press the **Reset Button** once.
4. Release the **Flash Button**.
5. Click **Upload** in Arduino IDE.
6. Once finished, press **Reset** again to run your code.

---
*Created with ❤️ for the ESP8266 Community.*
