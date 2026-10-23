---
title: Wireless Bridge
parent: NOVALINK mLRS Radio System
nav_order: 7
---

# Wireless Bridge
{: .d-inline-block }

NOVALINK supports an onboard Wireless Bridge out of the box. By default, this is an ESP32-C3 configured for UDP mode.

Enable
{: .fs-6 .fw-500 }

To use, please configure the Transmitter module as follows (Ignore `Power` setting):

<img src="{{ '/assets/images/novalink-38.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

Upon power on, the transmitter module will create a WiFi hotspot with either the SSID ```XRC TECHNOLOGIES NOVALINK``` or something similar to ```mLRS-4983 AP UDP```

Connect to this WiFi network. By default there is no password:

<img src="{{ '/assets/images/novalink-44.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="300">

In Mission Planner, change connection settings to:

- UDP

- 115200 Baud Rate

<img src="{{ '/assets/images/novalink-45.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

Press ```Connect```

When it asks for Local port, enter ```14550``` then click OK

<img src="{{ '/assets/images/novalink-46.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="800">

Params should now start loading via Mavlink. To test, try rotating the flight controller to see attitude change in HUD:

<img src="{{ '/assets/images/novalink-47.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="800">

At 433MHz, the params will load slower than on a higher frequency. However, it should only take a minute or two before all params have loaded.

<img src="{{ '/assets/images/novalink-48.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="300">

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a>.
