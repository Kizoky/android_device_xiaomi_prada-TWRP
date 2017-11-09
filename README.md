Device configuration for Xiaomi Redmi 4(prada).
==================================================

To do: -Use latest kernel from latest Stable ROM (Stable ROM released later than Dev ROM)

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 1.4 GHz ARM® Cortex™ A53 
CHIPSET | Qualcomm MSM8937 Snapdragon 430
GPU     | Adreno 505
Memory  | 2GB RAM
Shipped Android Version | 6.0.1
Storage | 16GB, 9-11GB usable
Battery | 4100 mAh
Display | 720 x 1280 pixels, 5.0" 
Rear Camera  | 13 MP, 4128 x 3096 pixels, autofocus
Front Camera | 5.0 MP

![Xiaomi Redmi 4](http://cdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-redmi-4-1.jpg "Xiaomi Redmi 4")


Add to `.repo/local_manifests/prada.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/xiaomi/prada" name="android_device_xiaomi_prada" remote="Kizoky" revision="master" />
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
```sh
make -j4 recoveryimage
```
Building takes approx. 10-11 minutes (It depends on your CPU, and how many cores you use to build)

In case of building errors:
```Remove ../frameworks/native-caf```

Kernel sources for Prada is still not released by Xiaomi.
