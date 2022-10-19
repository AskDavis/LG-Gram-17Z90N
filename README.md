# [LG Gram 17Z90N Hackintosh](https://www.lg.com/us/laptops/lg-17z90n-r.aac8u1-ultra-slim-laptop)
### Opencore Version: 0.8.5
| Specification       | Details                                 |
| ------------------- | --------------------------------------- |
| Model               | LG gram 17 - 2020 (17Z90N)              |
| Processor           | Intel Core i7-1065G7                    |
| Integrated Graphics | Intel® Iris® Plus                       |
| Memory              | 16GB RAM & 512GB SSD                    |
| Sound Card          | Conexant CX8200                         |
| Wireless Card       | Intel® Wi-Fi 6 AX201                    |

# Work In Progress
- I have had this laptop since November, spent so many hours on this (so far I havent found anyone who has had success) and Finally got it to work YAY!
- I am excited to get this fully finished but still have more to do! Will update when I fix whats not working!

![Screenshot](/Images/AboutThisMac-Monterey.png)

## Instructions
### 1. BIOS Settings
- Hold F2 to enter BIOS on boot up
- Press CTRL-ALT-F7 to open Advanced Options
- Main - Boot Features - Quick Boot => Disabled
- Advanced - Intel Advanced Menu - CPU Configuration - Software Guard Extentsions (SGX) => Disabled
- Advanced - Intel Advanced Menu - Power & Performance - "CPU - Power Management Control" - CPU Lock Configuration - CFG Lock => Disabled and Overclocking Lock => Disabled 
- Advanced - Intel Advanced Menu - System Agent (SA) Configuration - Graphics Configuration - DVMT Pre-Allocated => 64M
- Advanced - Intel Advanced Menu - PCH-IO Configuration - USB Configuration - XHCI Compliance Mode => Enabled
- Advanced - Intel Advanced Menu - PCH-IO Configuration - Security Configuration - Force unlock on all GPIO pads => Enabled (Thanks 1OldSWguy)
- Advanced - Intel Advanced Menu - Platform Settings - System Time and Alarm Source => Legacy RTC
- Advanced - Intel Advanced Menu - ACPI Settings - Low Power S0 Idle Capability => Disabled
- Security - Secure Boot Configuration - Secure Boot Option - Disabled
- Exit - Exit Saving Changes

### 2. Generate SMBIOS
- https://github.com/corpnewt/GenSMBIOS
- MacbookPro16,2
- Follow Guide to Add to config.plist - https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html#platforminfo

### 3. Boot Installer
- Boot Opencore, select installer, and Install Big Sur. (Youll have to Create a MacOS Big Sur installer)

## Notes
- The NVME Drive that comes with this Laptop is a SKHynix 512GB which is not supported by Mac OS, Please replace it as it will not boot with it installed. (I bought a WD SN750 500GB that worked great).
- If the system Crashes, Kernal Panics, or you manually shut it down you will have to re-enter BIOS settings above. (Havent figured out how to save them even if it kernal panics)
- Fixed - Graphics glitches when booting then is completely fine after the first 10-20 or so seconds. (Fixed Thanks to 1OldSWguy)

### Working
- WIFI
- Bluetooth
- Sound
- Graphics Acceleration
- Keyboard
- Trackpad
- Battery Settings
- Webcam
- USB-C
- Brightness Keys
- USB

### Partial Working
- USB-C (Sleep Crashes with dock)
  - might be fixed with latest, dont have a dock to test
- Sleep 

### Not Working
- Thunderbolt
- HDMI
- FingerPrint Reader

## Credits
- Thanks [Opencore community](https://github.com/acidanthera/OpenCorePkg)
- Thanks 1OldSWguy
- Thanks daniyo27
