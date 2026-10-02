# Özfa ODM — Binary Releases

This repository is the official **binary release and update channel** for **Özfa ODM — ONVIF & CCTV Service Utility**, developed by **KLOWZY**.

Website: https://klowzy.com

It contains **no source code**. Application source is maintained separately; this repository contains only public release artifacts required to install, verify, and update Özfa ODM.

## Current stable release

**Özfa ODM 1.0.0 Stable**

Download it from the repository's **Releases** section:

- `OzfaODM-Setup-1.0.0-x64.exe` — Windows installer
- Portable ZIP — optional portable build
- `SHA256SUMS.txt` — SHA-256 checksums for release artifacts
- `stable.json` + `stable.json.sig` — signed update metadata used by the application's Stable update channel

Özfa ODM supports Windows 10/11 x64.

## Installing and updating

Run the latest `OzfaODM-Setup-<version>-x64.exe`.

Existing installations can be upgraded by running a newer Setup over the installed version. Settings, saved credentials, and trusted device certificates are preserved across normal upgrades.

Özfa ODM also includes **Check for Updates** in the application. Stable builds use the signed Stable update channel from this repository and do not automatically consume Alpha or Release Candidate builds.

## Verify a download

Release artifacts include SHA-256 checksums.

Example:

```powershell
Get-FileHash .\OzfaODM-Setup-1.0.0-x64.exe -Algorithm SHA256
```

Compare the result with the matching value in `SHA256SUMS.txt` on the same release.

The current 1.0.0 installer is not Windows code-signed, so Windows SmartScreen may show a warning on first run. This is separate from Özfa ODM's own signed update metadata and integrity verification.

## Uninstalling

Open:

**Settings → Apps → Installed apps → Özfa ODM → Uninstall**

Application settings under `%LocalAppData%\KLOWZY\OzfaODM` are retained so reinstalling or upgrading can preserve them. Delete that folder manually if you also want to remove the retained settings.

## Diagnostics and problem reports

Inside Özfa ODM you can use:

- **About → Copy diagnostics**
- **Devices → Export test report**

These reports are designed to be sanitized and exclude passwords and other sensitive authentication data.

## Project status

Özfa ODM has completed its Alpha and Release Candidate phases and is now on the **Stable** release channel.

Future versioning follows Semantic Versioning:

- `1.0.x` — maintenance and bug fixes
- `1.x.0` — backward-compatible feature releases
- `2.0.0` — major product generation / breaking changes

---

**Özfa ODM**  
**ONVIF & CCTV Service Utility**  
Developed by **KLOWZY**  
https://klowzy.com
