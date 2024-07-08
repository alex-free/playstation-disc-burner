# [PlayStation Disc Burner](readme.md) -> PSX 80 Minute Patch

Menu options: `Add PSX 80 Minute Patch`, `Add PSX 80 Minute Patch and burn`.

Patcher used: PSX80MP ([Github page](https://github.com/alex-free/psx80mp)).

The PSX 80 Minute Patch works around a hardware bug that occurs when reading 80 Minute CD-Rs (disc seek over-run to unburned area causes lock up of optical drive) on early models of PS2 (SCPH-10000-SCPH-390004). It does this by adding dummy data, appended to the end of the disc image. This allows all PS1 games to be burned to 80 Minute CD-Rs and be readable. This patch is useful for affected PS2 console ,odels with either a mod-chip or a soft-mod.

[Tonyhax International](https://github.com/alex-free/tonyhax) has a work-around for this same problem it uses when booting discs on affected PS2 consoles. This work-around allows booting said games burned to 80 Minute media unpatched, but it can not guarantee the game itself won't trigger the same bug during game play (though that hasn't actually happened yet to my knowledge). This patch does.

If the input was a CD BIN or CUE file a new directory will be created in the same directory as the input file, ending with `_PSX80MP` containing the LibCrypt patched version of the CD image.

If a compressed file containing supported input files was the input this option will extract the archive to a folder with the same filename, in the same directory of the compressed archive.

## Example: Kurushi (PS1, Europe) + `Add PSX 80 Minute patch` Option

![ki-1](images/ki-1.png)

![ki-2](images/ki-2.png)

![ki-3](images/ki-3.png)

![ki-4](images/ki-4.png)