# AltTab Community

A community fork of [AltTab](https://github.com/lwouis/alt-tab-macos) for macOS.

## Why this fork?

The original AltTab project introduced a paid Pro offering, putting some features behind a paywall. While the original project remains open source, I wanted to keep those features accessible without requiring a subscription.

This fork started as a way to make that possible, along with a few practical fixes and a simpler build process.

This is not an actively maintained alternative or a separate development project. It is a fork of the original AltTab, with a few changes for people who want to build and use it with the additional Pro functionality.

## Features

- Based on the original AltTab project.
- Access to the unlimited Pro feature set.
- A few fixes and adjustments.
- A build script to simplify compiling the application locally.

## Requirements

- macOS
- Xcode

No additional dependencies are required.

## Build instructions

### Requirements
- macOS
- Xcode

No additional dependencies are required.

### Build

Clone or download this repository, open Terminal in the project directory, and run:

```bash
./scripts/build-local.sh
```

When the build completes, the application will be located at:

```text
DerivedData/Build/Products/Debug/AltTab.app
```

Open it with:

```bash
open DerivedData/Build/Products/Debug/AltTab.app
```

On launch, an additional screen provides access to the unlimited Pro feature set.

## Releases and code signing

This fork does not currently provide official, Apple-signed and notarized releases.

The application is built locally using Xcode through the included build script. Because the app is not signed with an Apple Developer ID certificate and notarized by Apple, macOS may display security warnings when opening it.

To build your own copy, follow the [Build instructions](#build-instructions) above.

## Credits

All original work belongs to the developers and contributors of [AltTab](https://github.com/lwouis/alt-tab-macos).

This repository is an unofficial fork. It is not affiliated with or endorsed by the original developer.

## License

AltTab remains an open-source project. This fork retains the upstream licensing terms. See [LICENSE](LICENSE) for details.
