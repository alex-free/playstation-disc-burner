# [PlayStation Disc Burner](readme.md) -> Changelog

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