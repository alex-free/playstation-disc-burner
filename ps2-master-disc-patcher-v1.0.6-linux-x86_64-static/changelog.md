# [PS2 Master Disc Patcher](readme.md) -> Changelog

## Version 1.0.5 (7/3/2024) (Alex Free)

*   Fixed patching for [Viewtiful Joe](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3#post-356788). Every other edge case for detecting the boot file name has now been accounted for.

----------------------------

Download v1.0.5 from the [PSX-Place Thread](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3)

## Version 1.0.4 (7/1/2024) (Alex Free)

*   [Implementation](build.md) of my [EzRe](https://github.com/alex-free/ezre) build system now allows for Linux i386 and x86_64 releases (in .deb and portable .zip format), and Windows i686 and x86_64 releases (in portable .zip format).
*   Re-formatted source code to a consistent syntax (K&R). Lots of clean up and optimizations.
*   EDC/ECC for CD images is now implemented with a static library.
*   Source is now completely C for Linux releases. Windows releases only use a small bit of C++ for the file picker if no arguments are given (the 'GUI' aspect of the program if you just double click the .exe).
*   `itoa()` replaced with `strncmp()` for same behavior, but now using a C standard function rather then a DEVCPP specific implementation.
*   Implemented my pure C version of `system("pause");` and improved exit handling.
*   Conversion/rewrite of docs in markdown format.
*   Wrote an entire [changelog](changelog.md).

----------------------------

Download v1.0.4 from the [PSX-Place Thread](https://www.psx-place.com/threads/playstation-2-master-disc-patcher-for-mechapwn.36547/page-3)

## Version 1.0.3 (8/17/2022) (MottZilla)

* Fixed issues with some games not patching. ex: Jak 3.

----------------------------

* [PS2 Master Disc v1.0.3](https://www.psx-place.com/resources/playstation-2-master-disc-patcher-for-mechapwn.1219/download?version=2364) _for Windows x86_

## Version 1.0.2 (2/22/2022) (MottZilla)

* Added ECC\EDC Error Correction for CD images.

----------------------------

* [PS2 Master Disc v1.0.2](https://www.psx-place.com/resources/playstation-2-master-disc-patcher-for-mechapwn.1219/download?version=2226) _for Windows x86_

## Version 1.0.1 (2/18/2022) (MottZilla)

* Fixed issues patching problematic DVD images.

----------------------------

* [PS2 Master Disc v1.0.1](https://www.psx-place.com/resources/playstation-2-master-disc-patcher-for-mechapwn.1219/download?version=2211) _for Windows x86_

## Version 1.0 (MottZilla)

* Initial Release.

* [PS2 Master Disc v1.0](https://www.psx-place.com/attachments/ps2_master_v1-0-zip.36248/) _for Windows x86_
