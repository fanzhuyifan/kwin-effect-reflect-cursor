# kwin-effect-reflect-cursor
This plugin reflects the cursor near screen edges to make it more visible.

## Dependencies
- kconfig
- kcoreaddons
- kwin
- qt6-base

and these are needed for building:
- cmake
- extra-cmake-modules

## Packages
### Arch Linux
Available in the AUR as [kwin-effect-reflect-cursor-git](https://aur.archlinux.org/packages/kwin-effect-reflect-cursor-git/).

## Build from source
### Build
```
cmake -B build -S . -DCMAKE_BUILD_TYPE=Release
cmake --build build
```
### Install
```
cmake --install build
```

## Enable/Disable the effect
Go to System Settings -> Window Management -> Desktop Effects -> Force Cursor Visibility


## Other
Ongoing MR and demonstration at https://invent.kde.org/plasma/kdeplasma-addons/-/merge_requests/601.