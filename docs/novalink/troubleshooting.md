---
title: Troubleshooting
parent: NOVALINK mLRS Radio System
nav_order: 20
---

# Troubleshooting
{: .d-inline-block }

Refer to the <a href="https://github.com/olliw42/mLRS-docu/blob/main/docs/TROUBLE.md" target="_blank" rel="noopener noreferrer">mLRS Official Documentation for Software Troubleshooting</a>.

For NOVALINK-specific issues, please see below:

Won't Bind
{: .fs-6 .fw-500 }

- Ensure both Tx and Rx are in bind mode by pressing the Bind/DFU button and holding for >4 seconds or until lights flash.

- Ensure Tx and Rx are both getting at least 7.0V.

- Verify firmware, re-flash if necessary with full chip erase (requised DFU mode and STM32CubeProgrammer)

- Verify bind phrase

- Turn off privacy mode

No Power
{: .fs-6 .fw-500 }

- Check voltage with multimeter

- Nominal current should be <300mA for both Rx and Tx. Tx will sometimes be higher if Wireless Bridge is enabled. Ensure proper power supply.

Transmitter Can't Connect with Radio Controller
{: .fs-6 .fw-500 }

- Ensure proper installation of JR Bay Adapter

- Try different ethernet cable

- Try shorter ethernet cable

- Ensure H7 radio is >2.12.4 for EdgeTX

- Update LUA script

Poor RF Range (<10km)
{: .fs-6 .fw-500 }

- Antennas installed incorrectly. Check SWR and measure with antenna in aircraft.

- Calibrate VNA and test antenna again

- Using wrong antenna connectors. Use ONLY SMA-type with NOVALINK.

- RF output power too low

- Noisy RF environment (try to fly away from the city and where people are)

- Radio jammers or Amateur Radio activity on 433MHz band nearby. Verify with spectrum analyzer and directional antenna.

- Electrical noise in power supply going to Tx/Rx. Verify with oscilloscope.

- Obstacles blocking range (ex. building, hill/mountain, etc.)

- Curvature of earth getting in way - move to higher elevation, fly higher.

- Link drops before RSSI is at minimum value - obstacles, noise, poor RF environment degrading signal

- Move Transmitter physically away from radio controller >6ft

- Place radio controller in Faraday Cage. In other words, place it in a tin-foil box. See <a href="https://youtube.com/shorts/lHI9unWujQ0?si=KLJxnrXuJR4S8XNi" target="_blank" rel="noopener noreferrer">RF Testing Example</a>

- Use higher-gain antenna

- Try new coax cable - may be damaged by bending, cracks, etc.

- Do manual range test without attached to aircraft to determine if the airfraft is detuning antenna or introducing noise in to RF system.

- Try different or new Tx and Rx module.

- Try different antenna

- Try different JR Bay Adapter (bad connector - check power)

- RF connectors not screwed in properly

RF Output Power Low
{: .fs-6 .fw-500 }

- Check input voltage (use multimeter)

- Device may be overheating

- RF power meter damaged (ImmersionRF RF Power Meter is notorious for incorrect/low RF power measurements and is also easily damaged in general)

Overheating
{: .fs-6 .fw-500 }

- Verify with thermal camera

- Add heatink

- Add airflow over part

- Check antenna

- Check antenna connection to Tx/Rx

- Lower RF output power and test with power meter

- Attach 50 ohm load instead of antenna to root out antenna impedance mismatch
