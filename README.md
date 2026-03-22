# blf2mat-releases

Public update metadata and installer distribution repo for BLF to MAT Converter.

Files:

- `version.json`: App update metadata read by the desktop app
- `release_notes.json`: Version-by-version release notes read by the desktop app after updates

Recommended release flow:

1. Create this repo as a public repository.
2. Add release tags like `v1.0.0`.
3. Upload `BlfToMatConverter_Setup.exe` to the matching GitHub Release.
4. Keep `version.json` and `release_notes.json` updated so the desktop app can detect new versions and show cumulative release notes.

If you use the private source repo workflow:

1. Add a fine-grained PAT as `BLF2MAT_RELEASE_PAT` in the private source repo secrets.
2. Give that token access to this repo with at least `Contents: Read and write`.
3. Push a new version to the `release` branch in the private source repo.
4. GitHub Actions will build the installer, update `version.json` and `release_notes.json`, and upload the installer asset here.
