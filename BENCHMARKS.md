# Benchmark and Thermal Log

Thermal/benchmark testing began after the August 2026 cleaning and AX210 wireless upgrade.

## Session checkpoint — 2026-08-30

Completed:
- Post-cleaning HWiNFO idle/light-use baseline.
- Cinebench 2026 CPU multi-core test.
- Cinebench 2026 GPU test.
- CPU and GPU both matched Cinebench's displayed identical-hardware reference scores.
- No CPU thermal throttling observed.
- CPU/AIO and GPU cooling results do not justify repasting or disassembly at this time.

Deferred to next session:
- CrystalDiskMark testing of the MSI M371 1TB NVMe and Samsung 860 QVO 2TB.
- HWiNFO monitoring of MSI M371 temperature sensor 2 during storage load.
- Investigation of occasional very slow archive extraction; compare 7-Zip with Windows Explorer if needed.
- Optional real-game thermal/stability benchmark after storage testing.

## Baseline system conditions

- Date: 2026-08-30
- Room/ambient temperature: Not recorded
- Side panel: Not recorded
- BIOS version: AMI 1.24 (2023-05-22)
- GPU driver version: 32.0.15.9159 (reported earlier by Windows)
- Windows power mode: Not recorded
- Monitoring: HWiNFO64 v8.52-6060
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

## CPU load — Cinebench 2026

- Test: Cinebench 2026.1.3 CPU (Multiple Threads)
- Date: 2026-08-30
- Score: **3211 pts**
- Cinebench built-in ranking showed an identical Ryzen 5 7600X reference score of 3211 pts.
- HWiNFO capture covered approximately 13 minutes including the benchmark and brief post-test cooldown.

| Metric | Result |
|---|---:|
| CPU Tctl/Tdie maximum | 82.6 C |
| CPU Tctl/Tdie average | 78.8 C |
| CPU Die (average) maximum | 80.6 C |
| CPU Die (average) average | 75.4 C |
| Peak CPU package power | 102.2 W |
| Average CPU package power | ~95.6-96.2 W |
| Peak CPU PPT | 100.0 W |
| Average CPU PPT | ~93.5-94.1 W |
| Peak core clock | 5,440 MHz |
| Average effective core clock | 4,807.6 MHz |
| Average total CPU usage | 96.2% |
| Maximum thermal-limit utilization | 94.8% |
| Thermal throttling (HTC) | No |
| Thermal throttling (PROCHOT CPU) | No |
| Thermal throttling (PROCHOT EXT) | No |
| Score | 3211 pts |

### CPU load assessment

- Result is excellent and exactly matches Cinebench 2026's displayed reference result for an identical Ryzen 5 7600X.
- The CPU sustained roughly 4.8 GHz average effective clocks at about 96 W package power without any reported thermal throttling.
- Peak Tctl/Tdie of 82.6 C is comfortably below the processor's thermal ceiling during this all-core rendering workload.
- The AIO is handling the 7600X properly. Current data does **not** justify replacing CPU thermal paste or the AIO.

## GPU load — Cinebench 2026

- Test: Cinebench 2026.1.3 GPU
- Date: 2026-08-30
- GPU: MSI GeForce RTX 4070 Ti Ventus 3X
- Score: **79,915 pts**
- Cinebench built-in ranking displayed **79,915 pts** for an identical NVIDIA GeForce RTX 4070 Ti reference entry.
- HWiNFO capture covered roughly 12.5 minutes including the benchmark and brief post-test cooldown.

| Metric | Result |
|---|---:|
| GPU core maximum | 54.7 C |
| GPU core average | ~50.3 C |
| GPU hotspot maximum | 61.2 C |
| GPU hotspot average | 57.3 C |
| Maximum hotspot-to-core delta | ~6.5 C |
| GPU memory junction maximum | 62.0 C |
| GPU memory junction average | 58.2 C |
| GPU thermal limit | 84.0 C |
| Peak reported GPU power | 155.2 W |
| Peak GPU rail power | 208.4 W |
| Peak total GPU power (% TDP) | 58.6% |
| Peak GPU clock | 2,910 MHz |
| Average GPU clock | ~2,745 MHz |
| Peak effective clock | 2,890.5 MHz |
| Average effective clock | ~2,735 MHz |
| Peak GPU core load | 95% |
| Average GPU core load | ~71% |
| Peak memory usage | 93.5% |
| Fan 1 maximum | 1,211 RPM / 30% |
| Fan 2 maximum | 1,222 RPM / 30% |
| Cinebench score | 79,915 pts |

### GPU load assessment

- Performance is exactly on Cinebench 2026's displayed reference score for an RTX 4070 Ti.
- Cooling performance is excellent: 54.7 C maximum core temperature, 61.2 C hotspot, and 62 C memory junction are all very comfortable under this workload.
- The hotspot-to-core spread is extremely small, giving no indication of poor cooler contact or dried thermal interface material.
- Fan speeds remained modest at roughly 30% maximum while maintaining low temperatures.
- HWiNFO showed `GPU Performance Limiters = Yes`; this alone is normal on NVIDIA GPUs because at least one boost limiter (power, voltage, utilization, etc.) is commonly active. With the exact-reference score and very low temperatures, there is no evidence of thermal throttling.
- HWiNFO briefly recorded up to 8 PCI Express error-counter events during this capture. No instability or performance loss was observed; monitor this counter in later testing rather than treating it as a fault from one isolated sample.
- Current data strongly argues **against** disassembling or repasting the RTX 4070 Ti.

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
| MSI M371 1TB | Pending CrystalDiskMark | | | Watch temperature sensor 2; idle/light-use max observed 69 C |
| Samsung 860 QVO 2TB | Pending CrystalDiskMark | | | Baseline temperature was excellent |
