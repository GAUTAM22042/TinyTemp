Perfect 👍 — let me update the **README.md** so it credits both you and Aadvik Mishra as co-authors.

---

# TinyTemp 🌡️  
*A compact digital thermometer built on the ATtiny85 microcontroller*  

TinyTemp is a lightweight temperature monitoring system designed to demonstrate low-power embedded system design on resource-constrained hardware.  
It’s a downsized version of our **MegaTemp** project (ATmega328P) redesigned for the **ATtiny85** microcontroller.  

---

## ✨ Features
- Reads ambient temperature using the **TMP36 sensor**  
- Displays readings on a **0.96" SSD1306 OLED** (I²C interface)  
- Supports **Celsius/Fahrenheit switching**  
- Optimized firmware with **sleep modes + watchdog timers** for reduced power consumption  
- Runs for **weeks on a coin cell battery**  

---

## 🛠️ Tech Stack
- **Microcontroller:** ATtiny85  
- **Firmware:** Embedded C (avr-gcc, avrdude)  
- **Display:** SSD1306 OLED (I²C)  
- **Sensor:** TMP36 temperature sensor  
- **Tools:** KiCad (PCB design), Arduino IDE (prototyping), OSH Park (fabrication)  

---

## 🚀 Getting Started

### Prerequisites
- AVR toolchain (`avr-gcc`, `avrdude`)  
- Arduino IDE (optional, for testing)  
- SSD1306 OLED + TMP36 sensor  
- ATtiny85 + USB programmer  

### Build & Flash
bash
# Compile
avr-gcc -mmcu=attiny85 -Os -o tinytemp.elf tinytemp.c

# Convert to HEX
avr-objcopy -O ihex tinytemp.elf tinytemp.hex

# Flash to ATtiny85
avrdude -c usbtiny -p attiny85 -U flash:w:tinytemp.hex



## 📐 Hardware Setup

* **TMP36 sensor** → Analog input pin
* **SSD1306 OLED** → I²C pins (SDA/SCL)
* **Power source:** Coin cell / 3V battery

Schematic and PCB layout are available in the `/hardware` folder (KiCad files).

---

## 📸 Demo

*(Add images/gifs of your setup + OLED output here once ready)*

---

## 📄 License

MIT License – feel free to use, modify, and build upon this project.

---

## 👥 Authors

* **Gautam Jayakishan** – [LinkedIn](https://www.linkedin.com/in/gautam-jayakishan-350a8b1b8/)
* **Aadvik Mishra** – [LinkedIn](https://www.linkedin.com/in/aadvik-mishra-2a8981252/) 

