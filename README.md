# PlatformIO OSX Atom Launcher Application
![platformio-atom-osx](https://raw.githubusercontent.com/tripflex/platformio-atom-osx/master/PlatformIO-atom-osx-icon.png)

**Author:** Myles McNamara

**Version:** 1.0.0

Run this application in OSX to launch [Atom](http://atom.io) using `~/.platformio-ide` as `ATOM_HOME` instead of the default `~/.atom`.  This allows you to have two separate setups for [Atom](http://atom.io), one specifically for [PlatformIO](http://platformio.org) and one for any other development purposes.

See PlatformIO package discussion for more details and possible other setups and solutions: https://github.com/platformio/platformio-atom-ide/issues/158

## Why?
I created this because I already use [Atom](http://atom.io) almost everyday for other programming purposes, and only wanted to load the [PlatformIO](http://platformio.org) and associated packages when I specifically needed it for [PlatformIO](http://platformio.org) Arduino coding purposes.

## How?
This was created using the open source [Platypus](https://sveinbjorn.org/platypus) developer tool (very awesome), and the code in the `PlatformIO.sh` file.

## FAQ

1. Where do I download it?

   Go to the [Releases](https://github.com/tripflex/platformio-atom-osx/releases) page and download the `PlatformIO.app` file

2. Can I run both standard Atom and PlatformIO Atom instances together?

   Unfortunately, no, not at this time.  Reason being is that it appears if an instance of Atom is already running, when we make the call to open another instance, it uses the same `ATOM_HOME` environment variable that is already set.

3. How does this application find the Atom.app to use?

   Just like in the shell script code used by the core of Atom, spotlight search is used to locate the correct `Atom.app` or whatever custom name you have used (it searches for `com.github.atom` bundle identifier)

4. It says I have to install Atom, but it's already installed?

   Make sure you have moved the file to `Applications` and try again
