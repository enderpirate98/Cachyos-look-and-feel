# Introduction

Ever wanted to have the aesthetic look and feel of CachyOS but can switch distros? In this guide we will teach you on how to make your Kde Plasma desktop envrionment look and feel like it does on CachyOS itself!

## Prerequisites

- You will need the latest version of Kde Plasma for this to work (As of writing it is 5.27.5)

- And you will optionaly need the Fish shell installed if you also want that wonderful configuration.

## How do I install everything?

First of all download the files needed

```
cd Downloads/
git clone https://github.com/CachyOS/CachyOS-Nord-KDE
git clone https://github.com/CachyOS/char-white
```

Next we will create the directories needed for the theme
```
mkdir -p "${pkgdir}/usr/share/color-schemes"
mkdir -p "${pkgdir}/usr/share/plasma/desktoptheme"
mkdir -p "${pkgdir}/usr/share/plasma/look-and-feel"
```
Move the files we got from earlier to the necessary directories

```
sudo mv CachyOS-Nord-KDE/color-schemes/CachyOSNord.colors /usr/share/color-schemes
sudo mv CachyOS-Nord-KDE/color-schemes/CachyOSNordLightly.colors /usr/share/color-schemes
cd plasma/
sudo mv desktoptheme/CachyOS-Nord-round/ /usr/share/plasma/desktoptheme
sudo mv look-and-feel/com.cachyos.ddh4r4m.nord /usr/share/plasma/look-and-feel
```

Reboot your device and go into your system settings and the global theme should appear in Appearance>Global Theme

### My system looks better but where are my glorious icons?

More to come
