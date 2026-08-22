# Maintenance Log and Plan

## 2026-08-22 — Planned maintenance

### Cleaning
- [ ] Power down PC and unplug it.
- [ ] Use compressed air or an electric duster.
- [ ] Hold fan blades stationary while cleaning them.
- [ ] Clean top radiator/fins from both directions where accessible.
- [ ] Clean GPU heatsink/fans.
- [ ] Clean rear and front case fans.
- [ ] Clean case filters and bottom intake area.
- [ ] Avoid opening the sealed AIO loop.

### Cooling inspection
- [ ] Check AIO pump operation/noise after cleaning.
- [ ] Record CPU idle and load temperatures.
- [ ] Record GPU core and hotspot temperatures.
- [ ] Decide whether CPU thermal paste replacement is justified.
- [ ] Do not disassemble/repaste GPU unless thermal data supports it.

### Wireless upgrade — PCIe AX210 bypass
- [ ] Use an Intel AX210-based PCIe adapter rather than removing the motherboard to access the existing AC 3168 module.
- [ ] Preferred current option: Cudy WE3000S 2.0 (Intel AX210, Wi-Fi 6E, Bluetooth 5.3).
- [ ] Shut down Windows, switch PSU off, and unplug the PC.
- [ ] Press the case power button briefly after unplugging to discharge residual power.
- [ ] Install the adapter in an available PCIe slot.
- [ ] Connect the adapter's supplied Bluetooth cable to an available motherboard USB 9-pin header.
- [ ] Mount/connect the adapter's external antennas.
- [ ] Reassemble and power on.
- [ ] Install current Wi-Fi/Bluetooth drivers for the new adapter.
- [ ] Pair Xbox controller and test Bluetooth stability for at least 15 minutes.
- [ ] Test at least one additional Bluetooth device if available.
- [ ] After the new adapter is verified, disable the old Intel AC 3168 Wi-Fi/Bluetooth devices in Windows so the PC uses only the new radio.

## Notes

The CPU cooler appears to be a sealed DeepCool AIO. Its coolant is not treated as routine user-serviceable fluid; if pump/coolant performance fails, the normal remedy is AIO replacement rather than opening the loop.

The existing AC 3168 is in an awkward rear-I/O / vertical M.2 assembly. The decision is to bypass it with a PCIe AX210 adapter rather than remove the motherboard solely to replace the hidden module.
