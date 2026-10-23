---
title: SiK Telemetry Mode
parent: NOVALINK mLRS Radio System
nav_order: 11
---

# SiK Telemetry Mode
{: .d-inline-block }

NOVALINK can be used as a drop-in replacement for the popular SiK Telemetry Radio.

To setup, simply use the Transmitter and Receiver MAVLink protocol ONLY and disregard CRSF RC channels.

<img src="{{ '/assets/images/novalink-68.jpg' | relative_url }}"
         alt="NOVALINK radio system"
         width="700">

Ensure Transmitter `Ser Port` = `com` and `Snd RadioStat` = `1 Hz`

<img src="{{ '/assets/images/novalink-70.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="700">

Ensure Receiver `Ser Baudrate` = `your flight controller's baudrate setting` and `Snd RcChannel` = `off`

<img src="{{ '/assets/images/novalink-69.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="700">

Simply connect the TX1 and RX1 pads of the Receiver to the MAVLink serial prot on the flight controller.

Please ensure `SERIALx_PROTOCOL = 2` (Do not use MAVLink 1) and `SERIALx_BAUD` to match the receiver's baudrate setting as configured above.

Then, connect the Transmitter via the USB cable to the computer to be used as the ground station telemetry radio.

Alternatively, if the wireless bridge is used for MAVLink instead of the USB cable, configure the Transmitter as follows:

<img src="{{ '/assets/images/novalink-71.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="700">

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a>.
