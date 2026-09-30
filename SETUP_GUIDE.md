# 📖 DroidDesk User Setup & Getting Started Guide

This guide provides simple, step-by-step instructions to install and start using **DroidDesk** on your Windows computer.

---

## 📋 Table of Contents
1. [Installation](#1-installation)
2. [Setting Up Your Android Phone](#2-setting-up-your-android-phone)
3. [Connecting Your Phone to DroidDesk](#3-connecting-your-phone-to-droiddesk)
4. [Using Key Features](#4-using-key-features)
   - [APK Analysis](#apk-analysis)
   - [Screen Mirroring & Control](#screen-mirroring--control)
   - [Screen Video Recording](#screen-video-recording)
   - [Logcat Log Viewer](#logcat-log-viewer)
   - [Secret & Credential Scanner](#secret--credential-scanner)
5. [Troubleshooting](#5-troubleshooting)

---

## 1. Installation

1. Navigate to the `installer` folder or download [**DroidDesk-Setup-v1.0.0.exe**](installer/DroidDesk-Setup-v1.0.0.exe).
2. Double-click the installer:
   - If Windows shows a blue prompt (**Windows protected your PC**), click **More info** and select **Run anyway**.
3. Choose your installation folder (default: `C:\Program Files\DroidDesk`).
4. Keep the checkbox **"Create a desktop shortcut"** enabled for easy access.
5. Click **Install**, and once completed, click **Finish** to open DroidDesk.

---

## 2. Setting Up Your Android Phone

To allow DroidDesk to communicate with your device, you need to enable **USB Debugging**:

### How to Enable Developer Options:
1. Open your device **Settings**.
2. Scroll to the bottom and select **About phone** (or **About device**).
3. Find **Build number**:
   - On Xiaomi / Redmi: Tap **MIUI Version** or **HyperOS Version** 7 times.
   - On Samsung / Pixel / Motorola: Tap **Build number** 7 times.
4. You will see a toast notification: *"You are now a developer!"*.

### How to Turn On USB Debugging:
1. Return to the main **Settings** menu.
2. Select **System** > **Developer options** (or **Additional settings** > **Developer options**).
3. Toggle the **USB debugging** switch to **ON**.
4. *(Optional for Xiaomi devices)*: Also enable **USB debugging (Security settings)** and **Install via USB** if you wish to run automated tests.

---

## 3. Connecting Your Phone to DroidDesk

1. Connect your Android phone to your PC using a reliable USB data cable.
2. Unlock your phone. A popup dialog will appear on your phone screen:
   > **"Allow USB debugging?"**
3. Check the box **"Always allow from this computer"** and tap **Allow**.
4. In DroidDesk, your device will appear in the top device selector bar with its model name and battery level.

---

## 4. Using Key Features

> **Visual Tour Available:** See [README.md — Visual Tour & Demo Walkthrough](README.md#-visual-tour--demo-walkthrough-from-home-to-settings) for full screenshot breakdowns and guides for all 12 interface pages from Home to Settings.

### APK Analysis
- Drag any `.apk` file from File Explorer and drop it onto the DroidDesk window.
- Alternatively, click the **Browse APK** button on the home screen.
- View immediate details:
  - Package ID and Version Name / Code
  - Minimum and Target Android SDK versions
  - Declared Permissions (highlighting high-risk dangerous permissions)
  - Activity components and export status
  - Signature scheme verification (v1 / v2 / v3 / v4) and cryptographic hashes

### Screen Mirroring & Control
- Click **Screen Mirror** in the left sidebar.
- Click **Start Mirror** to display your physical device screen inside DroidDesk with ultra-low latency.
- Control your phone using your computer mouse and keyboard.

### Screen Video Recording
- On the Screen Mirror page or Device Control, click the **Record Video** button to start recording your phone screen during tests.
- When finished, click **Stop Recording**.
- Switch to the **Recordings** page to browse, view thumbnails, and double-click to play your captured video sessions.

### Logcat Log Viewer
- Click **Logcat** in the left sidebar.
- Click **Start Stream** to view live logs streaming from your phone.
- Filter by log level: **Verbose**, **Debug**, **Info**, **Warn**, **Error**, or **Assert**.
- Use the search bar to search tags, package names, or regex patterns.

### Secret & Credential Scanner
- Click **Secret Scanner** to scan an APK or project folder for accidentally committed API keys, tokens, or private credentials.
- Powered by the built-in, pre-packaged Gitleaks engine — runs completely offline with zero data leakage.

---

## 5. Troubleshooting

| Issue | Cause | Solution |
| :--- | :--- | :--- |
| **Device not listed** | Cable or driver issue | Ensure USB cable supports data transfer (not charging-only). Check that USB Debugging is ON. |
| **Device says "Unauthorized"** | ADB permission unconfirmed | Unlock your phone and look for the "Allow USB debugging" prompt. Tap "Allow". |
| **ADB not found** | Android SDK missing | Install Android Studio or download Android Platform Tools. Configure the path in **Settings > Tool Locator**. |
| **Mirroring fails to start** | Device screen locked or ADB busy | Unlock your phone screen and click "Restart ADB Server" in DroidDesk. |

---
*For additional support or bug reports, please consult the project repository.*
