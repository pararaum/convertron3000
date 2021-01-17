# Convertron3000

Convertron3000 is a graphics converter for Commodore 64 computers.
It runs on 64 bit versions of Linux, MacOS, Windows and other systems supported by Python. 


# Why Convertron3000?

reason | description
---|---
open source | easy to modify and to improve, any useful contribution is highly welcome
portable | available on Linux, MacOS, Windows and any other system supported by Python3
instant preview | just fiddle around with the sliders and see the result before converting


# Usage

Using Convertron3000 is pretty straight-forward:

* Open some image.
* Adjust the sliders or apply an effect.
* Convert to koala or hires format.
* Save the resulting image.


# Brightness palette

Sometimes converted images look better when applying a palette based on brightness values.

* Select "brightness palette" mode.
* Choose one of the presets ("purple", "brown" etc.).

You can also create your own palette like this:

* Edit the .json file: In the .json file you specify the size of your palette and the C64-colors like in one of the examples provided.
* Open your .json file. You find this option in the drop-down menu under "open custom gradient".
* Choose "custom" as your brightness palette.




# File Formats

The multicolor bitmap is stored in the widely-spread KoalaPainter (.koa) format:

* 2 bytes load address
* 8000 bytes raw bitmap data
* 1000 bytes raw "Video Matrix" (screen) data
* 1000 bytes raw "Color RAM" data
* 1 byte background data

The hires bitmap is stored in the widely-spread Advanced Art Studio (.art) format:

* 2 bytes load address
* 8000 bytes raw bitmap data
* 1000 bytes raw "Video Matrix" (screen) data



# Authors

* fieserWolF/Abyss-Connection - *initial work* - [https://github.com/fieserWolF](https://github.com/fieserWolF) [https://csdb.dk/scener/?id=3623](https://csdb.dk/scener/?id=3623)


Acknowledgments

* thanks to [Green/ATW](http://csdb.dk/scener/?id=20695) for spontaneously naming Convertron3000 :)
* thanks to people on [csdb.dk](http://csdb.dk/release/?id=155606) for commenting and giving ideas how to improve
# Getting Started

Convertron3000 comes in two flavors:

- standalone executable for 64-bit systems Linux, MacOS/Darwin and Windows
- Python3 script

## Run the standalone executable

Just download your bundle and enjoy. Keep in mind that only 64bit systems are supported as I could not find a 32bit system to generate the bundle.

### Note for Windows users

If some antivirus scanner puts Convertron3000 into quarantine because it suspects a trojan or virus, simply put it out there again.
It isn`t harmful, I used PyInstaller to bundle the standalone executable for you.
Unfortunately, the PyInstaller bootloader triggers a false alarm on some systems.
I even tried my best and re-compiled the PyInstaller bootloader so that this should not happen anymore. Keep your fingers crossed ;)

### Note for MacOS users

Your system might complain that the code is not signed by a certificated developer. Well, I am not, so I signed the program on my own. 
```
"Convertron3000" can`t be opened because it is from an unidentified developer.
```
You need to right-click or Control-click the app and select “Open”.



## Run the Python3 script directly

Download _convertron.py_ and the whole _resource_ - directory into the same folder on your computer.

### Prerequisites

At least this is needed to run the script directly:

- python 3
- python tkinter module
- python "The Python Imaging Library" (PIL)

On my Debian GNU/Linux machine I use apt-get to install everything needed:
```
apt-get update
apt-get install python3 python3-tk python3-pil
```


# Changelog

## Future plans

- ordered dithering: too high values in ordered dithering modes, slider to control dithering strength
- custom brightness palette editor

Any help and support in any form is highly appreciated.

If you have a feature request, a bug report or if you want to offer help, please, contact me:


[http://csdb.dk/scener/?id=3623](http://csdb.dk/scener/?id=3623)
or
[wolf@abyss-connection.de](wolf@abyss-connection.de)


## Changes in 1.1

- transfered whole code to Python3
- great speed improvement, converts much faster now
- new feature: specify image on the command-line, e.g. "convertron.py picture.jpg"
- standalone executables for 64bit-systems: Linux, Darwin (MacOS) and Windows
- GUI design adjusted for MacOS/Darwin
- numpy library not used any more
- documentation
- custom brightness palette now uses .json format


## Changes in 1.01

- added licenses
- added to github with proper README.md


## Changes in 1.0

- hires mode
- colodore palette
- button: reset color modifiers to default
- start address now in hex
- custom brightness palette (config file)


## Changes in 0.1

- initial release


# License

_Convertron3000 is a graphics converter for Commodore 64 computers._

_Copyright (C) 2021 fieserWolF / Abyss-Connection_

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.
If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/).

See the [LICENSE](LICENSE) file for details.

For further questions, please contact me at
[http://csdb.dk/scener/?id=3623](http://csdb.dk/scener/?id=3623)
or
[wolf@abyss-connection.de](wolf@abyss-connection.de)

For Python3, The Python Imaging Library (PIL), Tcl/Tk and other used source licenses see file [LICENSE_OTHERS](LICENSE_OTHERS).


