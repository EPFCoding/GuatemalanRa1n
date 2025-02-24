# MeridianFix
Meridian is an iOS 10.x Jailbreak for all 64-bit devices.

MeridianFix is a build of Meridian's `substrate` branch with an updated bootstrap.

- Uses Cydia Substrate instead of Substitute for tweak injection and compatibility
- Installs Zebra v1.1.36 instead of Cydia on initial installation

App version (ipa): https://github.com/LukeZGD/MeridianFix/releases

Web version (TNS): https://lukezgd.github.io/MeridianFix

Note: The web app might not work for iOS versions below 10.3.x. It is recommended to use the app instead for iOS 10.0-10.2.1

Note 2: Because MeridianFix still uses v0rtex exploit, jailbreaking is going to take a lot of tries. This is because the success rate of v0rtex is really bad.

## For previously jailbroken devices
If your device was previously jailbroken with Meridian (or other jailbreak tools) and would like to switch to MeridianFix, you may try to do the following steps:

- Note: Replace `mount_apfs` with `mount_hfs` on iOS 10.0-10.2.1
- WARNING: There is a chance for your device to bootloop after doing this procedure. Proceed at your own risk
- A safer version of this is to remove the folders `/Applications/Cydia.app` and `/meridian` while jailbroken, using Filza, SSH, or other jailbroken methods.

1. Run [Legacy iOS Kit](https://github.com/LukeZGD/Legacy-iOS-Kit), go to Other Utilities -> SSH Ramdisk
1. Follow instructions. Once in the SSH Ramdisk, select Connect to SSH
1. Run the following commands:
```
/sbin/mount_apfs /dev/disk0s1s1 /mnt1
rm -rf /mnt1/Applications/Cydia.app /mnt1/meridian
sync
/sbin/umount /mnt1
sync
exit
```
4. Select Reboot Device
5. Once device reboots, jailbreak with MeridianFix instead

## Building

Clone repo, open Xcode project, target your device (or generic), and **make sure ldid is in $PATH**. /usr/local/bin, /usr/bin, /bin, ~/bin, whatever, make sure it's present. You'll also need tar, but I'd like to assume everyone has that already ;)
