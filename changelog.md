# [PlayStation Disc Burner](readme.md) -> Changelog

## v1.0.4 (9/27/2025)

*   [playstation-disc-burner-v1.0.4-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.4/playstation-disc-burner-v1.0.4-x86_64.zip) _Portable Release For x86\_64 Linux_.

---------------------------

Changes:

* Updated [EDCRE](https://github.com/alex-free/edcre) to version 1.1.0.

* Updated [Libcrypt Patcher](https://github.com/alex-free/libcrypt-patcher) to version 1.0.9.

* Updated [PS2 Master Disc Patcher](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-409346) to v1.0.6.

* Updated [P7zip-zstd](https://github.com/p7zip-project/p7zip) to git commit 6819e2dc1917e1267babddc6391cea56ead7123d.

* Implemented fixes for an issue where if you [symlink](https://github.com/alex-free/playstation-disc-burner/pull/2) `psdb` to i.e. `/usr/local/bin/psdb` thanks to [brkzlr](https://github.com/brkzlr). Since it had been over a year and I had more plans on how to re-archeticutre the current `psdb` to work under such conditions, I took inspirations/code changes from his original pull request and re-integrated it into the v1.0.4 source tree. But they did point out this issue first and provided fixes which I built upon on v1.0.4 nearly a year later so many thanks to them.

* New default burning mode is **non-RAW**. This change has happened because [_many_](https://gbatemp.net/threads/do-modern-burners-cds-make-lower-quality-ps1-backups.628708/page-12#post-10710761) burners do not support RAW burning mode, and only a [small](https://github.com/alex-free/tonyhax/blob/master/anti-piracy-bypass.md#edc) amount of PSX games require it. **The RAW burning mode can be enabled by specifying `psdb -r yes` to burn such games. I recommend to do this if your burner works with RAW mode. If you have issues burning discs in RAW mode, you can specify `pdsb -r no` to disable RAW mode.**

* Changed how to specify a custom burner config. Instead of i.e. `psdb -burner /dev/sr1`, do `psdb -b /dev/sr1`. This is still an "advanced" feature and `psdb` will find the default burner by default in almost all cases (which is normally `/dev/sr0`).

* Re-compiled the portable build. This fixes [issues](https://github.com/alex-free/playstation-disc-burner/issues/7#issue-3348980745) with Linux distros using GLIB 2.34 which can't load the included STATIC ld loader. Really strange why this ever became an issue.

* Mandated GCC/G++ 13 be used for compilation since cdrtools is broken on GCC 14+.

* Improved build system.

## v1.0.3 (8/7/2024)

*   [playstation-disc-burner-v1.0.3-i686](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.3/playstation-disc-burner-v1.0.3-i686.zip) _Portable Release For i686 Linux (x86 32 bit Pentium or better)_.

*   [playstation-disc-burner-v1.0.3-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.3/playstation-disc-burner-v1.0.3-x86_64.zip) _Portable Release For x86\_64 Linux_.

---------------------------

Changes:

*   Added ability to set a burn speed for CD and DVDs independently. You can have one speed set for CDs, and another for DVDs.

*   Updated [EDCRE](https://github.com/alex-free/edcre) to version 1.0.8.

*   Added ability to set burn speed with command line arguments (`-cds <cd burn speed>` or `-dvds <dvd burn speed>`) without having to give a valid input file first.

*   Added ability to set the burner with command line arguments (`-b <burner>`) without having to give a valid input file first.

*   Fixed setting burner in the DVD ISO options menu.

## v1.0.2 (7/26/2024)

*   [playstation-disc-burner-v1.0.2-i686](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.2/playstation-disc-burner-v1.0.2-i686.zip) _Portable Release For i686 Linux (x86 32 bit Pentium or better)_.

*   [playstation-disc-burner-v1.0.2-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.2/playstation-disc-burner-v1.0.2-x86_64.zip) _Portable Release For x86\_64 Linux_.

---------------------------

Changes:

*   Fixed LibCrypt patcher command not found issue.

## v1.0.1 (7/25/2024)

*   [playstation-disc-burner-v1.0.1-i686](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.1/playstation-disc-burner-v1.0.1-i686.zip) _Portable Release For i686 Linux (x86 32 bit Pentium or better)_.

*   [playstation-disc-burner-v1.0.1-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0.1/playstation-disc-burner-v1.0.1-x86_64.zip) _Portable Release For x86\_64 Linux_.

---------------------------

Changes:

*   Added an option to select a specific burner to use. This is saved to a configuration file used on startup. The Linux default is `/dev/sr0`, but if you have multiple burners this could be `/dev/sr1`, `/dev/sr2`, etc..

*   Added automatic installation of build dependencies for APT Linux systems (Pop!OS, Ubuntu, Debian, etc.) in the `build` script.

*   Added support for building for Linux i686 (x86 32 bit Pentium or better) to the `build` script.

*   Updated burn functions to check for if the user is already root before executing either the `cdrdao` or `cdrecord` executable with `sudo`.

*   Added my [EDCRE](https://github.com/alex-free/edcre) patcher. EDC/ECC is now corrected if it is found invalid in any sectors after the system volume descriptor, where game data lives. Sectors before the system volume descriptor are left untouched as invalid EDC/ECC in those sectors are used in EDC protected PS1 games.

## v1.0 (7/8/2024)

*   [playstation-disc-burner-v1.0-x86\_64](https://github.com/alex-free/playstation-disc-burner/releases/download/v1.0/playstation-disc-burner-v1.0-x86_64.zip) _Portable Release For x86\_64 Linux_.

Changes:

*   Initial release.