# 4BitLED_Module-74HC595_NUCLEO_F411RE
NUCLEO-F411RE | Half-Duplex 4-Digit Display Interface & Real-Time Data Visualization

🔹 Project Overview
This implementation demonstrates a compact, industrial-grade data visualization solution using the STM32 NUCLEO-F411RE platform. A 4-digit seven-segment LED module, driven through a 74HC595 shift-register chain, is interfaced using a half-duplex, master-controlled serial protocol operating at 1–4 MHz.

🔹 Functional Scope
✔ Acquisition of real-time analog signal using the onboard 12-bit ADC (2.4 MSPS precision engine)
✔ Conversion of 0–3.3 V input range into ~0.8 mV resolution
✔ Display of:
• Scaled ADC sensor value
• Programmable counter sequence
• Internal die-temperature reading

🔹 Display Architecture
✦ Digit-by-digit multiplexing @ ~1 ms refresh assures persistence-of-vision rendering
✦ led4d.c / led4d.h manage:
• Segment encoding
• SPI burst updates
• Timing loops
• Integer-to-segment translation

🔹 Firmware Stack
💠 Application engine in main.c performs:
• ADC sampling logic
• calibration scaling
• multi-source value formatting
• display scheduling

💠 The architecture provides deterministic timing suitable for automation dashboards and portable diagnostic tools.

🔹 Industrial Relevance
▪️ Reduced wiring complexity using half-duplex signaling
▪️ Excellent for embedded panels, meters, operator consoles, field calibration units
▪️ Easily extendable to alarm annunciation, production counters, test fixtures, and data logging console add-ons.

✔ Result
This project offers a scalable real-time HMI reference architecture for multi-parameter numeric display applications — combining high-speed ADC, compact LED interfacing, calibrated value processing, and deterministic embedded timing execution.
