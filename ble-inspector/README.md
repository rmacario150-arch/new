# BLE Inspector

A single-file web page (`index.html`) that connects to a Bluetooth Low Energy device you own and shows its services, characteristics, and values. Read-only. No dependencies, and nothing leaves your device.

## Use it on a phone

Web Bluetooth needs a secure page (`https://` or `localhost`) and a supporting browser:

- Android: Chrome or Edge.
- iPhone/iPad: Safari does not support it. Use a browser such as Bluefy.
- Desktop: Chrome or Edge.

To use it on a phone the page must be served over HTTPS. The easiest option is to enable GitHub Pages for this repo and open the published URL.

## Your own projects

Browsers only expose services that are named up front. Standard ones (battery, heart rate, device info, ...) are included. For a device you built, paste its service UUIDs into "Custom service UUIDs" before choosing the device.

## Planned next

- Proximity tracker (signal strength of your own devices)
- Device controller (write to characteristics of devices you own)
