<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ff9966,100:ff5e62&height=200&section=header&text=peachdev-uz&fontColor=ffffff&fontSize=70&fontAlignY=35&desc=E-IMZO%20SDKs%20%26%20tools%20for%20every%20platform&descAlignY=58&descSize=18" alt="peachdev-uz" width="100%" />

**E-IMZO integration SDKs for iOS, macOS, Android, and Flutter**

*O'zbekiston ERI (elektron raqamli imzo) tizimini har qanday platformaga integratsiya qilish uchun SDK'lar*

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-peachdev--uz-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/peachdev-uz)
[![Telegram](https://img.shields.io/badge/Telegram-peachdevuz-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/peachdevuz)

</div>

---

## About

**peachdev-uz** builds developer SDKs and tools for **E-IMZO** — Uzbekistan's national e-signature (ERI / elektron raqamli imzo) system. Our mission is to make E-IMZO signing easy to integrate everywhere developers work: native **iOS** and **macOS**, native **Android**, and **Flutter**. Each SDK ships pre-built signing UI and supports the OzDST cryptographic standards (with GOST 28147 also supported on iOS), with key import via PFX files, QR codes, NFC ID cards, and USB tokens — so you can add compliant digital signing to your app without building the crypto stack yourself.

---

## Platforms supported

<div align="center">

![iOS](https://img.shields.io/badge/iOS-16%2B-000000?style=for-the-badge&logo=apple&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-5.9%2B-F05138?style=for-the-badge&logo=swift&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-13%2B-000000?style=for-the-badge&logo=apple&logoColor=white)
![Android](https://img.shields.io/badge/Android-API%2024%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-3.10%2B-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

</div>

---

## Products / SDKs

| SDK | Platforms | Description |
| --- | --- | --- |
| [**eimzo-ios-sdk**](https://github.com/peachdev-uz/eimzo-ios-sdk) | iOS 16+ · SwiftUI | E-IMZO mobile signing SDK for iOS, distributed as a closed-source XCFramework with a unified SwiftUI signing view (`EImzoView`). |
| [**eimzo-mac**](https://github.com/peachdev-uz/eimzo-mac) | macOS 13+ | Native macOS desktop app for E-IMZO — sign documents with PFX keys, QR keys, and Feitian / CCID USB tokens. |
| [**eimzo-mobile-sdk**](https://github.com/peachdev-uz/eimzo-mobile-sdk) | Android (API 24+) · Flutter (3.10+) | E-IMZO Mobile SDK with pre-built complete UI for the O'zbekiston ERI system — native Android and Flutter. |
| [**eimzo_flutter**](https://github.com/peachdev-uz/eimzo_flutter) | Android (minSdk 24) · iOS 16+ | Thin Flutter plugin that bootstraps the official E-IMZO Mobile SDK and handles `eimzo://sign?...` deep links. |

---

## Highlights

- **Pre-built signing UI** — drop-in screens for the home view, key list, sign flow, NFC animations, and QR scanner (no need to build your own).
- **Native cryptography** — OzDST 1092 (electronic signature) and OzDST 1106 (hash function), plus GOST 28147 on iOS.
- **Flexible key import** — PFX / `.p12` files, QR-code key import, NFC ID card reading, and USB token support (Feitian / CCID, FT-1280).
- **Deep linking** — handle `eimzo://sign?qc=...` links to jump straight into the signing flow.
- **Test mode** — target the E-IMZO test endpoint during development.

---

## Getting Started

Each SDK has its own README with full setup instructions, requirements, and a documented API. Start there:

- **iOS** — [eimzo-ios-sdk](https://github.com/peachdev-uz/eimzo-ios-sdk) · install via Swift Package Manager or manually embed `EimzoSDK.xcframework`. See [`docs/INTEGRATION.md`](https://github.com/peachdev-uz/eimzo-ios-sdk/blob/main/docs/INTEGRATION.md) and [`docs/MANUAL_INSTALLATION.md`](https://github.com/peachdev-uz/eimzo-ios-sdk/blob/main/docs/MANUAL_INSTALLATION.md).
- **macOS** — [eimzo-mac](https://github.com/peachdev-uz/eimzo-mac) · download the signed & notarized DMG from the [latest release](https://github.com/peachdev-uz/eimzo-mac/releases/latest).
- **Android & Flutter** — [eimzo-mobile-sdk](https://github.com/peachdev-uz/eimzo-mobile-sdk) · add the GitHub-hosted Maven repository and the `uz.eimzo:eimzo-sdk` dependency (Android), or the `eimzo_flutter` package (Flutter).
- **Flutter plugin** — [eimzo_flutter](https://github.com/peachdev-uz/eimzo_flutter) · add it as a Flutter dependency per the repo's README.

> **Licensing note:** the SDKs are license-gated. App bundle IDs (iOS) and package names (Android) must be registered with the vendor before use — unregistered apps will see the SDK's built-in blocked screen. See each repo's README for the exact terms and contact details.

---

## Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-peachdev--uz-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/peachdev-uz)
[![Telegram](https://img.shields.io/badge/Telegram-peachdevuz-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/peachdevuz)

For integration questions, licensing, and registering your app, contact the vendor by email (**info@peachdev.uz** / **info@yt.uz**, per each repo's README), reach out on [Telegram](https://t.me/peachdevuz), or open an issue on the relevant repository.

</div>

<div align="center">

<sub>Built with 🍑 by peachdev-uz · O'zbekiston uchun E-IMZO yechimlari</sub>

</div>
