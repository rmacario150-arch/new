# BLE Inspector

A single-file web page (`index.html`) with two tools for Bluetooth Low Energy devices you own. No dependencies, and nothing leaves your device.

- **Inspect**: connects to a device and shows its services, characteristics, and values. Read-only.
- **Proximity**: listens to the broadcasts of one or more devices (up to 6) and shows, for each, a live signal-strength reading, a close/far label, a rough distance, a short history graph, and an optional beeping sound that speeds up as you get closer. Calibration is remembered on the phone. Needs a browser that supports `watchAdvertisements` (Bluefy does on iPhone). A **Listening mode** setting picks how several devices are tracked: one continuous scan for all of them, each device restarted together, or devices taking turns. Automatic tries the first that works and switches to taking turns if one device keeps going quiet while another is heard. The distance is only a rough guess, so use "Calibrate at 1 m" to calibrate.

Each tracked device card also has:

- **Rename**: give a device a nickname. It is remembered on the phone.
- **Alert**: beeps and flashes the card when the device gets far or goes out of range. The alert tone is two notes, so it sounds different from the proximity beeps.
- **Record**: logs the signal while you walk around, draws a graph, and saves or copies the data as a CSV file.
- **What it broadcasts**: decodes what the device announces in the open (name, services, manufacturer, iBeacon, Eddystone-URL, common Apple message types) and explains what that reveals to anyone nearby.
- **Spots**: save the signal at named places. The card then guesses which spot a device is closest to.

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
