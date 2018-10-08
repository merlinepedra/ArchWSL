# ArtixWSL
Artix Linux on WSL (Windows 10 FCU or later)
based on [wsldl](https://github.com/yuk7/wsldl)


![screenshot](https://raw.githubusercontent.com/wiki/yuk7/wsldl/img/Arch_Alpine_Ubuntu.png)

[![Build Status](https://img.shields.io/travis/hdk5/ArtixWSL.svg)](https://travis-ci.org/hdk5/ArtixWSL)
[![Github All Releases](https://img.shields.io/github/downloads/hdk5/ArtixWSL/total.svg)](https://github.com/hdk5/ArtixWSL/releases/latest)
[![License](https://img.shields.io/github/license/hdk5/ArtixWSL.svg)](https://choosealicense.com/licenses/mit/)


### [Download](https://github.com/hdk5/ArtixWSL/releases/latest) | [Wiki](https://github.com/hdk5/ArtixWSL/wiki)

## Requirements
* Windows 10 1709 Fall Creators Update 64bit or later.
* Windows Subsystem for Linux feature is enabled.

## Install
#### 1. [Download](https://github.com/hdk5/ArtixWSL/releases/latest) installer zip

#### 2. Extract all files in zip file to same directory
Please extract to a folder that has write permission.
For example 'Program Files' can not be used.

#### 3. Run Artix.exe to Extract rootfs and Register to WSL
Exe filename is using to the instance name to register.
If you rename it you can register with a diffrent name.

  **Note:** _Source code for Artix.exe can be found in [yuk7/wsldl](https://github.com/yuk7/wsldl)._

#### 4. Before using pacman, please initialize keyring
```console
# pacman-key --init
# pacman-key --populate
```


## How-to-Use(for Installed Instance)
#### exe Usage
```console
$ Artix.exe help
Useage :
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro. Inherit current directory.

    config [setting [value]]
      - `--default-user <user>`: Set the default user for this distro to <user>
      - `--default-uid <uid>`: Set the default user uid for this distro to <uid>
      - `--append-path <on|off>`: Switch of Append Windows PATH to $PATH
      - `--mount-drive <on|off>`: Switch of Mount drives

    get [setting]
      - `--default-uid`: Get the default user uid in this distro
      - `--append-path`: Get on/off status of Append Windows PATH to $PATH
      - `--mount-drive`: Get on/off status of Mount drives
      - `--lxuid`: Get LxUID key for this distro

    clean
     - Uninstalls the distro.

    help
      - Print this usage message.
```

## Known issues
Please see [Wiki](https://github.com/hdk5/ArtixWSL/wiki).