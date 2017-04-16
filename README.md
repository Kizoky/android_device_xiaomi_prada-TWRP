## TWRP device tree for Xiaomi Redmi 4 (prada)

Add to `.repo/local_manifests/prada.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/xiaomi/prada" name="android_device_xiaomi_prada" remote="Kizoky" revision="android-6.0" />
</manifest>
```
Then run `repo sync` to download the git.

OR
Download `android_device_xiaomi_prada` as ZIP, and extract ALL files to `../device/xiaomi/prada`

To build:

```sh
. build/envsetup.sh
lunch omni_prada-eng
```
Jx (x is how many cores your CPU have)
```sh
make -j4 recoveryimage
```
If you are unsure, just build it with 1 core only
```sh
make -j1 recoveryimage
```
Building takes approx. 10-11 minutes (It depends on your CPU, and how many cores you use to build)

Kernel sources for Prada is still not released by Xiaomi.

Bugs:
```xml
-"Failed to unmount '/system' (Device or resource busy)"
```
