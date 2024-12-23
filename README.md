# macOS on ASUS VivoBook X512DA (AMD)

Base EFI built for ASUS x512DA with AMD 3700U with 2GB Vega 10 iGPU according to <a href = https://dortania.github.io/OpenCore-Install-Guide/> Dortania's OpenCore guide. 

## Specifications

Type | Spec
:---------|:---------
CPU              | AMD Ryzen™ 7 3700U
RAM           | Samsung 8 GB 2400 MHz DDR4
Wi-Fi             | Intel Dual Band Wireless-AC 8265
Audio       | Realtek High Definition Audio ALC 256
SSD       | Kingston 256 Gb

## macOS Update History
- ✅ macOS Sequoia 15.2 (Updated through AppStore)
- ✅ macOS High Sierra (offline installation through this <a href = https://www.reddit.com/r/hackintosh/comments/jrrhox/how_to_make_a_full_offline_installer_for_macos_on/> guide)

## What's working

Type | Status
:---------|:----------
CPU | ✅
AMD GPU Acceleration | ✅
CPU & GPU Power Management | ✅
Audio | ✅
Intel Wi-Fi (you can edit itlwm.kext and manually add your Wi-Fi configuation like SSID and password for online installation) | ✅
Battery Status | ✅
Shutdown / Reboot | ✅
Bluetooth | ✅
Sleep (you can also change through terminal hibernation settings, but anyway will not work as in Windows) | ✅
Microphone | ✅
## What's not working 

Type | Info | Status
:---------|:---------|:----------
Airdrop | Airdrop is not working.|❌
Bluetooth | If bluetooth does not work - reboot.|❌
Audio & Mic | If audio or mic do not work - reboot or try another alcid.|❌


## Notes
Please disable the Secure Boot & Fast Boot in BIOS.

<a href="https://github.com/openintelwireless/itlwm/releases" target="_blank">Airport.kext</a> is not available for this version of macOS yet, and anyway it did not work on this device on older versions, so we use itlwm.kext instead.

Kexts should be replaced according to Dortanias guide, especially when dealing with keyboard & touchpad.

If not booting, change SecureBootModel to Disabled in config.plist. Information regarding this can be found <a href = https://dortania.github.io/OpenCore-Post-Install/universal/security/applesecureboot.html#securebootmodel>here.

Add drivers and do not disrupt the original driver order.

For every change in OC folder, I recommend to use <a href = https://github.com/corpnewt/ProperTree> Propertree, but please do not forget to do OC Snapshot.

Please use GenSMBIOS to generate your three codes and change them!!!

Chrome-based applications like Google Chrome or Steam will cause graphical artefacts amongst other problems. Your goal in dealing with this is to disable GPU acceleration in app if it gives such an option. In STEAM, you should go to settings disabling internet connection and turn off gpu acceleration, for chrome you can start it in terminal as it is shown in <a href = https://chefkissinc.github.io/applehax/nootedred/>NootedRED guide. 


## SSDTs info

You can check in ACPI directory, but I recommend you to recreate new ones exactly for your device according to <a href = https://chefkissinc.github.io/guides/hackintosh/gathering-files/acpi/> this guide 

## Screenshot of the system.

<img src = "macos152.png">
