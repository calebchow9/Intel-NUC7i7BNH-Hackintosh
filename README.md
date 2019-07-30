## Specs
 - Processor: 3.5 GHz i7-7567U (Kaby Lake)
 - Graphics: Intel Iris Plus Graphics 650
 - SSD: Samsung SSD 850 EVO M.2 500 GB (dual-boot Windows/macOS)
 - Memory: 32 GB 2133 MHz DDR4

## Kexts
- AppleALC: fixes audio output
- FakeSMC: essential for booting, SMC emulator
- Lilu/Whatevergreen: graphics patching along with intelframebuffer
- USBInjectAll: fixes USB 2.0/3.0 ports
- IntelMausiEthernet: enables ethernet port for internet access (essential for downloading Mojave)

## BIOS
- DVMT: make sure to allocate 64 MB minimum, 256 MB aperture in 'Devices > Video'
- Disable Network Boot in 'Boot'
- Disable Secure Boot in 'Boot'
- Disable Execute Disable Bit in 'Security'

## Config.plist
- SMBIOS: iMac 18.1 - used for Kaby Lake computers with iGPU
- Audio Layout 1: enable audio
- Device Properties: ig-platform-id 0x59120000 (hex-swap, then convert to base64)
- inject kexts
- inject Intel = false
- BooterConfig set to 0x28
- CsrActiveConfig set to 0x3E7 (to disable SIP)

## Working
- Facetime, iMessage, iCloud
- Graphics acceleration on the Iris 650 Plus
- USB 2.0/3.0 native ports
- HDMI (4k/1080p)
- HDMI audio/headphone jack
- macOS app store


## Not Working
- Wi-fi (wifi card is soldered on, so can't be replaced)
- Bluetooth (also soldered on)

## Screenshots
![Clover Bootloader](https://i.imgur.com/wi50UsP.png)
![Mojave Desktop](https://i.imgur.com/NGOEPch.jpg)
