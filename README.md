# PSN_get_pkg_info.py (c) 2018 by "windsurfer1122"
Extract package information from header and PARAM.SFO of PS3/PSX/PSP/PSV/PSM and PS4 packages.

## Goals
* One-for-all solution to retrieve all header data and PARAM.SFO data from PSN packages
* Decryption of PS3 encrypted data to get all data
* Support of all known package types: PS3/PSX/PSP, PSV/PSM, PS4
* Easy enhancement of interpreting data (=done at the very end with all data at hand)
* Support http download streaming to avoid harddisk usage
* Support multiple output formats
* Support multiple debug verbosity levels
* Easy to maintain and no compiler necessary (=interpreter language)
* Cross platform support
  * Decision: Python 3
    * Compatible with Python 2 (target version 2.7)
      * Identical output
      * Forward-compatible solutions preferred
* Modular and flexible code for easy enhancement and/or extensions (of course there's always something hard-coded left)

## Execution
For available options execute: PSN_get_pkg_info.py -h<br>
Use at your own risk!<br>
If you state URLs then only the necessary bytes are downloaded into memory.

## Requirements
* Python Modules
  * [pycryptodomex](https://www.pycryptodome.org/) (note the X at the end)
  * requests

### Installing on Debian
1. Most Python modules can be installed via apt.<br>
Install Python 3 modules via the following apt packages: python3-requests python3-cryptography.<br>
As Python 2 is the default on Debian and this version should be used, then install apt packages: python-future python-requests python-cryptography.

1. Install pycryptodomex module via pip<br>
   Python 3: `pip3 install pycryptodomex`<br>
   Python 2: `pip2 install pycryptodomex`

### Installing on Windows
1. Install Python<br>
   Checked with Python 3.7 x64 on Windows 10 x64 Version 1803.
   * Get it from the [Python homepage](https://www.python.org/)
   * Install launcher for all users
   * Add Python to PATH<br>
     Adds %ProgramFiles%\Python37 + \Scripts to PATH
   * __Use Customize Installation (!!! necessary for advanced options !!!)__
   * Advanced Options
     * Install for all users

1. Install necessary Python modules
   * Start an elevated(!!!) Command Prompt (Run As Admin via Right Click)
   * Update PIP first: `python -m pip install --upgrade pip`
   * Install requests module: `pip install requests`
   * Install pycryptodomex module: `pip install pycryptodomex`
   * Install cryptography module: `pip install cryptography`
   * Exit Command Prompt: `exit`

Executing python scripts can be done via Windows Explorer or a Command Prompt. Normally no elevation is necessary for script execution, except when the python script wants to change something in the system internals.

## Using a HTTP Proxy with Python
* Linux: `export HTTP_PROXY="http://192.168.0.1:3128"; export HTTPS_PROXY="http://192.168.0.1:1080";`

## Original Source
git master repository at https://github.com/windsurfer1122

## License
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Additional Credits for Ideas and Several Details
* AnalogMan
* https://playstationdev.wiki/ (previously https://vitadevwiki.com/ & https://www.pspdevwiki.com/)
* http://www.psdevwiki.com/
* mmozeiko
* st4rk
* qwikrazor87
