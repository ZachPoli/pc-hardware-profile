# Benchmark and Thermal Log

Thermal/benchmark testing began after the August 2026 cleaning and AX210 wireless upgrade.

## Baseline system conditions

- Date: 2026-08-30
- Room/ambient temperature: Not recorded
- Side panel: Not recorded
- BIOS version: AMI 1.24 (2023-05-22)
- GPU driver version: 32.0.15.9159 (reported earlier by Windows)
- Windows power mode: Not recorded
- Monitoring: HWiNFO64 v8.52-6060, sensors-only, roughly 5 minutes of light/idle observation
- Notes: PC had just been cleaned with an air duster. New Wavlink Intel AX210 PCIe Wi-Fi/Bluetooth adapter installed and working. Old Intel AC 3168 disabled for normal use.

## Post-cleaning idle / light-background baseline

| Sensor | Current / observed | Maximum | Average | Assessment |
|---|---:|---:|---:|---|
| CPU Tctl/Tdie | ~52.1 C | 58.6 C | 44.1 C | Healthy for Ryzen 5 7600X at idle/light background load |
| CPU Die (average) | ~37.7 C | 50.6 C | 38.7 C | Healthy |
| CPU Package Power | ~30.9 W | 55.3 W | 30.9 W | Background activity present; not a pure zero-load idle |
| CPU thermal throttling | No | No | 0% | No throttling observed |
| Motherboard | 36 C | 37 C | 36.1 C | Healthy |
| AMD chipset | 46.5 C | 47.4 C | 46.8 C | Healthy |
| DDR5 DIMM A | 37.8 C | 38.8 C | 38.2 C | Healthy |
| DDR5 DIMM B | 35.5 C | 36.2 C | 35.9 C | Healthy |
| RTX 4070 Ti core | 40.7 C | 43.9 C | 41.3 C | Excellent idle temperature; zero-RPM fans active |
| RTX 4070 Ti memory junction | 48 C | 52 C | 48.8 C | Healthy |
| RTX 4070 Ti hotspot | ~49-51 C | 54.3 C | 52.1 C | Healthy |
| RTX 4070 Ti power | ~13 W | 32.9 W | ~12-13 W | Normal light desktop use |
| Samsung 860 QVO 2TB | 28 C | 29 C | 29 C | Excellent |
| MSI M371 1TB sensor 1 | 43 C | 47 C | 44 C | Fine |
| MSI M371 1TB sensor 2 | 64 C | 69 C | 66 C | Warm; watch this sensor during storage/load testing |
| Windows Hardware Errors (WHEA) | 0 | 0 | 0 | No hardware errors observed |

### Initial assessment

- CPU and AIO behavior look healthy at idle/light load. Nothing here justifies replacing CPU thermal paste yet.
- RTX 4070 Ti temperatures are excellent. Do not repaste or disassemble the GPU based on current data.
- RAM, motherboard, chipset, and SATA SSD temperatures look healthy.
- The MSI M371 NVMe secondary temperature sensor is the only notable warm reading. It reached 69 C during this short observation, so it should be watched during storage and gaming tests before deciding whether it needs better airflow or an M.2 heatsink.
- HWiNFO reported zero CPU thermal throttling and zero WHEA hardware errors.

## CPU load

Test:
Duration:

| Metric | Result |
|---|---:|
| CPU max temperature | |
| CPU average temperature | |
| Peak package power | |
| Peak clock | |
| Score | |

## GPU load

Test:
Duration:

| Metric | Result |
|---|---:|
| GPU max core temperature | |
| GPU max hotspot temperature | |
| Hotspot delta | |
| Peak board power | |
| Peak clock | |
| Score | |

## Gaming stability test

Game:
Resolution:
Graphics settings:
Duration:

- Average FPS:
- 1% low:
- CPU max temp:
- GPU max temp:
- GPU hotspot max:
- Bluetooth/controller drops:
- Notes:

## Storage

| Drive | Benchmark | Read | Write | Notes |
|---|---|---:|---:|---|
| MSI M371 1TB | | | | Watch temperature sensor 2; idle/light-use max observed 69 C |
| Samsung 860 QVO 2TB | | | | |
