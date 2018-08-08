# HeyYouMIDI
## macOS audio unit v3 MIDI

You can validate the plugin from the command line with *auval*.

```
auval -strict -v aumi hymd gend
```

For example
```
[gene@rockhopper:][~]$ auval -v aumi hymd gend

AU Validation Tool
Version: 1.6.1a1
Copyright 2003-2013, Apple Inc. All Rights Reserved.
Specify -h (-help) for command options

--------------------------------------------------
VALIDATING AUDIO UNIT: 'aumi' - 'hymd' - 'gend'
--------------------------------------------------
ERROR: Manufacturer OSType should have at least one non-lower case character: 'gend'
Manufacturer String: Gene De Lisa
AudioUnit Name: HeyYouAU
Component Version: 1.6.0 (0x10600)

* * FAIL
```
In this case, I updated the extension's info.plist to correct the "error". it seems iOS doesn't care about this uppercase thing.
