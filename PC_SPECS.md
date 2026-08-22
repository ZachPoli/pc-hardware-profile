# PC Specifications

_Last updated: 2026-08-22_

## Core hardware

| Component | Current hardware | Notes |
|---|---|---|
| CPU | AMD Ryzen 5 7600X | 6 cores / 12 threads |
| Motherboard | ASRock B650M-C | AM5 / B650 |
| RAM | 32 GB DDR5 | 2 × 16 GB Kingston KF552C40-16 |
| RAM configured speed | 5200 MT/s | Reported by Windows |
| GPU | NVIDIA GeForce RTX 4070 Ti | Primary discrete GPU |
| Integrated graphics | AMD Radeon Graphics | Integrated with CPU |
| BIOS | AMI 1.24 | Release date reported as 2023-05-22 |
| CPU cooling | DeepCool AIO liquid cooler | Exact model TBD |
| PSU | TBD | Model/wattage not yet recorded |
| Case | TBD | Model not yet recorded |

## Internal storage

| Drive | Type | Approx. usable capacity |
|---|---|---:|
| MSI M371 | NVMe SSD | 932 GB |
| Samsung SSD 860 QVO 2TB | SATA SSD | 1,863 GB |

## External storage

External SSDs are available, but model/capacity details have not yet been recorded.

## Networking / Bluetooth

### Current
- Intel Dual Band Wireless-AC 3168
- Bluetooth on this adapter is unstable on the desktop:
  - severe intermittent controller input lag
  - temporary unresponsiveness
  - repeated disconnect/reconnect behavior
- The same Xbox controller works normally over Bluetooth on a laptop.
- Troubleshooting already performed:
  - antennas verified connected
  - Bluetooth power-saving disabled
  - Xbox controller firmware updated
  - Intel Bluetooth driver clean reinstall
  - PC full power reset
  - Wi-Fi-side disable test
- Result: problem persists, making the desktop wireless module the leading suspect.

### Planned
- Replace AC 3168 with Intel AX210 M.2 2230 Key-E Wi-Fi/Bluetooth module.

## RAM details reported by Windows

Both installed DIMMs report:
- Manufacturer: Kingston
- Part number: `KF552C40-16`
- Capacity: 16 GB each
- Configured clock speed: 5200 MT/s

Total installed RAM: **32 GB**

## Upgrade priorities

1. Replace failing/unstable AC 3168 wireless module with Intel AX210.
2. Clean dust from case, radiator, fans, GPU heatsink, and filters.
3. Run thermal/benchmark baseline after cleaning.
4. Evaluate CPU thermal paste only if temperatures warrant it.
5. Evaluate GPU repaste only if core/hotspot behavior indicates a real thermal problem.
6. Consider RAM upgrade only if actual memory pressure exceeds 32 GB.
7. Record PSU model/wattage, monitor resolution/refresh rate, external SSD details, and exact AIO model.
