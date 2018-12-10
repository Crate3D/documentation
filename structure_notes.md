Main overview
=============

9 slot of pcie:
 - 1 slot x4 for controller
 - 1 slot x1 for power
 - 7 slot x1 for modules
 
PCIe x1 - 36 pin, PCIe x4 - 64 pin, PCIe x8 - 98 pins

Plasment is [P|C|1|2|3|4|5|6|7]
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
 - 4-5 pin power (5 and 3.3 volts + GND)
 - 8 pin of external power (12 - 24 volts + GND)
 - 3 pin module address (unique for everything slot)

Board:
 - stm32f4(11,12,14,15) (64, 100 pins) / another logic or special chips
 - digital and/or analog electronic elements
 - buffers and drivers

Panel:
 - another extrenal interface (module specific)
 
Power
=====

Pcie slot:
 - 9 pin GND
 - 9 pin VCC (12 - 24 volts) (pass through)
 - 9 pin 5 volts
 - 8 pin 3.3 volts
 - 1 pin Power Good feedback signal

Board:
 - highspeed flyback DC-DC convertors for 5 and 3.3 volts
 - overcurrent and overload protection

Panel:
 - High current pins for VCC connection.
