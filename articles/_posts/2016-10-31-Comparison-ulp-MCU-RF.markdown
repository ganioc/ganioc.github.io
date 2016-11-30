---
layout: post
title:  Compare ultra low power MCU+RF solutions
date:   2016-10-31 15:28:00 +0800
categories: articles
---
极低耗电的MCU+无线发射器方案比较:

| Brand | Model  | IC dimension | Core |Cost | Power Consumption |
|:-----|:----:|-----| --- |:---:| --- |
| Silicon Labs | Si1010 | 5*7mm, 42pin, LGA | 8051, 25MIPS, 25 MHz clock |   0 | 18mA receive, 18mA@1dBm 30mA@13dBm |
| Nordic | nRF905 |  | 8051 | 0 | 1.9~3.6V, 3mA@16MHz, 30mA@10dBm |
| Microchip | PIC12LF1840T39A | 0 | | | |
| TI | CC1110 | |  |  | MIN 1.8V; |
|SEMTECH | sx1243  |   |   |    | transmitter only   |
| SEMTECH | sx1223 |  |  |     | Min. 2V; transmitter only   |

I plan to use Piezoelectric device to power a 433MHz transmitter. Some tests done. I'd like to test the energy-harvesting technology used in battery-less door-bell solutions. It seems they are not using Piezo for power source, which is too weak energy. They must be using magnet-coil solution which I may take a look later.

I am using:
* MSP430F149 for MCU, which is good, low power as in the datasheet
* 2 piece of Piezo from buzzer
* CC1101 transceiver from TI
* LTC3588-1 from Linear Tech.

The result is: I do succeed to power a single burst of CC1101, output power of 0dBm. But the distance is only within 10 meter inside the office. I have to bend the Piezo about 10 times, which will absolutely prevent using it in the doorbell. I feel a 3.0V coin battery will serve it good for years.

### Pictures:

#### Test setup
<img  src="/assets/images/eh_setup.jpg" alt="test_setup" width="600" />

#### Piezoelectric and energy-harvesting device
It's 2 parallel pieces.
<img src="/assets/images/eh_piezo.jpg" alt="piezo" width="600" />

#### MCU and RF transceiver
<img src="/assets/images/eh_mcu_rf.jpg" alt="MCU&RF" width="600" />

Within 18 ms, the MCU configured the transmitter and send out a burst. The power supply drop from 3.3V to 1.8V. The energy needed is about 2.5V * 12mA * 0.02 = 0.6mJ. I made consumption that the average current is 12mA, but in fact it's not. The energy needed maybe 200uJ instead. Which is very large for a single bend of Piezo copper sheet.












