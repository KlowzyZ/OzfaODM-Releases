# Özfa ODM — binary releases

This repository is the **binary release channel** for **Özfa ODM — ONVIF & CCTV Service Utility**, developed by
**KLOWZY** (https://klowzy.com).

It contains **no source code**. Builds are published here as GitHub Releases only.

## Downloading

Open **[Releases](../../releases)** and download the Setup for the newest build:

- `OzfaODM-Setup-<version>-x64.exe` — the installer (Windows 10/11 x64, per-user, no administrator rights needed)
- `SHA256SUMS.txt` — SHA-256 checksums of every file in the release

Current builds are **Alpha pre-releases** for testing. They are not code-signed yet, so Windows SmartScreen may
warn before the first run (More info → Run anyway). Verify the checksum if in doubt:

```powershell
Get-FileHash .\OzfaODM-Setup-<version>-x64.exe -Algorithm SHA256
```

## Uninstalling

Settings → Apps → Installed apps → **Özfa ODM** → Uninstall. Your settings in
`%LocalAppData%\KLOWZY\OzfaODM` are kept so that reinstalling or upgrading preserves them; delete that folder to
remove them too.

## Reporting problems

Use **About → Copy diagnostics** or **Devices → Export test report** in the app; both are sanitized (no passwords,
user names or machine names). Send the report to KLOWZY.
