## TWRP device tree for LG G5 (International H850)

Add to `.repo/local_manifests/h850.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<remote name="LG-G5" fetch="https://github.com/LG-G5"/>
	<project path="device/lge/h850" name="twrp_device_lge_h850" remote="LG-G5" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```
. build/envsetup.sh
lunch omni_h850-eng
mka recoveryimage
```

Kernel sources are available at: https://github.com/LineageOS/android_kernel_lge_msm8996

