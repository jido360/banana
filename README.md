# Muhammad El Khwaga

Phone diagnosis tools that run in the browser. Read UART logs, run ADB and Fastboot commands, and check device info and temperature, all from Chrome or Edge with nothing to install.

## Pages

| Page | What it does |
| --- | --- |
| `index.html` | Home page |
| `uart-reader.html` | Read live UART logs through a USB-TTL module (Web Serial). Baud rate hints by SoC and a basic error analysis |
| `adb-reader.html` | Phone info (model, Android version, baseband, IMEI, MAC addresses), thermal readings, and Wi-Fi, Bluetooth, cellular and thermal logs (WebUSB ADB) |
| `fastboot-reader.html` | Fastboot device info, bootloader status, and general fastboot commands (WebUSB) |

## Requirements

- Chrome or Edge. Web Serial and WebUSB do not work in Safari or Firefox.
- The page must be opened over HTTPS or `localhost`.
- ADB page: turn on USB debugging on the phone.
- Fastboot page: put the phone in bootloader mode.
- The ADB and Fastboot pages load their libraries from the internet (esm.sh).

## Privacy

Device details such as IMEI, MAC addresses and serial number are shown only in your browser. They are not uploaded anywhere.

## Warning

The Fastboot page includes risky commands (unlock bootloader, lock bootloader, erase user data). They ask for confirmation, but you use them at your own risk. Unlocking the bootloader wipes the phone.

## Status

Work in progress. Login, subscriptions, saved logs and AI analysis are planned and not built yet.

## بالعربية

أدوات تشخيص الهواتف من المتصفح: قراءة سجل UART، وأوامر ADB وFastboot، ومعلومات الهاتف والحرارة. تعمل على Chrome أو Edge فقط.
