# PlayStation Disc Burner (PSDB) : Patch + Burn PS2 And PS1 Discs On Linux

_by Alex Free_

This is an open source tool kit that allows you to burn PS2 and PS1 backup discs on Linux, with the option of patching the disc image in various ways:

*   [ESR patch](esr.md) PS2 games, and burn them to DVD-R.

*   [Master Disc patch](master-disc.md) PS2 games, and burn them to CD-R or DVD-R.

*   [LibCrypt patch](libcrypt.md) PS1 games, and burn them to a CD-R.

*   [PSX 80 Minute patch](psx80mp.md) PS1 or PS2 games, and burn them to a CD-R.

*   Support for compressed files. If PSDB finds a file ending in `.iso`, `.ISO`, `.cue`, `.CUE`, `.BIN`, or `.bin` in a compressed archive format that p7zip supports it will automatically be extracted and configured for all features.

*   Burn PS2 and PS1 games to CD-R or DVD-R as-is (no patching). PSDB correctly burns EDC/ECC protected PS1 games by default.

*   Save the desired burn speed to a configuration file, which can be set with a PSDB option.

| [GitHub](https://github.com/alex-free/playstation-disc-burner) | [Homepage](https://alex-free.github.io/psdb) |

## Table Of Contents

*   [Downloads](#downloads)
*   [Usage](#usage)
*   [Building From Source](build.md)
*   [License](#license)

## Downloads

### v1.0 (7/8/2024)

*   [playstation-disc-burner-v1.0-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0/playstation-disc-burner-v1.0-x86_64.zip) _Portable Release For x86\_64 Linux_.

Changes:

*   Initial release.

## Usage

1) Download and unzip the latest release.

2) Execute `psdb` with one argument, the input file.

`./psdb <input file>`

You can also drag and drop a disc image onto the `ps2db` file in the release if your Linux desktop environment supports it.

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


## License

PSDB itself is released into the public domain, see the file `licenses/psdb.md`.

PSDB makes use of the following programs listed below, which have their own licenses/terms:

*   [PortableLinuxExecutableDirectory](https://alex-free.github.io/pled) (Public Domain, see the file `licenses/pled.md`).

*   [CDRTools-PLED](https://github.com/alex-free/cdrtools-pled) (CDDL v1.0 AND GPL v2, see the files `licenses/cdrecord-cddl.md` and `licenses/cdrecord-gpl2.md`).

*   [CDRDAO-PLED](https://github.com/alex-free/cdrdao-pled) (GPL v2, see the file `licenses/cdrdao.md`).

*   [PSX80MP](https://github.com/alex-free/psx80mo) (3-BSD, see the file `licenses/psx80mp.md`).

*   [LibCrypt Patcher](https://github.com/alex-free/psx80mo) (3-BSD, see the file `licenses/libcrypt-patcher.md`).

*   [ESRTool-legacy](https://github.com/ali-raheem/esrtool-legacy) (GPL v2, see the file `licenses/esrtool-legacy.md`).

*   [PS2 Master Disc Patcher](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-393254) (by MottZilla, closed source currently).

*   [P7zip-zstd](https://github.com/p7zip-project/p7zip) (GNU LGPL with unRAR license restriction, BSD-3 Clause, and Public Domain), see `licenses/p7zip.md`.