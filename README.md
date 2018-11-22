# Debian stretch deb packages for Apple Swift 4
- [Swift 4.2.1-RELEASE amd64](https://github.com/patrick-zippenfenig/swift-debian-build/releases/tag/4.2.1-RELEASE)

Deb packages can be downloaded and installed with ``dpkg -i <deb-file>``

# Build settings
Unfortunatlly the Apple provided ubuntu packages do not work anymore for Debian stretch since swift 4.2. Packages have been build on Debian stretch with:
```bash
git clone https://github.com/apple/swift.git
./swift/utils/update-checkout --clone --tag swift-4.2.1-RELEASE
./swift/utils/build-toolchain org.swift
```
and packaged with FPM
