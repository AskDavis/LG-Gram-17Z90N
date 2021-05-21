# [LG Gram 17Z90N Hackintosh](https://www.lg.com/us/laptops/lg-17z90n-r.aac8u1-ultra-slim-laptop)

| Specification       | Details                                 |
| ------------------- | --------------------------------------- |
| Model               | LG gram 17 - 2020 (17Z90N)              |
| Processor           | Intel Core i7-1065G7                    |
| Integrated Graphics | Intel® Iris® Plus                       |
| Memory              | 16GB RAM & 512GB SSD                    |
| Sound Card          | Conexant CX8200                         |
| Wireless Card       | Intel® Wi-Fi 6 AX201                    |

## Work In Progress

## Instructions
### 1. BIOS Settings
- Hold F2 to enter BIOS on boot up,
- Press CTRL-ALT-F7 to open Advanced Options
- Main - Boot Features - Quick Boot => Disabled
- Advanced - Intel Advanced Menu - CPU Configuration - Software Guard Extentsions (SGX) => Disabled
- Advanced - Intel Advanced Menu - Power & Performance - "CPU - Power Management Control" - CPU Lock Configuration - CFG Lock => Disabled and Overclocking Lock => Disabled 
- Advanced - Intel Advanced Menu - System Agent (SA) Configuration - Graphics Configuration - DVMT Pre-Allocated => 64M
- Advanced - Intel Advanced Menu - Platform Settings - System Time and Alarm Source => Legacy RTC
- Exit - Exit Saving Changes

### 2. Generate SMBIOS
- https://github.com/corpnewt/GenSMBIOS
- MacbookPro16,2
- Follow Guide to Add to config.plist - https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html#platforminfo

### 3. Boot Installer
- Boot Opencore and select Installer and Install Big Sur.

## Notes
- I am excited to get this to work but still have more to do! will update when i fix whats not working!

- If the system Crashes, Kernal Panics, or you manually shut it down you will have to re-enter BIOS settings above. (Havent figured out how to save them even if it kernal panics)
- Graphics glitches when booting then is Completely Fine after the first 10-20 or so seconds.


### Working
- WIFI
- Blutooth
- Sound
- Graphics Acceleration
- Keyboard
### Partial Working
- USB (Two of the 3 support hot plug)
### Not Working
- Thunderbolt /  USB C
- Trackpad
- HDMI - (not tested)
- Battery Settings
- Webcam
- FingerPrint Reader
- FN keys for brightness

## Credits
- Thanks [Opencore community](https://github.com/acidanthera/OpenCorePkg)