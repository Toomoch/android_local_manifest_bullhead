LineageOS
===========

Building 17.1 for Nexus 5X
---------------
Follow the [official build guide for 15.1](https://wiki.lineageos.org/devices/bullhead/build#turn-on-caching-to-speed-up-build) until "Turn on caching to speed up build".


Initialize your local repository using the LineageOS trees with a command:
```
repo init --depth=1 -u https://github.com/LineageOS/android.git -b lineage-17.1
```

Clone this repo:
```
git clone https://github.com/Toomoch/android_local_manifests_bullhead .repo/local_manifests -b lineage-17.1
```
Sync LineageOS trees:
```
repo sync --no-tags --no-clone-bundle --force-sync -c -j8
```
**Normal build:**
```
. build/envsetup.sh
lunch lineage_bullhead-userdebug 
mka bacon
```
**or**

**BLOD patched build:**
```
. build/envsetup.sh
lunch lineage_bullhead_blod-userdebug 
mka bacon
```


