# Smart Voltage-Gated Equipment & Motor Protection System

An embedded system simulation designed in Proteus 9 using C++ on an Arduino UNO. It protects electrical equipment and AC motors from dangerous voltage anomalies (overvoltage, undervoltage, and spikes) using precision AC signal conditioning and automated switching.

## System Architecture & Components
- **Microcontroller:** Arduino UNO
- **Display:** 16x2 LCD (LM016L) via PCF8574 I2C Adapter Module
- **Signal Conditioning:** 10kΩ Resistor Divider + 10µF Filter Capacitor (2.5V DC Offset)
- **Transformer Model:** `TRAN-2P2S` (100H Primary, 6.46mH Secondary for 124.4:1 Step-Down)

## Mathematical & Electrical Parameters
- **AC Mains Input:** 220V RMS (311.13V Peak) @ 50Hz
- **Conditioned Secondary Output:** ±2.5V Peak AC
- **ADC Range (Pin A0):** 0.0V to 5.0V (Centered at 2.5V DC = 512 ADC value)

## Key Features
- Real-time AC voltage sampling and True RMS calculation.
- Automated voltage-gated trip/isolation logic for motor safety.
- Non-blocking I2C telemetry output.
