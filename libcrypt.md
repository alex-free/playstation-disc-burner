# [PlayStation Disc Burner](readme.md) -> LibCrypt Patch

PSDB menu options: `Add LibCrypt patch`, `Add LibCrypt patch and burn`.

Patcher used: LibCrypt Patcher ([Github page](https://github.com/alex-free/libcrypt-patcher)).

LibCrypt is an additional copy protection found in some PAL region PS1 games. It is the only additional copy protection type for PS1 that can trigger on MechaPwn'd PS2 consoles. LibCrypt patching removes the protection.

If the input was a CD BIN or CUE file a new directory will be created in the same directory as the input file, ending with `_LCP` containing the LibCrypt patched version of the CD image.

If a compressed file containing supported input files was the input this option will extract the archive to a folder with the same filename, in the same directory of the compressed archive.

## Example: Spyro: Year Of The Dragon (PS1, Europe) + `Patch LibCrypt` Option

![spyro-1](images/spyro-1.png)

![spyro-2](images/spyro-2.png)

![spyro-3](images/spyro-3.png)

![spyro-4](images/spyro-4.png)
