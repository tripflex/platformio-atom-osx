# PlatformIO OSX Atom Launcher Application
![platformio-atom-osx](https://raw.githubusercontent.com/tripflex/platformio-atom-osx/master/PlatformIO-atom-osx-icon.png)

**Author:** Myles McNamara
**Version:** 1.0.0

Install this application under your Applications in OSX to launch Atom using `~/.platformio-ide` as `ATOM_HOME` instead of the deafult `~/.atom`.  This allows you to have two separate instances of Atom, one specifically for PlatformIO and one for any other development purposes.

## Why?
I created this because I already use Atom almost everyday for other programming purposes, and only wanted to load the PlatformIO and associated packages when I specifically needed it for PlatformIO Arduino coding purposes.

## How?
This was created using the open source [Platypus](https://sveinbjorn.org/platypus) developer tool (very awesome), and the code in the PlatformIO.sh file.

## FAQ

1.) Can I run both standard Atom and PlatformIO Atom instances together?
Unfortunately, no, not at this time.  Reason being is that it appears if an instance of Atom is already running, when we make the call to open another instance, it uses the same `ATOM_HOME` environment variable that is already set.

2.) How does this application find the Atom.app to use?
Just like in the shell script code used by the core of Atom, spotlight search is used to locate the correct `Atom.app` or whatever custom name you have used (it searches for `com.github.atom` bundle identifier)

3.) It says I have to install Atom, but it's already installed?
Make sure you have moved the file to `Applications` and try again
