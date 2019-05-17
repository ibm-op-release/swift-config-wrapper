# swift-config-wrapper

**This repository creates the latest configuration files necessary to build OpenPower code for a Swift system:**
* swift_defconfig (used by 'op-build' repo)
* swift.config (used by 'hostboot' repo)

## Building a Swift Image

### To build an image for a Swift system from scratch:

```
git clone --recursive  https://github.com/ibm-op-release/swift-config-wrapper.git
cd swift-config-wrapper
./setup_swift
cd op-build
. op-build-env && op-build swift_defconfig && op-build
```

### To build an image for a Swift system from an existing op-build

```
git clone --recursive  https://github.com/ibm-op-release/swift-config-wrapper.git
cd swift-config-wrapper
./setup_swift --op-build-dir=/<path>/<to>/<existing>/op-build
cd /<path>/<to>/<existing>/op-build
. op-build-env && op-build swift_defconfig && op-build
```


NOTE:
* Run "./setup_swift -h" to see all options for the setup script
* See https://github.com/open-power/op-build/blob/master/README.md for more information on building an op-build repo.

