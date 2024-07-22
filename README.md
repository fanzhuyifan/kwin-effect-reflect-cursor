# kwin-effect-reflect-cursor
This plugin reflects the cursor near screen edges to make it more visible.

## Dependencies
- kwin 6.2. In particular, the patch from https://invent.kde.org/plasma/kwin/-/commit/c6ac6d3caa0ee07256576b87dc9d1d4690620e25 is needed.

## Build
```
cmake -B build -S . -DCMAKE_BUILD_TYPE=Release
cmake --build build
```
## Install
```
cmake --install build
```

## Enable/Disable the effect
Go to System Settings -> Window Management -> Desktop Effects -> Force Cursor Visibility


## Other
Ongoing MR and demonstration at https://invent.kde.org/plasma/kdeplasma-addons/-/merge_requests/601.