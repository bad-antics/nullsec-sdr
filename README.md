<div align="center">

# 📡 NullSec SDR

### Software-Defined Radio Security Toolkit

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
[![C](https://img.shields.io/badge/C-GNU_Radio-A8B9CC?style=for-the-badge&logo=c&logoColor=black)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()
[![NullSec](https://img.shields.io/badge/NullSec-Linux_v5.0-00ff41?style=for-the-badge&logo=linux&logoColor=white)](https://github.com/bad-antics/nullsec-linux)

*RF signal analysis, capture, replay, and protocol decoding for security research*

</div>

---

## 🎯 Overview

NullSec SDR is a comprehensive software-defined radio toolkit for security researchers. It wraps complex SDR workflows into streamlined commands for signal reconnaissance, protocol analysis, and vulnerability assessment across the RF spectrum.

## ⚡ Features

| Feature | Description |
|---------|-------------|
| **Spectrum Scanner** | Wideband scanning with automatic signal detection (1 MHz – 6 GHz) |
| **Signal Capture** | IQ recording with metadata tagging and GPS correlation |
| **Protocol Decoder** | Automatic identification of 30+ RF protocols |
| **Replay Engine** | Signal replay with timing and frequency adjustment |
| **Waterfall Viewer** | Real-time spectral visualization in terminal |
| **Frequency Database** | Known frequency lookup for your region |

## 📻 Supported Hardware

| Device | Frequency Range | Status |
|--------|----------------|--------|
| HackRF One | 1 MHz – 6 GHz | ✅ Full |
| RTL-SDR v3/v4 | 24 MHz – 1.766 GHz | ✅ Full |
| YARD Stick One | Sub-1 GHz | ✅ Full |
| LimeSDR | 100 kHz – 3.8 GHz | ✅ Full |
| BladeRF | 300 MHz – 3.8 GHz | ⚠️ Beta |
| Pluto SDR | 325 MHz – 3.8 GHz | ⚠️ Beta |

## 🚀 Quick Start

```bash
# Install
pip install nullsec-sdr

# Scan the spectrum
nullsec-sdr scan --range 315M-915M --threshold -40

# Capture a signal
nullsec-sdr capture --freq 433.92M --rate 2M --duration 10 -o capture.iq

# Decode protocol
nullsec-sdr decode capture.iq --protocol auto

# Replay signal
nullsec-sdr replay capture.iq --freq 433.92M --gain 40
```

## 🔬 Supported Protocols

| Protocol | Frequency | Use Case |
|----------|-----------|----------|
| ASK/OOK | 315/433 MHz | Garage doors, sensors |
| FSK | Various | Weather stations, TPMS |
| LoRa | 868/915 MHz | IoT networks |
| Z-Wave | 868/908 MHz | Home automation |
| Zigbee | 2.4 GHz | Smart home |
| POCSAG | 150-170 MHz | Paging systems |
| ADS-B | 1090 MHz | Aircraft tracking |
| ACARS | 131.55 MHz | Aviation data |
| P25 | Various | Public safety radio |
| DMR | Various | Digital mobile radio |

## 🔗 Related Projects

| Project | Description |
|---------|-------------|
| [nullsec-rfid](https://github.com/bad-antics/nullsec-rfid) | RFID/NFC cloning & analysis |
| [nullsec-glitch](https://github.com/bad-antics/nullsec-glitch) | Voltage glitching attacks |
| [nullsec-keyfob](https://github.com/bad-antics/nullsec-keyfob) | Automotive key fob analysis |
| [nullsec-flipper-suite](https://github.com/bad-antics/nullsec-flipper-suite) | Flipper Zero payload suite (430+ files) |
| [nullsec-linux](https://github.com/bad-antics/nullsec-linux) | Security Linux distro (140+ tools) |

## ⚠️ Legal

This tool is for **authorized security testing and educational purposes only**. Transmitting on frequencies you are not licensed for is illegal. Always check local regulations.

## 📜 License

MIT License — [@bad-antics](https://github.com/bad-antics)

---

<div align="center">

*Part of the [NullSec Hardware Security Suite](https://github.com/bad-antics)*

</div>
