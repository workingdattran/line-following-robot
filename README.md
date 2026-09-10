# 🏎️ ESP32 PID Line-Following Robot — Hardware Design

Hardware design, schematics, and PCB layouts for a high-speed line-following robot powered by ESP32, featuring an 8-channel IR sensor bar and dual TB6612FNG motor driver interface.

---

## 🛠️ Hardware Overview

The hardware architecture is split into two main custom-designed boards:

1. **MCU & Power Distribution Board:**
   * **Core:** ESP32 Development Board footprint / headers.
   * **Motor Driver:** Socket for TB6612FNG dual H-bridge module.
   * **Power Regulation:** Onboard step-down circuitry (supporting 2S LiPo input) to supply stable 5V and 3.3V rails.
   * **Peripherals:** Breakouts for debugging (UART/Serial), status LEDs, and calibration pushbuttons.

2. **8-Channel IR Sensor Array Board:**
   * Custom front-mounted sensor bar optimized for standard line-tracking geometry.
   * Integrated IR emitter-receiver pairs (TCRT5000 / reflective sensors) with signal conditioning.
   * Compact connector interface routing back to the main MCU board.

---

## 📂 Hardware Design Files

```text
├── assets/
│   ├── mcu_board_3d.png      # 3D view of MCU mainboard
│   └── sensor_array_3d.png   # 3D view of 8-sensor bar
└── hardware/
    ├── mcu-board/
    │   ├── schematics/
    │   └── pcb/
    └── sensor-array/
        ├── schematics/
        └── pcb/
