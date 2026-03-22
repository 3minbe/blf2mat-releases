# blf2mat-releases

Public update metadata and installer distribution repo for BLF to MAT Converter.

Files:

- `version.json`: App update metadata read by the desktop app

Recommended release flow:

1. Build the installer in the private source repo.
2. Create a release in this public repo with tag like `v1.0.0`.
3. Upload `BlfToMatConverter_Setup.exe` to that release.
4. Update `version.json` so the app can detect the new version.
