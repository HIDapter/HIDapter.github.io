---
name: Nintendo Gamecube
connector: ngc
voltage: 5V + 3.43V
---

# {{ page.name }}

name={{ page.name }}

title={{ page.title }}

## Pins

|Pin|Cable color|Description|
|-|------|-|
|1|Yellow|5V power supply (used by rumble motor).
|2|Red   |DATA line: bi-directional data to/from console, pull-up to 3.43V
|3|Green |Ground.
|4|White |Ground (Skillz interface has pins 3+4 wired as common ground).
|5|-     |Unknown: not connected by official controller, or Skillz interface.
|6|Blue  |3.43V logic supply.
|7|Black |Cable shielding / ground. Usually common ground with pin 3.

## Protocol

## Reference
- http://www.int03.co.uk/crema/hardware/gamecube/gc-control.htm
