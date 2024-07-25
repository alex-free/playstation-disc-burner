# PS2 Master Disc Patcher For MechaPwn

_By MottZilla_

Patch CD (bin/cue) or DVD (ISO) images to be detected as 'Master Discs' when read in a PS2 consoles configured as Retail-DEX by the [Mechapwn](https://github.com/MechaResearch/MechaPwn) exploit.

MechaPwn has a 'Force Unlock' configuration that allows burned PS2 discs to be played on exploited consoles. The downside to the 'Force Unlock' configuration is that it breaks DVD video playback, CD audio playback, and PS1 games.

The best work around is to instead use the 'Retail-DEX' configuration. This allows all discs types to work in the PS2 (PS1 games of any region, DVD video, CD audio, real PS2 game discs, etc.) and adds support for PS2 'Master Discs' of any region.

Disc images patched by this patcher may be burned to a CD-R, DVD-R, or DVD+R and can be played once booted by a method other than the normal PS2 OSD. FreeMCBoot's Fast Boot or Launch Disc features, and ULaunchELF's `PS2Disc` boot feature all work great.

## Table Of Contents

*   [Downloads](#downloads)
*   [Usage](#usage)
*   [License](#license)
*   [Credits](#credits)
*   [Building](build.md)

## Downloads

### Version 1.0.5 (7/3/2024) (Alex Free)

*   Fixed patching for [Viewtiful Joe](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-356788). Every other edge case for detecting the boot file name has now been accounted for.

----------------------------

Download v1.0.5 from the [PSX-Place Thread](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3)

[Previous versions](changelog.md)

## Usage

The program expects CD-ROM images to be 2352 bytes per sector format and DVD-ROM to be 2048 bytes per
sector. The program will abort if it doesn't seem to be either of these things. The program may also abort
if it cannot find the system.cnf file. If all goes as expected it will backup the sectors before patching
to either CD_Sectors.bin or DVD_Sectors.bin depending on disc type. These backups should only be needed
if you accidentally patched the wrong file. Otherwise you can ignore it.

Testing Info:

I have tested this patcher with MechaPwn on my SCPH-50001 console with FreeMCBoot. Discs should load via
FastBoot, 'Launch Disc', or ULE's PS2Disc option.

CD-ROM games used for testing were: Gradius III&IV (Usa), Marvel Vs Capcom 2 (Usa). TimeSplitters also worked - Alex Free.
DVD-ROM games used for testing were: Shinobi (Usa), Soul Calibur III (Usa). Max Payne 2 also worked - Alex Free.

You can change the Master Disc region by changing the letter in the region.ini found in the disc image. Valid values are:

*   `J` (Japan)
*   `U` (USA)
*   `E` (Europe)
*   `W` (World)

If Region.ini in the given disc image is missing it will default to USA. I haven't tested if the region setting matters.

It may be possible to patch an image for both ESR and Master Disc if you patch for ESR first. This is
untested. I have not looked into mixing Master Disc patching with FreeDVDBoot patching. If sectors 14&15
are not used then it may be possible.

If you try it and find any games that it can't patch let me know on the [psx-place release thread](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/). It should be pretty solid as long as your ISO images are good. I'd like to know about some of the games people had problems with using the old patcher. Hopefully this one processes them better.

EDC/ECC is regenerated for the patched sectors in bin/cue CD images (it isn't needed for DVD iso files).

## Credits

*   [MechaPwn](https://github.com/MechaResearch/MechaPwn) for the amazing exploit.
*   [Mathias Lafeldt (mlafeldt)](https://github.com/mlafeldt) for the [Master Disc documentation](https://github.com/mlafeldt/ps2logo/blob/master/Documentation/ps2boot.txt).
*   [CDRDAO](https://cdrdao.sourceforge.net/) for the EDC/ECC regeneration code.
*   [Alex Free](https://github.com/alex-free) for v1.0.4 and v1.0.5 update.
