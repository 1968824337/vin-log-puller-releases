# VehicleLogCapture Releases

This public repository contains only release artifacts for VehicleLogCapture.
The source repository stays private.

## Update source

`latest.json` and the installer are published as GitHub Release assets:

```text
https://github.com/1968824337/vin-log-puller-releases/releases/latest
```

The client must use the public GitHub REST API without a token.

## Release assets

Each stable release contains:

```text
VehicleLogCapture-Setup-<version>.exe
latest.json
```

`latest.json` fields:

```json
{
  "schema": 1,
  "version": "4.1.12",
  "url": "https://github.com/1968824337/vin-log-puller-releases/releases/download/v4.1.12/VehicleLogCapture-Setup-4.1.12.exe",
  "sha256": "...",
  "size": 90581663,
  "notes": "Changes in this release",
  "channel": "stable",
  "publishedAt": "2026-11-02T09:00:00+08:00"
}
```

## Publish order

1. Build the installer.
2. Compute SHA256.
3. Create a draft GitHub Release.
4. Upload the installer and `latest.json`.
5. Publish the release.
6. Test auto-check from an older installed build.

Do not publish `latest.json` before the installer is available.
Beta builds must use a separate prerelease and must not be selected by the
stable channel.
