<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This project implements a SPI-controlled PWM peripheral. It features:
- SPI interface for configuration (SCLK, COPI, nCS)
- 16 PWM outputs with individual enable control
- Configurable duty cycle (0-255 = 0-100%)
- 3 kHz PWM frequency

## How to test

1. Configure output enables via SPI registers 0x00-0x03
2. Set PWM duty cycle via register 0x04
3. Monitor outputs with an oscilloscope or logic analyzer
4. Use provided test bench to verify:
   - PWM frequency (3 kHz ±1%)
   - Duty cycle accuracy
   - Output enable functionality

## External hardware

No external hardware required for basic testing. For hardware validation:
- Logic analyzer or oscilloscope to verify PWM signals
- SPI master device for control (can be FPGA, microcontroller, etc)
