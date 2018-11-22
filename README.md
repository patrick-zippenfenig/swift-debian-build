# Debian stretch deb packages for Apple Swift 4
- [Swift 4.2.1-RELEASE amd64](https://github.com/patrick-zippenfenig/swift-debian-build/releases/tag/4.2.1-RELEASE)

Deb packages can be downloaded, afterwards installed with ``dpkg -i mb-swift_4.2.1-2_amd64.deb`` and ``apt --fix-broken install`` to install the depended libraries.

To remove run ``apt remove mb-swift`` and ``apt autoremove`` to cleanup no longer required packages.

These swift packages are used in production at [meteoblue](https://www.meteoblue.com) and therefore the prefix ``mb-``

# Build settings
Unfortunatlly the Apple provided ubuntu packages do not work anymore for Debian stretch since swift 4.2. Packages have been build on Debian stretch with:
```bash
git clone https://github.com/apple/swift.git
./swift/utils/update-checkout --clone --tag swift-4.2.1-RELEASE
./swift/utils/build-toolchain org.swift
```
And packaged with FPM.

This process is quite time consuming. If more people get interested in using swift on debian, I will setup a public apt repository.
