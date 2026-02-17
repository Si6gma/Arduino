<!--
Suggested GitHub Topics:
arduino, esp32, embedded-systems, iot, wifi, platformio, cpp, microcontroller, hardware, learning
-->

# Arduino ESP32 Projects

A collection of embedded systems experiments and learning projects for ESP32 microcontrollers, demonstrating IoT fundamentals from basic GPIO control to WiFi networking.

## Why This Exists

This repository serves as a personal learning sandbox for exploring ESP32 capabilities and embedded C++ development. It documents the journey from simple LED blinking to building functional WiFi-enabled applications, providing reference implementations for common IoT patterns.

## Tech Stack

- **Hardware:** ESP32 Development Board
- **Language:** C/C++ (Arduino Framework)
- **Build Tool:** PlatformIO
- **Libraries:** 
  - WiFi (ESP32 native)
  - WiFiClient
  - WiFiAP

## How to Build/Run

1. **Prerequisites:**
   - [PlatformIO](https://platformio.org/) installed (VS Code extension or CLI)
   - ESP32 development board

2. **Build and Upload:**
   ```bash
   # For ESP folder projects (PlatformIO)
   cd ESP
   pio run --target upload
   
   # For Storage sketches (Arduino IDE)
   Open .cpp files in Arduino IDE, select ESP32 board, and upload
   ```

3. **Monitor Serial Output:**
   ```bash
   pio device monitor --baud 115200
   ```

## Project Structure

```
Arduino/
├── ESP/                    # PlatformIO project
│   └── src/
│       └── main.cpp        # Testing sketch (placeholder)
├── Storage/                # Standalone Arduino sketches
│   ├── blink.cpp           # Basic LED blinking
│   ├── wifiScan.cpp        # WiFi network scanner
│   └── WifiAccessPoint.cpp # Web server + Access Point
├── .gitignore              # PlatformIO + macOS exclusions
└── README.md
```

## Key Learnings

- **ESP32 WiFi Modes:** Learned to switch between Station (STA) mode for scanning/connecting to networks and Access Point (AP) mode for hosting a standalone network
- **HTTP on Microcontrollers:** Built a minimal web server handling GET requests directly on the ESP32, controlling GPIO pins via browser
- **Serial Communication:** Used serial monitoring (115200 baud) for debugging and real-time network scan output
- **Embedded Development Workflow:** Transitioned from Arduino IDE to PlatformIO for better project structure and build management

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
