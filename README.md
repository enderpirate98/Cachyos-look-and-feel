# Introduction

Ever wanted to have the aesthetic look and feel of CachyOS but can't switch distros? In this guide we will teach you on how to make your Kde Plasma desktop envrionment look and feel like it does on CachyOS itself!

## Prerequisites

- You will need the latest version of Kde Plasma for this to work (As of writing it is 5.27.5)
- And fastfetch, exa and exa-fish-completion installed if you want the fish configuration
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

Time for the icons!

```
cd Downloads/
cd char-white/
sudo mv usr/share/icons/char-white /usr/share/icons/char-white
```

Reboot and select the theme in Appearance>Icons

## Don't forget the Sddm theme!

Go to Workspace>Startup and Shutdown>Login Screen and hit `Get New SDDM Themes...` 

A theme store should pop up and just search ``` Dexy-Color-SDDM ``` click install on the one made by L4K1

And switch to it!

With all that installed your system should now look like CachyOS but we all know somthing is missing...

## Fish shell configuration!

Install the Fish shell using the instructions at the bottem of the page for your distro here: https://fishshell.com

After doing all that go ahead and download the CachyOS fish config
```
cd Downloads/
git clone https://github.com/CachyOS/cachyos-fish-config
```

And now we move!

```
sudo mkdir /usr/share/cachyos-fish-config/conf.d/
cd cachyos-fish-config/
sudo mv conf.d/done.fish ~/.config/fish/conf.d
sudo mv cachyos-config.fish /usr/share/cachyos-fish-config/
sudo mv config.fish ~/.config/fish/conf.d/
```

Reboot and see what has changed!

If you have any issues report them to the CachyOS develupment team.

This guide was made by me and you can modify it, just mention enderpirate98 as the origional author. The actual files mentioned in these instructions were not made by me, they were made by the wonderful creators of the CachyOS Linux Distribution and special thanks to the team for giving me the breadcrumbs that I needed to figure out how to write this guide on installing these wonderful cusimizations!
