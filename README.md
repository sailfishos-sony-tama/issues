# Sailfish OS port to Sony Xperia Tama devices

Please read this document fully before planning or starting to use this port.

This is a community port, meaning that there is no official support and extensions included in the paid version:

* There is no Android app support
* There is no MS exchange support
* There is no Jolla Store predictive text support. Use Presage-based keyboards instead (see below)

The port is based on official port for Xperia 10. As a result, it has similar tools available for flashing
and the device userdata is partitioned using LVM.

As it requires unlocking bootloader on Sony Xperia, you will loose DRM keys and associated functionality. See
AOSP9 threads at XDA for your device for details. In particular, camera functionality will be considerably worse
than on stock Android by Sony, but should be similar to AOSP9.

While the care has been taken during porting, please see [LICENSE](LICENSE) for legal details.

## Issues 

Port issues are all reported within this repository: https://github.com/sailfishos-sony-tama/main/issues

## Supported devices

Out of Tama platform devices, the following are supported:

* Xperia XZ2 single sim variant (H8216)

Support for the other devices is expected in future.

## Current state

Port is based on AOSP9 / Linux kernel 4.9.

Software stack state:

* Sailfish 3.2.0.12
* Jolla Store access
* Kernel OTA update works
* OTA update for full OS not tested

Working hardware:

* Display
* Touch, multitouch
* LED
* Audio
* Bluetooth
* GPS
* WLAN (connect and hotspot)
* Camera (as in AOSP9)
* GSM (SMS, voice, data)
* Keys (Vol +/-, camera, power)
* Power management
* USB Charging
* Sensors: light, proximity, gyroscope, acceloremeter
* Vibrator
* SD card

## Flashing

Before flashing, please check the current [issues](https://github.com/sailfishos-sony-tama/main/issues) and 
pay attention to the [critical ones](https://github.com/sailfishos-sony-tama/main/issues?q=is%3Aopen+is%3Aissue+label%3Acritical). The critical issues may damage your hardware, so please
be aware of them.

Flashing guide is at [flashing.md](flashing.md).

## Predictive text support

For predictive text support, install Presage-based predictive keyboards. These keyboards are available 
at OpenRepos, under [sailfish_keyboard applications](https://openrepos.net/user/12231/programs). After enabling OpenRepos,
you will need to enable that repository and install the keyboard layout(s) on your device. All the dependencies will be pulled 
during installation. For example, for English, install 
[English US Keyboard layout](https://openrepos.net/content/sailfishkeyboard/english-us-keyboard-layout-presage-based-text-prediction). 

## Development

Port is developed under https://github.com/sailfishos-sony-tama with the local and OBS builds supported. For setting
up local build, see [HADK](hadk-sony-xz2.md).
