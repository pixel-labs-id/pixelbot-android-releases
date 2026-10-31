# 🤖 PixelBot Android Releases Repository

Official APK distribution and update repository for PixelBot Android (`pixel-labs-id/pixel-bot`).

This repository hosts official production APK builds, release notes, and manifests consumed directly by PixelBot's built-in In-App Auto-Updater on Android devices.

---

## 📦 Release Asset Specifications

For the In-App Updater to automatically detect, download, and verify APK releases, every GitHub Release in this repository adheres to the following naming format:

| Platform | Architecture | Asset File Name | Type | Notes |
|---|---|---|---|---|
| Android | ARM64 (`arm64-v8a`) | `PixelBot-<version>-android-arm64.apk` | Signed APK Package | Production signed APK package |
| All | Integrity Manifest | `checksums.txt` | Text / SHA-256 | SHA-256 integrity digests |
| All | Gatekeeper Policy | `release-manifest.json` | JSON Metadata | Version gatekeeper and mandatory update flags |

---

## 🔒 Security & Integrity Verification

Every release includes a `checksums.txt` file containing SHA-256 checksums generated during packaging:

```bash
# Example verification:
shasum -a 256 -c checksums.txt
```

---

© Pixel Labs ID. All rights reserved.
