---
title: Logging
parent: NOVALINK mLRS Radio System
nav_order: 8
---

# Logging
{: .d-inline-block }

There are many ways to log flight data. One convenient option will be presented in this guide, but please refer to the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a> for additional Logging options.

There is an excellent <a href="https://oscarliang.com/log-telemetry/" target="_blank" rel="noopener noreferrer">guide by OscarLiang</a> avaiable for further info.

Setup (TX16s Example)
{: .fs-6 .fw-500 }

In EdgeTX, navigate to `Model` -> `Special Functions`.

Add a special function called `SD Logs` and set it to a switch.

<img src="{{ '/assets/images/novalink-65.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

<img src="{{ '/assets/images/novalink-66.bmp' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

Enable this setting and set the `Interval` value to 1.0

Telemetry will be recorded every 1 second. This parameter may be changed but please note that for long flights, this will consume much data.

Now simply activate the switch and the radio controller will start logging telemetry data.

The data will be saved as a `.csv` file under `LOGS` in the radio controller's filesystem.

This data may be processed a number of ways with Python, Excel, Libreoffice Calc, or any other data analytics software.

A good online option may be found <a href="https://maxbl4.github.io/otx/index.html" target="_blank" rel="noopener noreferrer">HERE</a>
