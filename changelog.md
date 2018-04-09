# v2.1.0

- add a version option

# v2.0.0

- add `--dd` option to use `dd` instead of mount + `cp`
- drop `rsync` for `cp`
- add `sync` call right after copying to guarantee all writes are flushed to USB device before unmounting with progress indicator
- call `wipefs` before partitionning to cleanup device signature
- eject device after unmounting (can be disabled with `--no-eject` option)
- checkpkg now called for specific options (you don't need all dependencies installed before running)
- safeguard added to check bash version 4+
- better handling of missing dependencies with separation of command name and package name
- refactoring (better naming)

**Breaking changes**

- removed `--no-bootloader` in favor of `--bootloader` (syslinux bootloader disabled by default)

# v1.1.0

- Refactored security checks in selectDrive function
- Use `[ -b "$selectedDrive" ]` to assert device file is of type "block" in selectDrive function
- Start using semantic versioning

# v1.0.2

- Slightly enhanced help message.

# v1.0.1

- Add a help message when script misses argument.