<!-- Name Card -->
![x260 Hackintosh](https://cardivo.vercel.app/api?name=x260%20hackintosh&description=ThinkPad%20x260%20running%20macOS&image=https://raw.githubusercontent.com/SuhailSherief/ThinkPad-x260-macOS-OpenCore/main/screenshot/pfp.jpeg&backgroundColor=%22272E&pattern=hideout&colorPattern=%231abc9c&opacity=0.05&fontColor=%23eff4f6)
## Specification
Specification | Configuration
----------- | -----------
Processor | Intel Core i7-6500U
Integrated Graphics | Intel HD Graphics 520
Memory | SK-Hynix 8GB DDR4
Storage | 512GB WD Blue HDD Sata
Wireless Card | Intel AC-8260 Dual Band + Bluetooth
Bootloader | OpenCore
Bootloader Ver. | v0.8.1
## Screenshot
<p align="center">
  <kbd><br>M O N T E R E Y
  <br><br>
  <kbd><img src="https://raw.githubusercontent.com/SuhailSherief/ThinkPad-x260-macOS-OpenCore/main/screenshot/Screen%20Shot%202022-06-21%20at%2012.21.58%20AM.png"/></kbd></kbd>
<p align="center">
  <kbd><br>B A T T E R Y
  <br><br>
  <kbd><img src="https://github.com/SuhailSherief/ThinkPad-x260-macOS-OpenCore/blob/main/screenshot/Screen%20Shot%202022-06-21%20at%2012.31.06%20AM.png"/></kbd></kbd>
</p>
<p align="center">
  <kbd><br>S T A T S
  <br><br>
  <kbd><img src="https://raw.githubusercontent.com/SuhailSherief/ThinkPad-x260-macOS-OpenCore/main/screenshot/Screen%20Shot%202022-06-21%20at%2012.34.49%20AM.png"/></kbd></kbd>
</p>

### Before you start
Follow dortania guide on how to create a recovery usb for MacOS installation.
You can find the MacOS installation guide at the following link, [`Download Here`](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html#downloading-macos)

## MacOS
- Monterey (Tested, OpenCore)
- Bigsur (Tested, OpenCore)
> Airportitwlm needs to be replaced according to the OS version used, the latest airportitwlm default is Monterey.
> The kext file already has airportitwlm for Monterey and Bigsur. Use propertree and enable it in config.plist accordingly.
> To download latest Airportitwlm patch [`click here`](https://github.com/OpenIntelWireless/itlwm/releases)

# Bios
- `Security -> Security Chip`: **Disabled**;
- `Memory Protection -> Execution Prevention`: **Enabled**;
- `Virtualization -> Intel Virtualization Technology`: **Enabled**;
- `Virtualization -> Vt-directed IO`: **Disabled**;
- `Internal Device Access -> Bottom Cover Tamper Detection`: must be **Disabled**;
- `Anti-Theft -> Computrace -> Current Setting`: **Disabled**;
- `Secure Boot -> Secure Boot`: **Disabled**;
- `UEFI/Legacy Boot`: **UEFI Only**;
- `CSM Support`: **No**.

## What's Working?
- QE/CI Intel HD Graphics 5500 `BigSur` `Monterey`
- Power Management `BigSur` `Monterey`
- Sleep, Shutdown, Restart `BigSur` `Monterey` `[sleep not tested]`
- Audio Speaker & Earphone `BigSur` `Monterey`
- Bluetooth `BigSur` `Monterey`
- Trackpad, Trackball, Gestures `BigSur` `Monterey`
- Indikator baterai `BigSur` `Monterey`
- Camera `BigSur` `Monterey`
- etc

# Tips 

Help Fix Screen Sleep

```bash
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```

This will do 5 things for us:

- `Disables` **autopoweroff**: This is a form of hibernation
- `Disables` **powernap**: Used to periodically wake the machine for network, and updates(but not the display)
- `Disables` **standby**: Used as a time period between sleep and going into hibernation
- `Disables` wake from iPhone/Watch: Specifically when your iPhone or Apple Watch come near, the machine will wake
- `Disables` **TCP Keep Alive** mechanism to prevent wake ups every 2 hours

## Credits:
- [Ikhsaan](https://github.com/exxncss) my cool teacher
- [Friction • RK800](https://t.me/gerobaksariroti) help fix some bugs
- [Irawan](https://t.me/irawansalt)
- [Racka](https://github.com/racka98)
- [Vcyzteen](https://github.com/vcyzteen) wallpaper on Post
- [Hackintosh Lover](https://t.me/HackintoshLover)

## Download
click the button below to download EFI
<p align="left">
<a href="https://github.com/zamprjkt/Lenovo-Thinkpad-X250-Hackintosh/releases" target="blank"><img align="left" src="https://raw.githubusercontent.com/zamprjkt/Lenovo-Thinkpad-X250-Hackintosh/Opencore/screenshot/down.png" /></a>
</p>