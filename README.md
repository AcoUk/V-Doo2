# V-Doo2

this is obly a temp solution, for all who're not incline to install all the tools needed for the compilation

What is VoodooI2C?

VoodooI2C is a project from Alexandre Daoud

https://github.com/alexandred/VoodooI2C

consisting of macOS kernel extensions that add support for I2C bus devices. The project is split into two main components: the core extension and various other satellite extensions.

The Core

The core is the VoodooI2C.kext kernel extension. This kext is intended to be installed by anyone whose computer requires some form of I2C support. It consists of I2C controller drivers and is responsible for publishing device nubs to the IOService plane.

The Satellites

The satellites are a collection of various kernel extensions that implement support for a specific type of I2C device. An example of a satellite kext is VoodooI2CHID.kext which adds support for I2C-HID devices. Usually a user will install one satellite kext per class of I2C device.

Current Status

The following Intel I2C controllers are fully supported:

INT33C2 and INT33C3 - Haswell era INT3432 and INT3433 - Broadwell era pci8086,9d60, pci8086,9d61, pci8086,a160 and pci8086,a161 - Skylake/Kabylake era The following device classes are fully supported:

I2C-HID devices ELAN devices FTE devices Note that there is sometimes an overlap between device classes. For example, some ELAN devices may also be I2C-HID devices.

Releases

The latest version is release and can be downloaded on the release page.

Compatibility

Please check the compatibility page on the VoodooI2C wiki to find out if your device is compatible. If it is not on the list but you still suspect VoodooI2C may work for you, contact us on our Gitter page.

Documentation and Troubleshooting

Please visit the documentation site for further information how to install and troubleshoot VoodooI2C.

License

This program is protected by the GPL license. Please refer to the LICENSE.txt file for more information

Contributing

We are looking for competent C++, OS X kernel, Linux kernel, I2C, HID etc developers to help improve this project! Here are the guidelines for contributing:

Fork this repository and clone to your local machine Create a new feature branch and add commits Push your feature branch to your fork Submit a pull request upstream
