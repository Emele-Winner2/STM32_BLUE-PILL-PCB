# Custom STM32F103 "Blue Pill" Development Board 🚀

This repository contains the complete hardware design files for a custom, enhanced 4-layer redesign of the classic STM32F103 "Blue Pill" development board. Designed entirely in KiCad, this board optimizes signal integrity, power distribution, and clock stability compared to standard 2-layer commercial alternatives.

---

## 🛠️ Hardware Specifications & Features

* **MCU Core:** STM32F103C8T6 ARM Cortex-M3 microcontroller.
* **4-Layer Stackup:** Engineered with dedicated internal planes to maximize electromagnetic shielding and ensure pristine signal paths.
  * **Layer 1 (Top):** High-speed signaling (USB differential pairs), crystal oscillator tracking, and local component connections.
  * **Layer 2 (Internal):** Solid, unbroken **Ground (GND) Plane** for low-impedance return paths.
  * **Layer 3 (Internal):** **Power (PWR) Plane** for clean 5V power distribution.
  * **Layer 4 (Bottom):** General purpose I/O breakouts and non-critical low-speed routing.
* **USB Interface:** Native USB Full-Speed connection with hardware-matched series termination resistors and a proper 3.3V pull-up network for reliable host computer enumeration.
* **Dual Clock Architecture:** * High-Speed External (HSE): 8MHz main crystal with optimized, short symmetric routing.
  * Low-Speed External (LSE): 32.768kHz dedicated real-time clock (RTC) crystal.

---

## 📂 Repository Structure

```text
├── bluetooth_mcu.kicad_pro   # KiCad main project file
├── bluetooth_mcu.kicad_sch   # System schematic design
├── bluetooth_mcu.kicad_pcb   # 4-layer PCB layout design
├── .gitignore                # Automatically filters out KiCad backup/local files
└── README.md                 # Project documentation (this file)
