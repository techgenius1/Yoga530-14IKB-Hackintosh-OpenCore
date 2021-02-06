
# Lenovo Yoga 530-14IKB-81EK Hackintosh

macOS Big Sur on Lenovo Yoga 530-14IKB-81EK with OpenCore 0.6.6 EFI folder
<img src="https://github.com/techgenius1/Yoga530-14IKB-Hackintosh-OpenCore/blob/master/BigSurYoga540.png?raw=true" alt="look">

## Configuration

| Specifications      | Detail                                      |
| ------------------- | ------------------------------------------- |
| Computer model      | Lenovo Yoga 530-14IKB-81EK		         |
| BIOS Version        | Lenovo 7QCN44WW                             |
| Processor           | Intel Core i5-8250U Processor               |
| Memory              | 8GB DDR4 2666MHz	                          |
| Integrated Graphics | Intel UHD Graphics 620                      |
| Sound Card          | Realtek ALC255 (layout-id:16)               |
| Wireless Card       | Intel Wireless 3165                         |
| Touchpad            | Synaptics I2C Touchpad                      |



## What's not working (Never will work) ⚠️

- [ ] Fingerprint
- [ ] Touch Screen (including Pen)
- [ ] Nvidia MX130

## Current Status in OpenCore

- Discrete graphic card is not working, since macOS doesn't support Optimus technology
  - Disable it from Bios in order to save power
- Everything else works well

## Installation

### First-time installation

- Please refer to the following installation tutorials
  - [Xiaomi Mi Notebook Pro MacOS Catalina Installation Guide || ENGLISH](https://bit.ly/34biTqw)
- You can refer to the following tutorials for additional configuration
   - https://dortania.github.io/vanilla-laptop-guide/
- You should add Serial Number, UUID, MLB and ROM details to Config -> PlatformInfo -> Generic if you want to get iServices working.

- If you intend to dual boot Windows on the same drive, it is recommended that you install macOS **first** then use BootCamp to install Windows everything should work fine.
- It is highly recommended that you use [ProperTree](https://github.com/corpnewt/ProperTree) or OpenCore Configurator to make any changes to the config.plist in `\EFI\OC`, otherwise you may corrupt the file.
- Add `BOOT` and `OC` folders to your EFI partition.

## FAQ

### My touchpad isn't working after update.

You need to rebuild the kext cache after every system update. Use `Kext Utility.app` or type `sudo kextcache -i /` in `Terminal.app`. Then restart. If this still doesn't work, try to press F9.

### My screen turns to black and has no response during the updating process.

If you have black screen for five minutes and get no response from the device, please force restart your laptop(Long press power button) and choose `Boot macOS Install from ~` entry.


## Credits
- Thanks to [calculous](https://github.com/calculous/Lenovo-Yoga-530-14ikb---Opencore) for providing EFI for Yoga 530
- Thanks to [Acidanthera](https://github.com/acidanthera) for providing [AppleALC](https://github.com/acidanthera/AppleALC), [AppleSupportPkg](https://github.com/acidanthera/AppleSupportPkg),  [Lilu](https://github.com/acidanthera/Lilu), [OcBinaryData](https://github.com/acidanthera/OcBinaryData), [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg), [VirtualSMC](https://github.com/acidanthera/VirtualSMC), [VoodooInput](https://github.com/acidanthera/VoodooInput), [VoodooPS2](https://github.com/acidanthera/VoodooPS2), and [WhateverGreen](https://github.com/acidanthera/WhateverGreen).
- Thanks to [alexandred](https://github.com/alexandred) for providing [VoodooI2C](https://github.com/alexandred/VoodooI2C).
- Thanks to [daliansky](https://github.com/daliansky) for providing [OC-little](https://github.com/daliansky/OC-little), the template for this Readme, many valuable samples in patching SSDT and various ACPI patches for OpenCore.
- Thanks to [jsassu20](https://github.com/jsassu20) for providing samples for [patching the brightness keys i ACPI](https://github.com/jsassu20/OpenCore-HotPatching-Guide/tree/master/17-Brightness%20Shortcut%20Patch).
- Thanks to [Sniki](https://github.com/Sniki) for providing [OS-X-USB-Inject-All](https://github.com/Sniki/OS-X-USB-Inject-All).
- Thanks to [corpnewt](https://github.com/corpnewt) for providing [USBMap](https://github.com/corpnewt/USBMap) and [ProperTree](https://github.com/corpnewt/ProperTree).
- Thanks to [zxystd](https://github.com/zxystd) for providing [IntelBluetoothFirmware](https://github.com/zxystd/IntelBluetoothFirmware).
