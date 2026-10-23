---
title: Yaapu Telemetry App
parent: NOVALINK
nav_order: 6
---

# Yaapu Telemetry Script
{: .d-inline-block }

The Yaapu Telemetry Script is a powerful tool to allow live aircraft telemetry statistics to be displayed as a page on a radio transmitter.

This guide is meant as a quick-start to using the Yaapu Telemetry Widge with the NOVALINK mLRS Radio System. It is not an exhaustive guide, and more details specific to mLRS may be found <a href="https://github.com/olliw42/mLRS-docu/blob/main/docs/CRSF.md" target="_blank" rel="noopener noreferrer">HERE</a>.

There are a few assumptions in this guide:

- NOVALINK mLRS system has been bound and connected.

- Ardupilot flight controller with CRSF and Mavlink working.

- Radio controller compatible with Yaapu Telemetry Script. Check radio compatability <a href="https://github.com/yaapu/FrskyTelemetryScript/wiki/Supported-radios" target="_blank" rel="noopener noreferrer">HERE</a>.

Installation
{: .fs-6 .fw-500 }

Download and install the widget <a href="https://github.com/yaapu/frskytelemetryscript" target="_blank" rel="noopener noreferrer">HERE</a>.

Under `Model` -> `External RF`, check that protocol is set to `CRSF` and baud to `400k`.

<img src="{{ '/assets/images/novalink-62.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

Open the Yaapu Telemetry Configurator and select `enable CRSF Support` = `yes`

<img src="{{ '/assets/images/novalink-63.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

<img src="{{ '/assets/images/novalink-64.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

Yaapu Telemetry Widget should now be working. Please ensure that the widge view has been added as a view in EdgeTX.

<img src="{{ '/assets/images/novalink-61.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a>.