# Lab1 - Native Binary
Build a native binary for AOSP.

# How to Build
Setup AOSP
```
repo init -u https://android.googlesource,com/platform/manifest -b android-13.0.0_r31
repo sync -j1
source build/envsetup.sh
lunch aosp_arm64-eng
```

Copy the module source and bp to AOSP's tree
```
./configure
```

Build entire project
```
m -j$(nproc)
```

Build just the module
```
m HelloGio
```
