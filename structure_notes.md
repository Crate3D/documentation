Main overview
=============

9 slot of pcie:
 - 1 slot x4 for controller
 - 1 slot x1 for power
 - 7 slot x1 for modules
 
Pcie x1 - 36 pin, pcie x4 - 64 pin

Plasment is [P|C|1|2|3|4|5|6|7]
 - P (Power) - power supply unit: provide 5 and 3.3 volts
 - C (Controller) - main unit with high performace mcu and master unit of everthing communication
 - 1..7 - slave modules of io and drivers

Controller
==========

Pcie slot:
 - 2 spi (4 pin)
 - 2 i2c (2 pin)
 - 2 uart (2 pin)
 - 1 can (2 pin)
 - 7 pin cs (per module)
 - 7 pin reset (per module)
 - 7 pin interrupt (per module)
 - 7 gpio (2 pin) (per module)
 - 4-6 pin power (5 and 3.3 volts + GND)
 - 5 other pins (not used now)

Panel:
  - 2 uart
  - 2 spi
  - 2 i2c
  - 1 can
  - 1 ethernet (optional)
  - 1-2 usb
  - microsd
  - leds
  - buttons

Board:
  - stm32f746 (144, 176, 208 pins)
  - qspi memory chip (optional)
  - ram (optional)
  - battery for rtc
  - buffers for spi/i2c/gpio

Module
======

Pcie slot:
 - 2 spi (4 pin)
 - 2 i2c (2 pin)
 - 2 uart (2 pin)
 - 1 can (2 pin)
 - 1 pin cs
 - 1 pin reset
 - 1 pin interrupt
 - 1 gpio (2 pin)
 - 4-6 pin power (5 and 3.3 volts + GND)
 - 12 other pins (not used now)

Board:
 - stm32f4(11,12,14,15) (64, 100 pins) / another logic or special chips
 - digital and/or analog electronic elements
 - buffers and drivers

Panel:
 - another extrenal interface (module specific)