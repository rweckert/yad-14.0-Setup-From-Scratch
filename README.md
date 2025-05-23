# yad-14.0-Setup-From-Scratch
Step-by-step setup installation of YAD 14.0+ from scratch.

### Preface:
These instructions provide a step-by-step setup installation of YAD 14.0+ from scratch. The benefits of using YAD 14.0+ are described and illustrated with the following resource: [https://yad-guide.ingk.se](https://yad-guide.ingk.se) by Ingemar Karlsson.

YAD 14.0+ depends on minimal GTK+ version 3.22.0

YAD is authored by Victor Ananjevsky:<br/>
**Homepage:** [https://github.com/v1cont/yad/](https://github.com/v1cont/yad/)<br/>
**News:** [https://github.com/v1cont/yad/blob/master/NEWS](https://github.com/v1cont/yad/blob/master/NEWS)<br/>
**Download YAD 14.1:** [https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip](https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip)<br/>

### Pre-Requisite Setup:

The following items must be installed in order to get the full experience of YAD 14.0+ using GTK+. This is detailed below step by step:

**Pre-Requisite Packages:**
- libwebkit2gtk-4.0-dev
- libgspell-1-dev 
- autoconf
- intltool
- build-essential

Learn more about these pre-requisite packages below in the 'Pre-Requisite Package Information' section.

### Pre-Requisite Installation:

1) Update apt-repository to include "jammy main". This is will be removed once the setup and installation is complete. Issue the following command to add "jammy main" to the apt-repository list:<br/>
_sudo add-apt-repository -y "deb http://gb.archive.ubuntu.com/ubuntu jammy main"_

2) Issue the following command to install: libwebkit2gtk-4.0-dev:<br/>
_sudo apt install libwebkit2gtk-4.0-dev_

3) Issue the following command to install: libgspell-1-dev<br/>
_sudo apt install libgspell-1-dev_

4) Issue the following command to install: autoconf<br/>
_sudo apt install autoconf_

5) Issue the following command to install: intltool<br/>
_sudo apt install intltool_

6) Remove "jammy main" from the apt-repository list:<br/>
_sudo add-apt-repository -r "deb http://gb.archive.ubuntu.com/ubuntu jammy main"_

### YAD 14.1 Installation:

**Homepage:** [https://github.com/v1cont/yad/](https://github.com/v1cont/yad/)<br/>
**Download:** [https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip](https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip)

1) Create a temporary folder and download the following file into that folder:
[https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip](https://github.com/v1cont/yad/archive/refs/tags/v14.1.zip)

2) Navigate to your temporary folder an unpack the downloaded 'v14.1.zip' file using one of the following commands:<br/>
2A) Using unzip: _unzip v14.1.zip_<br/>
2B) Using 7z:    _7z v14.1.zip zipfile.zip_<br/>

3) You should now have a 'yad-14.1' folder. Navigate to that folder using terminal and issue the following commands:

4) Generate build scripts using the following command:<br/>
_autoreconf -ivf && intltoolize_

5) Create configuration using the following command:<br/>
_./configure_

6) Compile configuration using the following command:<br/>
_make_

7) Install the YAD 14.1 package using the following command:<br/>
_sudo make install_

8) Update GTK Icon Cache:<br/>
_sudo gtk-update-icon-cache_

9) Confirm Setup with the following command:<br/>
_yad --about_

You should see the following listed inside the yad about window:

Built with Webkit
Built with GtkSourceView
Built with GSpell
Using GTK+ 3.24.41

![yad --about Screenshot](https://github.com/rweckert/yad-14.0-Setup-From-Scratch/blob/main/yad14.jpg)

### Pre-Requisite Package Information:

**About libwebkit2gtk-4.0-dev:**
[https://packages.debian.org/sid/libwebkit2gtk-4.0-dev](https://packages.debian.org/sid/libwebkit2gtk-4.0-dev)
- WebKit is a web content engine, derived from KHTML and KJS from KDE, and used primarily in Apple's Safari browser. It is made to be embedded in other applications, such as mail readers, or web browsers.

**About libgspell-1-dev:**
[https://packages.debian.org/sid/libgspell-1-dev](https://packages.debian.org/sid/libgspell-1-dev)
- gspell provides a flexible API to add spell checking to a GTK+ application.

**About autoconf:**
[https://www.gnu.org/software/autoconf/](https://www.gnu.org/software/autoconf/)
- Autoconf is an extensible package of M4 macros that produce shell scripts to automatically configure software source code packages.

**About: intltool**
[https://freedesktop.org/wiki/Software/intltool/](https://freedesktop.org/wiki/Software/intltool/)
- intltool is a set of tools to centralize translation of many different file formats using GNU gettext-compatible PO files.

**About: build-essential**
[https://packages.debian.org/sid/build-essential](https://packages.debian.org/sid/build-essential)
- The build-essential package is a reference for all the packages needed to compile a Debian package. It generally includes the GCC/g++ compilers and libraries and some other utilities.

### Resources:
- [https://smokey01.com/yad/](https://smokey01.com/yad/)
- [https://yad-guide.ingk.se/](https://yad-guide.ingk.se/)
- [https://github.com/v1cont/yad](https://github.com/v1cont/yad)
- [https://github.com/v1cont/yad/blob/master/NEWS](https://github.com/v1cont/yad/blob/master/NEWS)
- [https://www.mankier.com/1/yad#Widgets_Names](https://www.mankier.com/1/yad#Widgets_Names)
- [https://forums.bunsenlabs.org/index.php](https://forums.bunsenlabs.org/index.php)
- [https://man.archlinux.org/man/yad.1.en](https://man.archlinux.org/man/yad.1.en)
- [https://man.freebsd.org/cgi/man.cgi?query=yad&sektion=1&manpath=freebsd-release-ports](https://man.freebsd.org/cgi/man.cgi?query=yad&sektion=1&manpath=freebsd-release-ports)
- [https://oldforum.puppylinux.com/viewtopic.php?t=97458](https://oldforum.puppylinux.com/viewtopic.php?t=97458)
- [https://www.forum.puppylinux.com/search.php?keywords=yad](https://www.forum.puppylinux.com/search.php?keywords=yad)
- [https://groups.google.com/g/yad-common/](https://groups.google.com/g/yad-common/)
- [https://eirenicon.org/yad-online-tutorials-etc/](https://eirenicon.org/yad-online-tutorials-etc/)

### Closing:
Setup instructions written by: Robert W Eckert - rweckert@gmail.com
Created: 02-10-2025 Updated: 04-16-2025

These instructions will be updated with comments from the community or when changes occur. Please feel free to email in submitting bugs, changes or requests.

### Project Page: <br/>
[https://github.com/rweckert/yad-14.0-Setup-From-Scratch/blob/f54efa13a25aa8618f5f03d0225772d8a5b32239/README.md](https://github.com/rweckert/yad-14.0-Setup-From-Scratch/blob/f54efa13a25aa8618f5f03d0225772d8a5b32239/README.md)
