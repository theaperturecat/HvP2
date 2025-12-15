# HvP2
Fork of Xbox 360 HvP2 source to allow loading of debug builds

This fork is modified for use with [BetterXBDM](https://github.com/theaperturecat/BetterXBDM)

HvP2 - This project allows you to play debug builds of games that previously won't launch.

How does it work? This project patches the Hypervisor function 'HvxResolveImports' to continue instead of erroring a '0xC0000225' HRESULT due to not being able to find a function import address.

We also hook 'XexpCompleteLoad' in the xboxkrnl.exe. 'XexpCompleteLoad' is used to apply patches to the modules loading and to print out the HRESULT for any error's while debugging.
