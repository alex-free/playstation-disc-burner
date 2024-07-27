# PlayStation Disc Burner (PSDB) : Patch + Burn PS2 And PS1 Discs On Linux

_by Alex Free_

This is an open source tool kit that allows you to burn PS2 and PS1 backup discs on Linux, with the option of patching the disc image in various ways:

*   [ESR patch](esr.md) PS2 games, and burn them to DVD-R.

*   [Master Disc patch](master-disc.md) PS2 games, and burn them to CD-R or DVD-R.

*   [LibCrypt patch](libcrypt.md) PS1 games, and burn them to a CD-R.

*   [PSX 80 Minute patch](psx80mp.md) PS1 or PS2 games, and burn them to a CD-R.

Additional features:

*   Burn PS2 and PS1 games to CD-R or DVD-R without applying one of the above patches. 

*   Portable Linux releases for i686 and x86_64.

*   Support for compressed files. If PSDB finds a file ending in `.iso`, `.ISO`, `.cue`, `.CUE`, `.BIN`, or `.bin` in a compressed archive format that p7zip supports it will automatically be extracted and configured for all features.

*   Correctly burns EDC protected PS1 games.

*   Corrects EDC and ECC starting at the system volume descriptor of the data track for CD images. Any translation patched bin file or otherwise which doesn't contain correct EDC/ECC in the actual game data will be corrected. EDC protected PS1 games continue to burn correctly with this default, as those games are looking at sectors that are before the volume descriptor.

*   Set the desired burn speed to a configuration file.

*   Set the desired burner (i.e. `/dev/sr0` is the default for Linux) to a configuration file.

| [GitHub](https://github.com/alex-free/playstation-disc-burner) | [Homepage](https://alex-free.github.io/psdb) | [PSX-Place Thread](https://www.psx-place.com/threads/psdb-patch-esr-master-disc-psx80mp-libcrypt-etc-burn-ps2-and-ps1-discs.44156) | [GBATemp Thread](https://gbatemp.net/threads/playstation-disc-burner-psdb-patch-esr-master-disc-psx80mp-libcrypt-etc-burn-ps2-and-ps1-discs.658102) |

## Table Of Contents

*   [Downloads](#downloads)
*   [Usage](#usage)
*   [Building From Source](build.md)
*   [License](#license)

## Downloads

### v1.0.2 (7/26/2024)

*   [playstation-disc-burner-v1.0.2-i686](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.2/playstation-disc-burner-v1.0.2-i686.zip) _Portable Release For i686 Linux (x86 32 bit Pentium or better)_.

*   [playstation-disc-burner-v1.0.2-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.2/playstation-disc-burner-v1.0.2-x86_64.zip) _Portable Release For x86\_64 Linux_.

---------------------------

Changes:

*   Fixed LibCrypt patcher command not found issue.

[Previous versions](changelog.md)

## Usage

`PSDB requires 1 argument.`

`Usage:`

`psdb <input file>`

`<input file>     A file ending in .iso, .ISO, .cue, .CUE, .BIN, or .bin (or a compressed archive containing said files)`

1) Download and unzip the latest release.

2) Execute `psdb` with one argument, the input file.

`./psdb <input file>`

You can also drag and drop a disc image onto the `ps2db` file in the release if your Linux desktop environment supports it. Otherwise you can drag `psdb` into your terminal and then the input file into your terminal and press return.

`<input file>` can be:

*   A PS1 or PS2 CD image BIN file with the extension `.bin` or `.BIN`.
*   A PS1 or PS2 CD image CUE file with the extension `.cue` or `.CUE`.
*   A PS2 DVD image ISO file with the extension `.iso` or `.ISO`.
*   A compressed archive containing any of the files above.

3) Enter option number for desired feature. PSDB will detect what type of file the disc image is and present you with options for either CD-Rs or DVD-Rs depending on the disc image.

![bloodrayne-2](images/bloodrayne-2.png)

![ts-2](images/ts-2.png)

![ki-2](images/ki-3.png)

![spyro-2](images/spyro-3.png)

Note: You will be prompted for root privileges when the burning program is executed in order to prevent buffer under-runs during burning which would result in a coaster. Root privileges also ensure that the burning program can access your burner hardware successfully.

## License

PSDB itself is released into the public domain, see the file `licenses/psdb.md`.

PSDB makes use of the following programs listed below, which have their own licenses/terms:

*   [PortableLinuxExecutableDirectory](https://alex-free.github.io/pled) (Public Domain, see the file `licenses/pled.md`).

*   [EDCRE](https://github.com/alex-free/edcre) (GNU GPL v2, see the file `licenses/edcre.md`.).

*   [CDRTools-PLED](https://github.com/alex-free/cdrtools-pled) (CDDL v1.0 AND GPL v2, see the files `licenses/cdrecord-cddl.md` and `licenses/cdrecord-gpl2.md`).

*   [CDRDAO-PLED](https://github.com/alex-free/cdrdao-pled) (GPL v2, see the file `licenses/cdrdao.md`).

*   [PSX80MP](https://github.com/alex-free/psx80mo) (3-BSD, see the file `licenses/psx80mp.md`).

*   [LibCrypt Patcher](https://github.com/alex-free/psx80mo) (3-BSD, see the file `licenses/libcrypt-patcher.md`).

*   [ESRTool-legacy](https://github.com/ali-raheem/esrtool-legacy) (GPL v2, see the file `licenses/esrtool-legacy.md`).

*   [PS2 Master Disc Patcher](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-393254) (by MottZilla, closed source currently).

*   [P7zip-zstd](https://github.com/p7zip-project/p7zip) (GNU LGPL with unRAR license restriction, BSD-3 Clause, and Public Domain), see `licenses/p7zip.md`.