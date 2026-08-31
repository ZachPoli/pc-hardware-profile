# PC Specifications

_Last updated: 2026-08-30_

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

### Active wireless hardware
- Wavlink PCIe Wi-Fi 6E / Bluetooth adapter using an Intel AX210.
- Windows identifies Wi-Fi as `Intel(R) Wi-Fi 6E AX210 160MHz`.
- Bluetooth hardware ID verified as `USB\\VID_8087&PID_0032`, confirming the AX210 Bluetooth radio.
- Bluetooth cable is connected from the Wavlink card to the motherboard `USB_5_6` internal USB 2.0 header.
- External antennas are connected to the Wavlink adapter.

### Bluetooth repair result
The previous Intel Dual Band Wireless-AC 3168 path produced severe intermittent controller input lag, temporary unresponsiveness, and repeated disconnect/reconnect behavior. The same Xbox controller worked normally on another computer, and extensive software/driver troubleshooting did not resolve the desktop problem.

The AC 3168 was bypassed with the Wavlink AX210 PCIe adapter. After driver installation, the old AC 3168 network adapter was disabled and the Xbox controller was paired through the AX210. **Bluetooth is now working normally with no observed lag or disconnect problem in the verification test.**

### Legacy hardware
- Intel Dual Band Wireless-AC 3168 remains physically installed in the motherboard's awkward rear-I/O / vertical M.2 assembly.
- It is no longer used for normal wireless operation and can remain physically installed unless the motherboard is removed for another reason.

## RAM details reported by Windows

Both installed DIMMs report:
- Manufacturer: Kingston
- Part number: `KF552C40-16`
- Capacity: 16 GB each
- Configured clock speed: 5200 MT/s

Total installed RAM: **32 GB**

## Upgrade / maintenance priorities

1. Run post-cleaning thermal and benchmark baseline.
2. Evaluate CPU thermal paste only if temperatures warrant it.
3. Evaluate GPU repaste only if core/hotspot behavior indicates a real thermal problem.
4. Consider RAM upgrade only if actual memory pressure exceeds 32 GB.
5. Record PSU model/wattage, monitor resolution/refresh rate, external SSD details, and exact AIO model.
6. Consider BIOS update after baseline testing / before any future memory tuning or major hardware change.
