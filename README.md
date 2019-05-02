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

