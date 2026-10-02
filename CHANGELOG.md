# 📋 DroidDesk Changelog & Release Notes

All notable changes to the DroidDesk application are documented in this file.

---

## [1.0.1] - Android Emulator & SDK Toolchain Manager (Windows 64-bit)

### 🚀 Highlights & New Features
- **Integrated Device & Emulator Manager**: Full virtual device management alongside physical phones in one unified dashboard.
- **Android Virtual Device (AVD) Creation Wizard**: Multi-step wizard to configure, create, and initialize Android emulators directly inside DroidDesk without opening Android Studio.
- **Android SDK Environment & Toolchain Diagnostics**: Auto-detection, manual configuration, and real-time health checks for Android SDK Root, ADB, Emulator, and AVD Manager.
- **Installed System Image Scanner**: Automatically detects and catalogs installed Android system images across API levels (e.g., Android API 37, Android 15 Vanilla Ice Cream API 35, Android 10 API 29).
- **One-Click Emulator Lifecycle Controls**: Boot, restart, gracefully stop, or delete virtual devices with live boot progress tracking.
- **Unified Testing & Screen Mirroring**: Full support for 1-click APK installation, low-latency screen mirroring, screenshot captures, and real-time logcat streaming directly on virtual emulators.
- **Enhanced Status Bar**: Real-time health indicators expanded to track `emulator`, `avdmanager`, and `sdkmanager` status alongside existing core tools.
- **Updated Production Installer**: Self-contained setup package `DroidDesk-Setup-v1.0.1.exe` (~218 MB).

---

## [1.0.0] - Initial Release (Windows 64-bit)

### 🚀 Highlights
- **First Official Production Release** of DroidDesk desktop companion for Windows 64-bit.
- Full self-contained installer (`DroidDesk-Setup-v1.0.0.exe`) bundling essential tools (`scrcpy` and `gitleaks`).
- Complete local-first, zero-telemetry architecture for maximum privacy.

### 🔍 APK Inspection & Security
- **Deep Manifest Inspection**: Automated extraction of package metadata, version names, SDK targets, activities, services, receivers, and content providers.
- **Permissions Audit**: Categorization of declared permissions with risk assessment for dangerous capabilities.
- **Signature & Certificate Verification**: Support for APK Signature Schemes v1, v2, v3, and v4 with fingerprint extraction (MD5, SHA-1, SHA-256).
- **Embedded Secret Scanner**: Integrated `gitleaks` engine to detect exposed API keys, secret tokens, and credentials in APK files and source trees offline.

### 📱 Device Control & Screen Features
- **Real-Time Device Discovery**: ADB connection manager with device model, architecture, battery status, and developer option indicators.
- **Ultra-Low Latency Screen Mirroring**: Integrated `scrcpy` engine embedded directly in the application.
- **Headless Video Recording**: Record test and reproduction sessions directly from device streams to `.mp4`.
- **Recordings Gallery**: Visual video recordings manager with automatic thumbnail generation and local video player launch.
- **High-Resolution Screenshots**: One-click screen capture with organized storage.

### ⚡ Developer Tools
- **Zero-Freeze Logcat Viewer**: Real-time log streaming with instant text search, regular expression filters, and severity level filtering.
- **Automated Smoke Testing**: Automated cycle of installing APK, launching main activity, monitoring for crashes/ANRs, taking verification screenshots, and clean uninstallation.
- **Environment Switcher**: Easy switching between Dev, Staging, and Production environments with safety build guards.

---
