#!/bin/sh

echo "Looking for Atom..."
echo "PROGRESS:20%"

MAIN_ATOM_EXEC="$(mdfind "kMDItemCFBundleIdentifier == 'com.github.atom'" | grep -v ShipIt | head -1 )"

sleep .5

if [ -z "$MAIN_ATOM_EXEC" ]; then
	echo "PROGRESS:80%"
	echo "ALERT:Unable to find Atom|Please make sure you have already installed Atom under Applications. Visit atom.io to download, then move to Applications, and rerun this application."
	sleep 1
	echo "QUITAPP"
	sleep 1
	echo "PROGRESS:100%"
else
	echo "PROGRESS:40%"
	echo "Atom found: ${MAIN_ATOM_EXEC}"
	echo "Setting ATOM_HOME to ${HOME}/.platformio-ide"
	export ATOM_HOME="$HOME/.platformio-ide"
	echo "PROGRESS:60%"
	echo "Loading PlatformIO for Atom.."
	$(/${MAIN_ATOM_EXEC}/Contents/Resources/app/atom.sh $@)
	sleep .5
	echo "PROGRESS:100%"
fi
