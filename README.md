# MeridianFix
Meridian is an iOS 10.x Jailbreak for all 64-bit devices.

MeridianFix is a build of Meridian's `substrate` branch with an updated bootstrap.

- Uses Cydia Substrate instead of Substitute for tweak injection and compatibility
- Installs Zebra v1.1.33 instead of Cydia on initial installation

App version (ipa): https://github.com/LukeZGD/MeridianFix/releases

Web version (TNS): https://lukezgd.github.io/MeridianFix

## Building

Clone repo, open Xcode project, target your device (or generic), and **make sure ldid is in $PATH**. /usr/local/bin, /usr/bin, /bin, ~/bin, whatever, make sure it's present. You'll also need tar, but I'd like to assume everyone has that already ;)
