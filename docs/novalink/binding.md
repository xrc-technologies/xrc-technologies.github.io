---
title: Binding
parent: NOVALINK mLRS Radio System
nav_order: 2
---

# Binding
{: .d-inline-block }

To bind the NOVALINK radio system, there are multiple ways to do this:

Transmitter Module:

- Press the Bind/DFU button while powered on for ~4 seconds or until the Ethernet Port LEDs start an alternating blinking pattern.
 
- Enter bind mode with 'bind' CLI command.

- Enter bind mode with LUA script.

<img src="{{ '/assets/images/novalink-6.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="1000">

Receiver:

- Press the Bind/DFU button while powered on for ~4 seconds or until the LEDs start an alternating blinking pattern.

- Power cycle the receiver quickly 3 times (wait for power LED to blink 3 times). Upon 4th power-up, the receiver will enter bind mode.

<img src="{{ '/assets/images/novalink-16.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="1000">

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/tree/main" target="_blank" rel="noopener noreferrer">mLRS Official Documentation</a>
