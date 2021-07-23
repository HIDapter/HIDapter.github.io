# Introduction

HID
: Human Interface Device

HIDapter
: HID + adapter

The HIDapter project aims to make it easy to use non-standard input devices by:
- documenting the [physical connections]({% link _docs/connectors.md %}) and [protocols]({% link _docs/protocols.md %})
- implementing portable drivers and adapter [code]({% link _impl/software.md %})
- embracing the [HID standard](https://en.wikipedia.org/wiki/USB_human_interface_device_class): it was initially defined in the [USB specification](https://www.usb.org/hid) and it's widely supported in both USB and Bluetooth

The initial focus is on "retro" videogame controllers, but the scope is open to other kinds of devices.
