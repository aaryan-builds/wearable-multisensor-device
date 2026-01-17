# Wearable Multi-Sensor Device (ECG + PPG + IMU + Temp) — STM32 + Custom FPC

A low-power wearable platform that streams synchronized physiological + motion signals in real time.
Built around an ARM Cortex (STM32) with I2C/SPI sensors, a custom FPC layout, and bench-validated
debugging focused on noise/EMI + sensor coexistence.

## What it does
- Captures **ECG**, **PPG**, **IMU (MPU6500)**, and **Temperature**
- Streams synchronized data for real-time visualization / logging
- Designed for **low power** operation and clean signal integrity on a wearable form factor

## System overview
**Sensors → STM32 (I2C/SPI) → buffering + timestamp sync → streaming/logging**

📌 Add your architecture diagram here:
`docs/images/architecture.png`

## Highlights
- Multi-sensor integration with synchronized timestamps
- Real-time streaming pipeline for synchronized readings
- Custom **FPC/PCB layout** to reduce noise, EMI, and crosstalk (validated through bench testing)
- Practical debugging: sensor coexistence, EMC/ESD/RF interference, failure analysis

## Repo layout
- `firmware/` — STM32 firmware (drivers, sampling, sync, streaming)
- `hardware/` — PCB/FPC design files, exports, notes
- `docs/` — architecture, bring-up notes, BOM, validation notes
- `data/` — sample logs (sanitized)
- `tools/` — scripts for parsing/plotting logs
- `demo/` — videos / GIF links

## Getting started
### Firmware
See `firmware/README.md`

### Hardware
See `hardware/README.md`

## Results & validation
Bench tests include:
- Signal integrity checks (scope + grounding strategy)
- Noise/EMI investigations and layout iteration notes
- Streaming stability + timing checks

(You can add plots/screenshots in `docs/images/`.)

## Future work
- Power profiling + sleep scheduling improvements
- On-device feature extraction (HR/HRV, motion features)
- More robust ESD/EMC hardening + enclosure considerations

## License
This project is licensed under the MIT License — see `LICENSE`.
