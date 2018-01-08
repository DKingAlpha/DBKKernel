# DBKKernel

This is a fixed version of DBKKernel (known as dbk64.sys, dbk32.sys).

DBKKernel is a subproject in [Cheat Engine](https://github.com/cheat-engine/cheat-engine)

This fixed project is compatible with VS2017 together with WDK for Windows 10 ver 1709.

### Fix Content

SigCheck is removed from source. (For applying driver in UCE)

CETC is removed from source. (We do not need Server-Client CE Arch)

Fix structure member errors related to [wdm.h](file:///C:/Program%20Files%20(x86)/Windows%20Kits/10/Include/10.0.16299.0/km/wdm.h)

i386/noexceptiona.asm is tweaked due to error `Undefined Symbol`. Not sure if it's correct.

### Compile

Prequist: VS2017

Install WDK from [Install WDK for Windows 10, version 1709)](https://developer.microsoft.com/en-us/windows/hardware/windows-driver-kit)

Just ... Open project and go ahead for x64.

\* DBK.inf need to be manaully updated if switched to compile an x86 version. (change filename from *64* to *32*)


### Sign

To use this driver without any system modification, you will need to cross sign the driver. To do that, you need a valid Class 3 cert.

To use this driver in Windows 10 x64 without cross sign, you either need to disable "Driver Signature Enforcement" (one-time), or enable TestMode (permanent)

### Credit

All credits to Cheat Engine and whoever wrote the driver.(Dark Byte?)
