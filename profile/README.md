<div align="center">

<img src="https://raw.githubusercontent.com/peachdev-uz/.github/main/profile/assets/peachdev-logo.jpg" alt="PeachDev" width="440" />

<h3>E-IMZO Integration SDKs</h3>

**Production-ready E-IMZO (national ERI) digital-signature SDKs for iOS, macOS, Android, and Flutter.**

<sub>O'zbekiston ilovalari uchun E-IMZO (ERI) integratsiya SDK to'plami.</sub>

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-peachdev--uz-1a1a1a?style=for-the-badge&logo=github&logoColor=E3C36B)](https://github.com/peachdev-uz)
[![Telegram](https://img.shields.io/badge/Telegram-peachdevuz-1a1a1a?style=for-the-badge&logo=telegram&logoColor=E3C36B)](https://t.me/peachdevuz)

</div>

---

## About

peachdev-uz publishes integration SDKs that let developers add **E-IMZO** — Uzbekistan's national electronic-signature (ERI) system — to their apps, with native implementations of the country's cryptographic standards built in.

The SDKs ship native cryptography for **OzDST 1092-2009** and **OzDST 1106-2009** (plus **GOST 28147** on iOS), along with ready-made signing UI, key import, NFC ID-card reading, QR scanning, USB-token support, and deep-link signing — so you don't have to implement the crypto stack yourself.

**Who is this for?** Developers building iOS, macOS, Android, or Flutter applications in Uzbekistan that need E-IMZO (ERI) digital signing without re-implementing the OzDST 1092/1106 (and GOST 28147 on iOS) cryptography themselves.

The Android, mobile, and Flutter SDKs are maintained by **Yangi Texnologiyalar (YT)** ([yt.uz](https://yt.uz)).

---

## Supported Platforms

[![iOS](https://img.shields.io/badge/iOS-16+-000000?style=for-the-badge&logo=apple&logoColor=white)](#)
[![macOS](https://img.shields.io/badge/macOS-13+-000000?style=for-the-badge&logo=apple&logoColor=white)](#)
[![Android](https://img.shields.io/badge/Android-API%2024+-3DDC84?style=for-the-badge&logo=android&logoColor=white)](#)
[![Flutter](https://img.shields.io/badge/Flutter-3.10+-02569B?style=for-the-badge&logo=flutter&logoColor=white)](#)
[![Swift](https://img.shields.io/badge/Swift-5.9+-F05138?style=for-the-badge&logo=swift&logoColor=white)](#)
[![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](#)

---

## Products & SDKs

| SDK | Platform | Latest | Distribution |
| --- | --- | --- | --- |
| [**eimzo-ios-sdk**](https://github.com/peachdev-uz/eimzo-ios-sdk) | iOS (Swift / SwiftUI) | [![iOS release](https://img.shields.io/github/v/release/peachdev-uz/eimzo-ios-sdk?sort=semver&style=flat-square&color=D4A24E&label=release)](https://github.com/peachdev-uz/eimzo-ios-sdk/releases/latest) | SPM / Swift XCFramework |
| [**eimzo-mac**](https://github.com/peachdev-uz/eimzo-mac) | macOS app | [![macOS release](https://img.shields.io/github/v/release/peachdev-uz/eimzo-mac?sort=semver&style=flat-square&color=D4A24E&label=release)](https://github.com/peachdev-uz/eimzo-mac/releases/latest) | Signed & notarized DMG |
| [**eimzo-mobile-sdk**](https://github.com/peachdev-uz/eimzo-mobile-sdk) | Android (Kotlin) | [![Android release](https://img.shields.io/github/v/release/peachdev-uz/eimzo-mobile-sdk?sort=semver&style=flat-square&color=D4A24E&label=release)](https://github.com/peachdev-uz/eimzo-mobile-sdk/releases/latest) | Gradle / Maven (AAR) |
| [**eimzo_flutter**](https://github.com/peachdev-uz/eimzo_flutter) | Flutter plugin | [![Flutter release](https://img.shields.io/github/v/release/peachdev-uz/eimzo_flutter?sort=semver&style=flat-square&color=D4A24E&label=release)](https://github.com/peachdev-uz/eimzo_flutter/releases/latest) | pubspec dependency |

---

## Quick Start

### iOS — `eimzo-ios-sdk`

Add the package in `Package.swift`:

```swift
.package(url: "https://github.com/peachdev-uz/eimzo-ios-sdk", from: "1.0.0")
```

To add it from Xcode's package manager, paste this URL: `https://github.com/peachdev-uz/eimzo-ios-sdk`

Manual install: download `EimzoSDK.xcframework` from [Releases](https://github.com/peachdev-uz/eimzo-ios-sdk/releases/latest) and add it to Xcode with **Embed & Sign**.

### Android — `eimzo-mobile-sdk`

Add the GitHub-hosted Maven repository and the dependency in Gradle:

```gradle
maven { url 'https://raw.githubusercontent.com/peachdev-uz/eimzo-mobile-sdk/main/maven/' }

implementation 'uz.eimzo:eimzo-sdk:1.2.8'
```

### Flutter — `eimzo_flutter`

Add to your `pubspec.yaml`:

```yaml
dependencies:
  eimzo_flutter: ^1.0.0
```

### macOS — `eimzo-mac`

1. Download the latest **E-IMZO** DMG from the [releases page](https://github.com/peachdev-uz/eimzo-mac/releases/latest).
2. Double-click the DMG.
3. Drag **E-IMZO** into the **Applications** folder.
4. Open from Launchpad or Spotlight.

The DMG is signed & notarized (~5.5 MB, no installer), under the Apple Developer team **Scientific Information Center Of New Technologies**.

> **macOS troubleshooting:** if macOS blocks the app (App Sandbox Provenance on macOS 15+), run:
> ```bash
> xattr -cr /Applications/E-IMZO.app
> ```

---

## Requirements

### iOS — `eimzo-ios-sdk`
- iOS 16+
- Swift 5.9+
- SwiftUI
- Camera permission for QR scanning
- NFC entitlements for ID card support
- Bundle ID registration required (via info@peachdev.uz)

### macOS — `eimzo-mac`
- macOS 13 (Ventura) or later
- Universal binary — runs natively on Apple Silicon (M1/M2/M3/M4) and Intel Macs

### Android — `eimzo-mobile-sdk`
- Android API 24+ (minSdk 24)
- compileSdk 34
- Kotlin
- Permissions: `INTERNET`, `NFC`, `CAMERA`

### Flutter — `eimzo_flutter`
- Flutter 3.10+
- Android: minSdk 24, compileSdk 34, Java 17, Kotlin JVM target 17, core library desugaring enabled (omitting it causes `NoClassDefFoundError: java/time/...`)
- iOS: 16.0+ minimum deployment target, with camera + NFC `Info.plist` keys
- Bundles native E-IMZO Mobile SDK 1.2.8

---

## Highlights

- **iOS** — Single SwiftUI `EImzoView` component presented as a sheet, NFC ID card support, QR scanning, PFX key import, USB token support, deep linking for inter-app signing requests, expired-certificate blocking, single-tap key selection, and a test mode.
- **macOS** — Native SwiftUI app with dark mode, PFX/.p12 drag-and-drop import, QR key import (hex paste from the Android E-IMZO app), Feitian USB token & CCID smart-card support (no vendor drivers, via Apple CryptoTokenKit), deep links (`eimzo://sign?qc=…`), full App Sandbox with Keychain-encrypted storage.
- **Android** — Complete pre-built UI (Home, Key management, Sign flow, NFC, QR scanner), key import via PFX/QR/NFC ID-card, USB token (FT-1280) support, deep-link signing, certificate validation, R8 obfuscation with tamper detection.
- **Flutter** — Plugin wrapping the native E-IMZO Mobile SDK (1.2.8 bundled); native code handles signing/key-management UI while Flutter handles init and deep-link routing. Core API: `init({EimzoConfig config})` returns a `bool` license check, `openSignUi({String? deepLink})` launches the native signing UI. Includes USB token signing (bundled FEITIAN libraries, auto-detection), NFC, and QR scanning.

**Recent highlights:** iOS **v1.1.6** added expired-certificate blocking and single-tap key selection; USB token support arrived in iOS **v1.1.1**; eimzo-mobile-sdk **v1.2.8** fixed USB token signing.

---

## Licensing

The SDKs are **proprietary / license-gated**. Unregistered apps hit the SDK's built-in blocked screen.

- **iOS (`eimzo-ios-sdk`)** — closed-source XCFramework; **Bundle ID registration required** via **info@peachdev.uz**.
- **Android & mobile (`eimzo-mobile-sdk`)** — proprietary, **Firebase-gated license verification** per app package name. Copyright (c) 2026 Yangi Texnologiyalar (YT). Registration via **info@yt.uz**.
- **Flutter (`eimzo_flutter`)** — license-gated: the app must be registered (package name + bundle id) and **NFC entitlement approved** via **info@yt.uz**.

---

## Documentation & Links

**iOS — `eimzo-ios-sdk`**
- [Integration guide](https://github.com/peachdev-uz/eimzo-ios-sdk/blob/main/docs/INTEGRATION.md)
- [Manual installation](https://github.com/peachdev-uz/eimzo-ios-sdk/blob/main/docs/MANUAL_INSTALLATION.md)
- [Changelog](https://github.com/peachdev-uz/eimzo-ios-sdk/blob/main/CHANGELOG.md)
- [Latest release](https://github.com/peachdev-uz/eimzo-ios-sdk/releases/latest)

**macOS — `eimzo-mac`**
- [Privacy policy](https://github.com/peachdev-uz/eimzo-mac/blob/main/PRIVACY.md)
- [Latest release](https://github.com/peachdev-uz/eimzo-mac/releases/latest)
- [Issues](https://github.com/peachdev-uz/eimzo-mac/issues)

**Android — `eimzo-mobile-sdk`**
- [Repository & README](https://github.com/peachdev-uz/eimzo-mobile-sdk)
- [Latest release](https://github.com/peachdev-uz/eimzo-mobile-sdk/releases/latest)
- [eimzo_flutter on pub.dev](https://pub.dev/packages/eimzo_flutter)

**Flutter — `eimzo_flutter`**
- [Repository & README](https://github.com/peachdev-uz/eimzo_flutter)
- [Underlying native SDK (eimzo-mobile-sdk)](https://github.com/peachdev-uz/eimzo-mobile-sdk)
- [Latest release](https://github.com/peachdev-uz/eimzo_flutter/releases/latest)

**General**
- Official E-IMZO site: [e-imzo.uz](https://e-imzo.uz)

---

## Security & Compliance

- Native implementation of **OzDST 1092-2009** and **OzDST 1106-2009** digital-signature standards (plus **GOST 28147** on iOS).
- macOS app distributed as a **signed & notarized DMG**, notarized under the Apple Developer team **Scientific Information Center Of New Technologies**.
- macOS storage uses the **full App Sandbox** with **Keychain-encrypted** key storage.
- Android builds use **R8 obfuscation with tamper detection**.
- All SDKs are **license-gated** (Firebase-gated for the mobile SDK), with bundle-ID / package-name registration required.

---

## Support & Contact

- **Bugs:** open an issue on the relevant repository (e.g. [eimzo-mac issues](https://github.com/peachdev-uz/eimzo-mac/issues)).
- **Licensing / registration:**
  - iOS SDK — **info@peachdev.uz**
  - macOS / Android / Flutter — **info@yt.uz**
- **Telegram:** [@peachdevuz](https://t.me/peachdevuz)
- **GitHub:** [github.com/peachdev-uz](https://github.com/peachdev-uz)

---

<div align="center">

<sub>© 2026 peachdev-uz · E-IMZO integration SDKs · O'zbekiston uchun ERI yechimlari</sub>

</div>
