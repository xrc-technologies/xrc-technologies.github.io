---
title: Firmware Upgrade
parent: NOVALINK
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
         width="1000">

Transmitter SWD pad location:

<img src="{{ '/assets/images/novalink-55.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="1000">

Wireless Bridge Firmware Update
{: .fs-6 .fw-500 }

Under some circumstances, it may be necessary to upgrade firmware of the Wireless Bridge.

Under most cases, users should use thge Web Flasher.

However, it is possible to use the USB port as a serial passthrough to flash the onboard ESP32 manually.

With CLI mode enabled, type `espboot;` on the Transmitter module. LEDs should flash quickly.

You may now flash the ESP32 normally using `esptool` and the CLI serial port. ESP32 version is `ESC32C3`.

More details <a href="https://docs.espressif.com/projects/esptool/en/latest/esp32c3/esptool/flashing-firmware.html" target="_blank" rel="noopener noreferrer">HERE</a>.

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a>.
