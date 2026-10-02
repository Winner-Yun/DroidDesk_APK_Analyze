# 📖 DroidDesk User Setup & Getting Started Guide

This guide provides simple, step-by-step instructions to install and start using **DroidDesk** on your Windows computer.

---

## 📋 Table of Contents
1. [Installation](#1-installation)
2. [Setting Up Your Android Phone (Physical Device)](#2-setting-up-your-android-phone-physical-device)
3. [Connecting Your Phone to DroidDesk](#3-connecting-your-phone-to-droiddesk)
4. [Managing Virtual Devices & Android Emulators (v1.0.1)](#4-managing-virtual-devices--android-emulators-v101)
   - [Configuring the Android SDK Path](#configuring-the-android-sdk-path)
   - [Creating a Virtual Device (AVD)](#creating-a-virtual-device-avd)
   - [Booting, Restarting & Stopping Emulators](#booting-restarting--stopping-emulators)
5. [Using Key Features](#5-using-key-features)
   - [APK Analysis](#apk-analysis)
   - [Screen Mirroring & Control](#screen-mirroring--control)
   - [Screen Video Recording](#screen-video-recording)
   - [Logcat Log Viewer](#logcat-log-viewer)
   - [Secret & Credential Scanner](#secret--credential-scanner)
6. [Troubleshooting](#6-troubleshooting)

---

## 1. Installation

1. Navigate to the `installer` folder or download [**DroidDesk-Setup-v1.0.1.exe**](installer/DroidDesk-Setup-v1.0.1.exe).
2. Double-click the installer:
   - If Windows shows a blue prompt (**Windows protected your PC**), click **More info** and select **Run anyway**.
3. Choose your installation folder (default: `C:\Program Files\DroidDesk`).
4. Keep the checkbox **"Create a desktop shortcut"** enabled for easy access.
5. Click **Install**, and once completed, click **Finish** to open DroidDesk.

---

## 2. Setting Up Your Android Phone (Physical Device)

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
5. *(Optional)* Connect wirelessly: enter your phone's Wi-Fi IP and port (e.g. `192.168.1.24:5555`) in the Devices page and click **Connect Wi-Fi**.

---

## 4. Managing Virtual Devices & Android Emulators (v1.0.1)

DroidDesk v1.0.1 introduces a complete **Device & Emulator Manager** allowing you to build, run, and test on Android Virtual Devices (AVD) directly alongside your physical phones.

### Configuring the Android SDK Path
1. In the sidebar, navigate to **Devices** (`CONNECT > Devices`).
2. Click the **Android SDK Ready** button in the top bar to open **Android Environment & Toolchain Diagnostics**.
3. If not automatically detected, set your **Android SDK Root Directory** (typically `C:\Android\sdk` or `C:\Users\<YourUsername>\AppData\Local\Android\Sdk`) and click **Save Revalidate**.
4. Verify the status of:
   - **Android SDK**
   - **ADB (Platform-Tools)**
   - **Android Emulator**
   - **AVD Manager**
   - **Installed System Images** (e.g. Android 15 Vanilla Ice Cream API 35, Android API 37)

### Creating a Virtual Device (AVD)
1. Click the blue **+ Create Emulator** button.
2. In the 4-step wizard:
   - **Step 1: Device Profile**: Choose from Pixel, Phone, Tablet, or Automotive hardware profiles with defined screen size and resolution. Use the search bar to filter quickly.
   - **Step 2: Android Version**: Select your target system image and API level (e.g. Android 15, API 35).
   - **Step 3: Configuration**: Review or adjust RAM, storage, and device skin orientation.
   - **Step 4: Create**: Click Create to build your new AVD.

### Booting, Restarting & Stopping Emulators
1. Your virtual devices appear under **Virtual Devices (Emulators)** in the Devices roster.
2. Click **Start / Boot** on the desired emulator. The status indicator will transition from `Offline` ➔ `Booting` ➔ `Ready`.
3. The native floating Android emulator window will boot into the Android OS.
4. Use the quick action buttons:
   - **Screen**: Launch screen mirror.
   - **APK**: Install the active APK directly to the emulator.
   - **Logs**: Open live Logcat streaming for the emulator.
   - **Restart**: Reboot the virtual device.
   - **Stop**: Gracefully terminate the emulator session.
   - **Delete**: Remove the AVD from disk when no longer needed.

---

## 5. Using Key Features

> **Visual Tour Available:** See [README.md - Visual Tour & Demo Walkthrough](README.md#-visual-tour--demo-walkthrough-from-home-to-settings) for full screenshot breakdowns and guides for all 12 interface pages from Home to Settings.

### APK Analysis
- Drag any `.apk` file from File Explorer and drop it onto the DroidDesk window.
- Alternatively, click the **Upload APK** button in the top bar.
- View immediate details:
  - Package ID and Version Name / Code
  - Minimum and Target Android SDK versions
  - Declared Permissions (highlighting high-risk dangerous permissions)
  - Activity components and export status
  - Signature scheme verification (v1 / v2 / v3 / v4) and cryptographic hashes

### Screen Mirroring & Control
- Click **Screen Mirror** in the left sidebar.
- Click **Start Mirror** to display your physical device or virtual emulator screen inside DroidDesk with ultra-low latency.
- Control your device using your computer mouse and keyboard.

### Screen Video Recording
- On the Screen Mirror page or Device Control, click the **Record Video** button to start recording your screen during tests.
- When finished, click **Stop Recording**.
- Switch to the **Recordings** page to browse, view thumbnails, and double-click to play your captured video sessions.

### Logcat Log Viewer
- Click **Logcat** in the left sidebar.
- Click **Start Stream** to view live logs streaming from your physical phone or emulator.
- Filter by log level: **Verbose**, **Debug**, **Info**, **Warn**, **Error**, or **Assert**.
- Use the search bar to search tags, package names, or regex patterns.

### Secret & Credential Scanner
- Click **Secret Scanner** to scan an APK or project folder for accidentally committed API keys, tokens, or private credentials.
- Powered by the built-in, pre-packaged Gitleaks engine - runs completely offline with zero data leakage.

---

## 6. Troubleshooting

| Issue | Cause | Solution |
| :--- | :--- | :--- |
| **Physical device not listed** | Cable or driver issue | Ensure USB cable supports data transfer (not charging-only). Check that USB Debugging is ON. |
| **Device says "Unauthorized"** | ADB permission unconfirmed | Unlock your phone and look for the "Allow USB debugging" prompt. Tap "Allow". |
| **Android SDK / Emulator not detected** | Custom SDK install path | Click **Android SDK Ready** button in the top header or **Settings > Tool Locator**, browse to your SDK directory (e.g. `C:\Android\sdk`), and click **Save Revalidate**. |
| **AVD Manager missing** | Command-line tools not installed | In Android Studio SDK Manager, install the "Android SDK Command-line Tools (latest)". |
| **Mirroring fails to start** | Device screen locked or ADB busy | Unlock your phone screen and click "Restart ADB Server" in DroidDesk. |

---
*For additional support or bug reports, please consult the project repository.*
