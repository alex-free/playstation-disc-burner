# [PlayStation Disc Burner](readme.md) -> Master Disc Patch

The PSDB menu options `Add Master Disc patch` and `Add Master Disc patch and burn` for DVD ISO files creates a new Master Disc patched ISO file in the same folder as the input file, sharing the same name as the original ISO file but ending with `_MD.iso` or `_MD.ISO` to differentiate it. For CD BIN/CUE files found in a compressed archive, a new folder will be created in the same directory as the input file, ending with `_MD`. If the CD BIN/CUE files are not from a compressed archive, the new directory will instead be created in the parent directory of the input file, also ending with `_MD`. The patcher used is [PS2 Master Disc Patcher](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-393254).

Master Disc patched PS2 disc images when burned to a CD-R or DVD-R read like real games on PS2 consoles set to DEX, **which can be done with MechaPwn for any SCPH-50000 or newer PS2 console model.** To boot Master Disc patched PS2 game on consoles set to DEX with MechaPwn

*  Boot the game with the uLaunchELF/wLaunchELF `PS2Disc` option (`misc`->`PS2Disc` in menu)

*  Turn on `Fast Boot` in FreeMCBoot's configuration options. This allows you to simply have the burned disc boot if it is already in the console when powering it on.

*   Use FreeMCBoot's `Launch Disc` option.

PS1 Discs do not need to be Master Disc Patched to work on PS2 consoles set to DEX, they simply boot like real PS1 discs. 

## Example: BloodRayne + `Add Master Disc patch and burn` Option

![bloodrayne-1](images/bloodrayne-1.png)

![bloodrayne-2](images/bloodrayne-2.png)

![bloodrayne-3](images/bloodrayne-3.png)

![bloodrayne-4](images/bloodrayne-4.png)

![bloodrayne-5](images/bloodrayne-5.png)

## Example: TimeSplitters Master Disc Patch And Burn

![ts-1](images/ts-1.png)

![ts-2](images/ts-2.png)

![ts-3](images/ts-3.png)

![ts-4](images/ts-4.png)

![ts-5](images/ts-5.png)

![ts-6](images/ts-6.png)