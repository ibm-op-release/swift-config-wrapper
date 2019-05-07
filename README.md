# swift-config-wrapper

**This repository has the latest configuration files necessary to build OpenPower code for a Swift system:**
* swift_defconfig (used by 'op-build' repo)
* swift.config (used by 'hostboot' repo)

## Building a Swift Image

To build an image for a Swift system:

```
git clone --recursive  https://github.com/ibm-op-release/swift-config-wrapper.git
cd swift-config-wrapper
./setup_swift
cd op-build
. op-build-env && op-build swift_defconfig && op-build
```

> See https://github.com/open-power/op-build/blob/master/README.md for more information on building an op-build repo.

## Updating Swift Configuration Files

### Updating swift_defconfig for op-build

**To update swift_defconfig, make changes directly to "create_swift_defconfig.patch".**

"./setup_switch" pulls down the witherspoon_defconfig file and then applies "create_swift_defconfig.patch"
to it to create swift_defconfig.  This allows any overall changes at the op-build level (like a new
custom kernel level) to automatically be picked up when the op-build repo is built.

### Updating the swift.config for hostboot

**Simply make changes directly to "swift.config" and they will be applied when the hostboot repo/package is built.**

