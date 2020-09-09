LineageOS
===========

Building 17.1 for Nexus 5X
---------------

```
1. mkdir -p mkdir -p ~/android/lineage && cd ~/android/lineage

2. Initialize your local repository using the LineageOS trees with a command
  repo init --depth=1 -u https://github.com/LineageOS/android.git -b lineage-17.1
  
3. Clone this repo:
  git clone https://github.com/Toomoch/android_local_manifests_bullhead .repo/local_manifests -b lineage-17.1

4. Sync LineageOS trees:
  repo sync --no-tags --no-clone-bundle --force-sync -c -j8

5. To build normally:
  . build/envsetup.sh
  lunch lineage_bullhead-userdebug 
  make -j8 bacon

6. To build for BLOD
  . build/envsetup.sh
  lunch lineage_bullhead_blod-userdebug 
  make -j8 bacon
```
