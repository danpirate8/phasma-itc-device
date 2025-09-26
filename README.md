# Phasma ITC Device

The **Phasma ITC Device** is a DIY paranormal communication tool built with a Raspberry Pi Zero 2 W.  
It generates spoken words or phonemes based on sensor inputs (accelerometer, magnetometer, EMF probe)  
and randomness logic. Inspired by Ovilus-style devices, but completely open-source.

---

## Features
- Touchscreen GUI (Tkinter)
- Spoken word or phoneme mode (eSpeak-NG)
- Accelerometer, magnetometer, and EMF sensors
- Event log with timestamps
- Desktop launcher + autostart option
- Portable case with rechargeable power bank

---

## Hardware
- Raspberry Pi Zero 2 W
- Waveshare/Adafruit touchscreen HAT (3.5" or 4.0")
- Adafruit LSM9DS1 (I²C, bus 3 on GPIO5/6)
- Passive EMF probe (coil → USB mic input)
- USB sound card (mic + audio out)
- Internal power bank (5V 2A)
- Custom case (3D-printed or project box)

---

## Software Setup
```bash
sudo apt update
sudo apt install espeak-ng python3-tk python3-pil python3-pil.imagetk
git clone https://github.com/YOURUSERNAME/phasma-itc.git
cd phasma-itc/software
DISPLAY=:0 python3 phasma_gui.py
