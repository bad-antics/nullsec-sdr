# NullSec SDR Hardware Guide

## Supported Devices

### RTL-SDR
- **Frequency**: 24-1766 MHz
- **Sample Rate**: Up to 3.2 MSPS
- **Cost**: ~$25-35
- **Best For**: Beginners, RF exploration

```bash
nullsec-sdr --device rtlsdr --freq 433.92e6 --gain 40
```

### HackRF One
- **Frequency**: 1 MHz - 6 GHz
- **Sample Rate**: Up to 20 MSPS
- **TX/RX**: Half-duplex
- **Cost**: ~$300

```bash
nullsec-sdr --device hackrf --freq 2.4e9 --bandwidth 20e6
```

### USRP B200/B210
- **Frequency**: 70 MHz - 6 GHz
- **Sample Rate**: Up to 56 MSPS
- **TX/RX**: Full-duplex
- **Cost**: ~$1000-1500

```bash
nullsec-sdr --device usrp --freq 900e6 --rate 10e6
```

### PlutoSDR
- **Frequency**: 325 MHz - 3.8 GHz
- **Sample Rate**: Up to 20 MSPS
- **TX/RX**: Full-duplex
- **Cost**: ~$150

```bash
nullsec-sdr --device pluto --freq 1090e6
```

## Antenna Recommendations

| Frequency Range | Antenna Type | Notes |
|-----------------|--------------|-------|
| VHF (30-300 MHz) | Discone, dipole | Vehicle tracking, marine |
| UHF (300-3000 MHz) | Log-periodic, Yagi | ISM bands, cellular |
| 2.4 GHz | Patch, Yagi | WiFi, Bluetooth |
| 5.8 GHz | Dish, horn | Drone video, radar |

## Common Frequencies

| Application | Frequency |
|-------------|-----------|
| Car key fobs | 315/433 MHz |
| Garage doors | 300-400 MHz |
| Weather stations | 433 MHz |
| ADS-B (aircraft) | 1090 MHz |
| GPS | 1575.42 MHz |
| WiFi | 2.4/5 GHz |
| Bluetooth | 2.4 GHz |

## Installation

```bash
# RTL-SDR drivers
sudo apt install rtl-sdr librtlsdr-dev

# HackRF
sudo apt install hackrf libhackrf-dev

# GNU Radio (optional)
sudo apt install gnuradio
```
