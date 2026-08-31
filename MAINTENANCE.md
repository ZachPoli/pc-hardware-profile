# Maintenance Log and Plan

## 2026-08-30 — Wireless repair completed

### Cleaning
- Electric air duster obtained and PC cleaned before/while installing the wireless upgrade.
- Detailed post-cleaning thermal measurements are still pending.
- AIO remains sealed; no coolant service performed.

### Cooling inspection — pending
- [ ] Check AIO pump operation/noise under load.
- [ ] Record CPU idle and load temperatures.
- [ ] Record GPU core and hotspot temperatures.
- [ ] Decide whether CPU thermal paste replacement is justified.
- [ ] Do not disassemble/repaste GPU unless thermal data supports it.

### Wireless upgrade — completed
- [x] Chose a PCIe Intel AX210 adapter instead of removing the motherboard to access the hidden AC 3168 module.
- [x] Installed Wavlink Wi-Fi 6E / Bluetooth PCIe adapter using Intel AX210.
- [x] Installed adapter in available PCIe slot below the GPU.
- [x] Connected supplied Bluetooth USB cable to motherboard `USB_5_6` internal USB 2.0 header.
- [x] Connected external antennas to the Wavlink adapter.
- [x] Installed current Intel AX210 Wi-Fi driver.
- [x] Verified Windows detects `Intel(R) Wi-Fi 6E AX210 160MHz`.
- [x] Verified AX210 Bluetooth hardware ID as `USB\\VID_8087&PID_0032`.
- [x] Disabled the old Intel Dual Band Wireless-AC 3168 network adapter.
- [x] Re-paired Xbox controller through the AX210 Bluetooth radio.
- [x] Verified controller operation with no observed lag/disconnect problem during the post-upgrade test.

## Bluetooth issue history

The original AC 3168 Bluetooth path caused severe intermittent controller input lag, temporary unresponsiveness, and repeated disconnect/reconnect behavior. Troubleshooting included antenna inspection, power-management changes, controller firmware update, Intel Bluetooth clean reinstall, full PC power reset, and Wi-Fi coexistence testing. The same controller worked correctly on another computer.

The AC 3168 is physically difficult to access because it sits in the motherboard rear-I/O / vertical M.2 assembly. Rather than remove the motherboard solely for that module, the final repair bypassed it with the Wavlink AX210 PCIe adapter. The new Bluetooth connection is working normally.

## Notes

The CPU cooler appears to be a sealed DeepCool AIO. Its coolant is not treated as routine user-serviceable fluid; if pump/coolant performance fails, the normal remedy is AIO replacement rather than opening the loop.
