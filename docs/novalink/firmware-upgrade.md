---
title: Firmware Upgrade
parent: NOVALINK mLRS Radio System
nav_order: 3
---

# Firmware Upgrade
{: .d-inline-block }

There are three options for firmware upgrade:

Web Flasher
{: .fs-6 .fw-500 }

This is the recommended firmware upgrade method.

Web-flasher support will arrive soon. Please visit <a href="https://olliw.eu/mlrs/flash/" target="_blank" rel="noopener noreferrer">mLRS Web Flasher</a> to upgrade firmware when it becomes available (November 2026).

DFU
{: .fs-6 .fw-500 }

Hold down Bind/DFU button while powering ON Transmitter/Receiver module.

Use STM32CubeProgrammer to upload .hex file.

Reboot.

ST-Link
{: .fs-6 .fw-500 }

Use STM32CubeProgrammer to upload .hex file.

Receiver SWD pad location:

<img src="{{ '/assets/images/novalink-54.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="300">

Transmitter SWD pad location:

<img src="{{ '/assets/images/novalink-55.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="300">

Wireless Bridge Firmware Update
{: .fs-6 .fw-500 }

Under some circumstances, it may be necessary to upgrade firmware of the Wireless Bridge.

It is recommended to flash using `esptool` in USB passthrough mode.

Connect the NOVALINK Transmitter module via USB while powered on and set the USB mode to `serial` - CLI mode. Also set `Ser Port2` to `wbridge` to enable the wireless bridge after flashing.

<img src="{{ '/assets/images/novalink-71.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="1000">

With CLI mode enabled, type `espboot;` in the serial console. LEDs should flash quickly.

<img src="{{ '/assets/images/novalink-76.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="500">

<img src="{{ '/assets/images/novalink-77.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="500">

You may now flash the ESP32 normally using `esptool` and the CLI serial port. ESP32 version is `ESP32C3`.

Please download the <a href="{{ '/assets/mlrs-wireless-bridge.ino.merged.bin' | relative_url }}" download>Wireless Bridge firmware binary</a>.

NOTE: Last date of compilation: October 26, 2026

An example command using the above binary and assuming COM port 16 would be:

`esptool --chip esp32c3 --port COM16 --baud 921600 write-flash 0x0 "mlrs-wireless-bridge.ino.merged.bin"`

<img src="{{ '/assets/images/novalink-75.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="1000">

Power cycle and if `wbridge` is enabled, the wireless bridge LED should start flashing, indicating that the WiFi hotspot is starting up.

It is also possible to use the <a href="https://olliw.eu/mlrs/flash/" target="_blank" rel="noopener noreferrer">mLRS Web Flasher</a>.

Please select the `MODULE_ESP32C3_ELRS_TX` version.

More ESP32 flashing details <a href="https://docs.espressif.com/projects/esptool/en/latest/esp32c3/esptool/flashing-firmware.html" target="_blank" rel="noopener noreferrer">HERE</a>.
