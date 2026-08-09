**Project Overview**

* Purpose: A real-time monitoring and alert system simulating core ADAS features for Electric Vehicles to improve driver safety and situational awareness.
* Core Workflow: Acquires vehicle telematics via sensors, processes thresholds on a microcontroller, and visualizes live data on a PC dashboard.

**Key Features**

* Real-time Monitoring: Tracks live vehicle speed, battery voltage, and motor temperature.
* ADAS Collision Warning: Uses proximity detection to alert drivers of imminent hazards.
* Interactive GUI Dashboard: Features clean graphical visualizers including gauges, charts, and alert logs.
* Dual Alert Mechanisms: Triggers immediate local hardware warnings alongside software dashboard flags.

**Hardware & Software Components**

* Microcontroller: STM32F103C8T6 ("Blue Pill") core processing unit programmed via ST-Link.
* Sensors & Modules: HC-SR04 ultrasonic sensor for obstacle detection, LM35/DHT11 for thermal tracking, and a custom voltage divider circuit for battery monitoring.
* Indicators & Interfaces: Local buzzer, indicator LEDs, and a USB-to-TTL converter for serial data transmission.
* Software Stack: Embedded C (STM32CubeIDE) for firmware; Python with serial and data visualization libraries for the PC GUI.

**System Architecture & Working Principle**

* Step 1 (Acquisition): Sensors continuously capture distance, temperature, and voltage metrics.
* Step 2 (Processing): STM32 evaluates raw data against predefined safety thresholds.
* Step 3 (Communication): Processed telemetry streams reliably to the PC via UART at 9600 baud.
* Step 4 (Visualization): The Python GUI parses incoming streams to update gauges and charts in real time.
* Step 5 (Alerting): Any threshold breach instantly activates local hardware indicators (buzzer/LED) and logs warning flags on the GUI.

**Key Results & Metrics**

* Latency: Achieved smooth real-time data acquisition with less than 500 ms response time.
* Proximity Precision: Reliable collision detection within a 20 cm range.
* System Stability: Continuous, error-free UART serial transfer.

**Applications**

* Prototyping platform for Electric Vehicles.
* Educational research tool combining Embedded C and Python data visualization.
* Driver assistance, fleet tracking, and telemetry base development.

**Future Enhancements**

* Hardware Upgrade: Replace PC GUI with a dedicated 7-inch TFT display and implement CAN Bus for real EV integration.
* Telematics Expansion: Integrate GPS and GSM modules for automated accident location tracking and emergency SMS notifications.
* Expanded ADAS Suite: Incorporate advanced algorithms for Lane Departure Warning and Speed Limit Alert systems.
