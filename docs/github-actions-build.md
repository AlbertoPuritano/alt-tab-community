# GitHub Actions releases

This fork has a no-secrets workflow at `.github/workflows/release.yml` for creating GitHub Releases with a zipped `AltTab.app` attached.

## Create a release

Create and push a version tag:

```zsh
git tag v1.0.0-community.1
git push origin v1.0.0-community.1
```

GitHub Actions will run **Release**, build the app, create a GitHub Release named `AltTab Community v1.0.0-community.1`, and attach `AltTab-v1.0.0-community.1.zip`.

You can also create a release from the GitHub UI:

1. Go to **Actions** → **Release**.
2. Click **Run workflow**.
3. Enter a tag such as `v1.0.0-community.1`.
4. Leave **pre-release** enabled for unsigned/not-notarized community builds, or disable it if you later add Developer ID signing and notarization.

GitHub shows the repository's **Releases** section as soon as the first release exists.

If the release build fails, open the failed run summary first. The workflow prints the matching `xcodebuild` diagnostics there and uploads an `xcodebuild-log-<tag>` artifact with the full raw log.

## Signing

The release workflow creates a temporary self-signed `Local Self-Signed` certificate inside the runner keychain, then runs the same Debug build command used by `ai/build.sh`. This is enough for community builds and personal testing, but it is not notarized.

For Developer ID signed/notarized public distribution, add a separate signed release workflow only after configuring Developer ID signing, notarization, Sparkle, and release secrets.

Keep the app bundle identifier and signing identity strategy stable unless you also plan a Keychain/license migration.
