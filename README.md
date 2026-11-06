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
