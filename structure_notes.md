Main overview
=============

9 slot of pcie:
 - 1 slot x4 for controller
 - 1 slot x4 for power
 - 7 slot x4 for modules
 
PCIe x1 - 36 pin, PCIe x4 - 64 pin, PCIe x8 - 98 pins

Plasment is [P|1|2|3|4|5|6|7|C]
 - P (Power) - power supply unit is DC-DC: provide
   - VCC (pass through)
   - 5V
   - 3.3
 - C (Controller) - main unit with high performace mcu and master unit of everthing communication
 - 1..7 - slave modules of io and drivers

Controller
==========

Pcie slot:
 - 2 spi (4 pin)
 - 2 i2c (2 pin)
 - 2 uart (2 pin)
 - 1 can (2 pin)
 - 8 pin cs (per module)
 - 7 pin reset (per module)
 - 7 pin interrupt (per module)
 - 7 gpio (2 pin) (per module)
 - 4-6 pin power (5 and 3.3 volts + GND)
 - 1 pin Power Good feedback signal
 - 3 analog pin (VCC, 5 and 3.3 volts value)

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
 - 6 pin digital power (5 and 3.3 volts + GND)
 - 3 pin module address (unique for everything slot)
 - 40 pin main power (12 - 24 volts + GND)

Board:
 - stm32f4(11,12,14,15) (64, 100 pins) / another logic or special chips
 - digital and/or analog electronic elements
 - buffers and drivers

Panel:
 - another extrenal interface (module specific)
 
Power
=====

Pcie slot:
 - 40 pin of main power (12 - 24 volts + GND)
 - 10 pin digital power (5 and 3.3 volts + GND)
 - 1 pin Power Good feedback signal
 - 1 spi (4 pin)
 - 1 i2c (2 pin)
 - 3 analog pin (VCC, 5 and 3.3 volts value)
 - 5 other pins (not used now)

Board:
 - highspeed flyback DC-DC convertors for 5 and 3.3 volts
 - overcurrent and overload protection

Panel:
 - High current pins for VCC connection.
