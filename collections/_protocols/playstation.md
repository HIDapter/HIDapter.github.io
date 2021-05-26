---
title: Playstation
connector: playstation
voltage: 3.6V + 7.6V?
---

# {{ page.title }}

## Pins

### PS1

|Pin|Signal|Dir|Active|Description|
|-|---|---|---|-|
|1|dat|in |pos|data from pad or memory-card|
|2|cmd|out|pos|command data to pad or memory-card|
|3|+7V| - | - |+7.6V power source for CD-ROM drive|
|4|gnd| - | - ||
|5|+3V| - | - |+3.6V power source for system|
|6|sel|out|neg|select pad or memory-card|
|7|clk|out| - |data shift clock|
|8| - | - | - |N.A.|
|9|ack|in |neg|acknowledge signal from pad or memory-card|

1. direction (in/out) is based from PSX
1. metal edge in pad connector is connected to pin 4 and shield cable
1. signal SEL in PAD1, PAD2 is separated

### PS2

1. Brown – Data: Controller -> PlayStation. This is an open collector output and requires a pull-up resistor (1 to 10k, maybe more). (A pull-up resistor is needed because the controller can only connect this line to ground; it can’t actually put voltage on the line).
2. Orange – Command: PlayStation -> Controller.
3. Grey – Vibration Motors Power: 6-9V? With no controller connected, this meausures about 7.9V, with a controller, 7.6V, most websites say this is 9V (except playstation.txt -> 7.6V), although it will still drive the motors down around 4V, although somewhat slower. When the motors are first engaged, almost 500mA is drawn on this line, and at steady state full power, ~300mA is drawn.
4. Black – Ground
5. Red – Power: Many sites label this as 5V, and while this may be true for Play Station 1 controllers, we found several wireless brands that would only work at 3.3V. Every controller tested worked at 3.3V, and the actual voltage measured on a live Playstation talking to a controller was 3.4V. McCubbin says that any official Sony controller should work from 3-5V. Most sites say there is a 750mA fuse for both controllers and memory cards, although this may only apply to PS1’s since 4 dual shock controllers could exceed that easily.
6. Yellow – Attention: This line must be pulled low before each group of bytes is sent / received, and then set high again afterwards. In our testing, it wasn’t sufficient to tie this permanently low–it had to be driven down and up around each set. Digitan considers this a “Chip Select” or “Slave Select” line that is used to address different controllers on the same bus.
7. Blue – Clock: 500kH/z, normally high on. The communication appears to be SPI bus. We’ve gotten it to work from less than 100kHz up through 500kHz (500k bits / second, not counting delays between bytes and packets). When the guitar hero controller is connected, the clock rate is 250kHz, which is also the rate the playstation 1 uses.
8. White – Unknown
9. Green – Acknowledge: This normally high line drops low about 12us after each byte for half a clock cycle, but not after the last bit in a set. This is a open collector output and requires a pull-up resistor (1 to 10k, maybe more). playstation.txt says that the playstation will consider the controller missing if the ack signal (> 2us) doesn’t come within 100us.

## Protocol

## Reference
- https://www.raphnet.net/electronique/psx_adaptor/Playstation.txt
- https://gamesx.com/controldata/psxcont/psxcont.htm
- https://store.curiousinventor.com/guides/PS2
- https://scanlime.org/2008/07/playstation-2-dual-shock-protocol-revisited/
- https://github.com/rafalgrodzinski/gamepad-adapter
