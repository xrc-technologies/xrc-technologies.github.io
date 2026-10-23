---
title: MavlinkX
parent: NOVALINK mLRS Radio System
nav_order: 17
---

# MavlinkX Support
{: .d-inline-block }

MavlinkX is supported by NOVALINK systems.

From the <a href="https://github.com/olliw42/mLRS-docu/blob/main/docs/MAVLINKX.md" target="_blank" rel="noopener noreferrer">mLRS Official Documentation on MavlinkX</a>:

MavlinkX is a technology designed to improve upon the original MAVLink protocol. It introduces robust framing and parsing which reduces packet losses to the minimum, and adds per-message compression. Both of these features allow for more efficient use of the link capacity.

MavlinkX is enabled by setting the "Rx Ser Link Mode" parameter in the receiver to "mavlinkx".

Packet Recovery
A major deficiency of the MAVLink protocol is that in the presence of data loss, it is prone to miss MAVLink packets which are actually valid. The packets are correctly and fully received and could provide valid data, but are missed in the parsing of the stream (for a deeper discussion of such topics see here).

Missing valid packets for no reason is highly undesirable, especially given that the bandwidth of long-range links is constrained and needs to be utilized in the most efficient manner. MavlinkX overcomes this issue by reframing the MAVLink messages and using parsing strategies which enables the parser to recover any valid packet from the lossy data stream.

Compression
MavlinkX can also provide compression of the MAVLink data stream. Given the nature of MAVLink data, the average compression rate will range from 10 to 20%, which is not huge but can be very beneficial for low-bandwidth links.

Example: In 19 Hz mode, the data rate of the telemetry stream might be ~ 1150 bytes/s. Enabling MavlinkX would increase the data rate to ~ 1300 bytes/s. This increase would enable an additional 3 ATTITUDE messages per second. Therefore, one could change the stream rate (parameter SRy_EXTRA1) for ATTITUDE messages to 5 Hz from 2 Hz and would have a substantially smoother HUD display.

Note: Compression is enabled only in the 19 Hz mode.
