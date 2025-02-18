<a href="#">
    <img width="192px" height="192px" src="doc/icon.svg" align="right" />
</a>

# Serial Studio

[![Build Status](https://github.com/Serial-Studio/Serial-Studio/workflows/Build/badge.svg)](https://github.com/Serial-Studio/Serial-Studio/actions/)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/4b6f3ce14a684704980fea31d8c1632e)](https://www.codacy.com/gh/Serial-Studio/Serial-Studio/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Serial-Studio/Serial-Studio&amp;utm_campaign=Badge_Grade)
[![Github All Releases](https://img.shields.io/github/downloads/Serial-Studio/Serial-Studio/total.svg)](https://github.com/Serial-Studio/Serial-Studio/releases/)
[![GitHub Latest Release](https://img.shields.io/github/downloads/Serial-Studio/Serial-Studio/latest/total.svg)](https://github.com/Serial-Studio/Serial-Studio/releases/latest)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate?hosted_button_id=XN68J47QJKYDE)

Serial Studio is a multi-platform, multi-purpose serial data visualization program. The goal of this project is to allow embedded developers & makers to easily visualize, present & analyze the data generated by their projects and devices, without the need of writing specialized computer software for each project.

The need for this project arose during the development of the Ground Station Software for several CanSat-based competitions in which I participate. It's simply not sustainable to develop and maintain different GSS programs for each competition & project. The smart solution is to have one common Ground Station software and let each CanSat define how the data is presented to the end user by using an extensible communication protocol.

Furthermore, this approach can be extended to almost any type of project that involves some kind of data acquisition & measurement. If you want a more in-depth explanation of why this project exists, and what its all about, check [this blog post](https://www.alex-spataru.com/blog/introducing-serial-studio).

Serial studio started out receiving data over a hardware serial port, but can now receive data over serial, MQTT and websockets (TCP/UDP).

**NOTE:** Information regarding the communication protocol is provided in the [wiki](https://github.com/Serial-Studio/Serial-Studio/wiki/Communication-Protocol).

*Read this in other languages*: [Español](README_ES.md) [简体中文](README_ZH.md) [Deutsch](README_DE.md)

![Software usage](doc/app-usage.gif)

## Install

You can [download](https://github.com/Serial-Studio/Serial-Studio/releases/latest) and install Serial Studio for your preferred platform.

GNU/Linux users must enable the `executable` flag before attempting to run the application:

```bash
chmod +x SerialStudio-1.0.21-Linux.AppImage
./SerialStudio-1.0.21-Linux.AppImage
```

### Prebuilt Linux packages

Arch Linux users can install [serial-studio-git](https://aur.archlinux.org/packages/serial-studio-git/) from the aur, e.g. with [aurutils](https://aur.archlinux.org/packages/aurutils/):

```bash
aur fetch serial-studio-git
aur build
sudo pacman -S serial-studio-git
```

## Licence

This project is released under the MIT license, for more information, check the [LICENSE](LICENSE.md) file.

## Development

#### Requirements

The only requirement to compile the application is to have [Qt](http://www.qt.io/download-open-source/) installed in your system. The desktop application will compile with Qt 5.15 or greater. You will also need to have the following Qt non-LGPL modules installed:

- Qt Charts

On GNU/Linux systems, you will also need to install `libgl1-mesa-dev` in order to compile the application.

Full list of used Qt modules:

- Qt SQL
- Qt Quick
- Qt Widgets
- Qt Charts
- Qt Serial Port
- Qt Quick Controls
- Qt Quick Controls 2
- Qt Graphical Effects

#### Cloning

This repository makes use of [`git submodule`](https://git-scm.com/book/en/v2/Git-Tools-Submodules). In order to clone it, execute these commands on your Terminal:

	git clone https://github.com/Serial-Studio/Serial-Studio
	cd Serial-Studio
	git submodule init
	git submodule update

Alternatively, just run:

	git clone --recursive https://github.com/Serial-Studio/Serial-Studio

#### Compiling the application

Once you have Qt installed, open *Serial-Studio.pro* in Qt Creator and click the "Run" button.

Alternatively, you can also use the following commands:

	qmake
	make -j4
	
## Tipping

If you find Serial Studio suitable for your needs, please consider [giving me a tip through PayPal](https://www.paypal.com/donate?hosted_button_id=XN68J47QJKYDE). Or, if you prefer to buy me a drink *personally* instead, just [send me a DM](https://instagram.com/aspatru) when you visit [Querétaro, Mexico](https://en.wikipedia.org/wiki/Querétaro), where I live. I look forward to meeting you!


