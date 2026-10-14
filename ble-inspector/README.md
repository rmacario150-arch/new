# BLE Inspector

A single-file web page (`index.html`) with two tools for Bluetooth Low Energy devices you own. No dependencies, and nothing leaves your device.

- **Inspect**: connects to a device and shows its services, characteristics, and values. Read-only.
- **Proximity**: listens to a device's broadcasts and shows a live signal-strength reading, a close/far label, a rough distance, a short history graph, and an optional beeping sound that speeds up as you get closer. Needs a browser that supports `watchAdvertisements` (Bluefy does on iPhone). The distance is only a rough guess, so use "Device is 1 m away" to calibrate.

## Use it on a phone

Web Bluetooth needs a secure page (`https://` or `localhost`) and a supporting browser:

- Android: Chrome or Edge.
- iPhone/iPad: Safari does not support it. Use a browser such as Bluefy.
- Desktop: Chrome or Edge.

To use it on a phone the page must be served over HTTPS. The easiest option is to enable GitHub Pages for this repo and open the published URL.

## Your own projects

Browsers only expose services that are named up front. Standard ones (battery, heart rate, device info, ...) are included. For a device you built, paste its service UUIDs into "Custom service UUIDs" before choosing the device.

## Planned next

- Device controller (write to characteristics of devices you own)
