# [PlayStation Disc Burner](readme.md) -> Changelog

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