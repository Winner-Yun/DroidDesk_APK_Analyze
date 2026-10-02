# 📱 DroidDesk - Local Android Development & APK Analysis Companion

[![Release](https://img.shields.io/badge/Release-v1.0.1-blue.svg)](installer/DroidDesk-Setup-v1.0.1.exe)
[![Platform](https://img.shields.io/badge/Platform-Windows%2064--bit-0078D6.svg)](installer/DroidDesk-Setup-v1.0.1.exe)
[![Architecture](https://img.shields.io/badge/Architecture-x64-green.svg)](installer/DroidDesk-Setup-v1.0.1.exe)
[![Android SDK](https://img.shields.io/badge/Android%20SDK-Emulator%20%26%20AVD-brightgreen.svg)](installer/DroidDesk-Setup-v1.0.1.exe)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](LICENSE.txt)

> **DroidDesk** is an all-in-one local desktop companion for Android developers, QA testers, and security researchers. Manage physical Android phones and Android SDK virtual emulators (AVDs) in one place, create custom virtual devices with an intuitive 4-step wizard, inspect APKs, audit permissions and signatures, mirror and record device screens at 60 FPS, scan for leaked credentials offline, and monitor real-time Logcat streams without cloud dependencies.

---

## 📥 Downloads (Latest Release v1.0.1)

| File | Version | Architecture | Size | SHA256 Checksum | Direct Download Link |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **DroidDesk-Setup-v1.0.1.exe** | **1.0.1 (Latest)** | Windows x64 | ~218 MB | `17089bd0daddae2707d2c0cd...` | [⬇️ Download v1.0.1 Setup](installer/DroidDesk-Setup-v1.0.1.exe) |
| **DroidDesk-Setup-v1.0.0.exe** | 1.0.0 | Windows x64 | ~217 MB | `fee2f11b174fb6557a9da15a...` | [⬇️ Download v1.0.0 Setup](installer/DroidDesk-Setup-v1.0.0.exe) |

*Full checksums for all installer packages are available in [installer/SHA256SUMS.txt](installer/SHA256SUMS.txt).*

---

## ⚡ Quick Start: Easy 3-Step Setup

### Step 1: Install DroidDesk
1. Download **[DroidDesk-Setup-v1.0.1.exe](installer/DroidDesk-Setup-v1.0.1.exe)**.
2. Double-click the file to open the setup wizard.
3. Follow the on-screen prompts to complete installation and create a desktop icon.
4. Launch **DroidDesk** from your Desktop or Start Menu.

*(Note: If Windows SmartScreen displays a warning, click **More info** and then **Run anyway**).*

---

### Step 2: Connect a Device (Physical Phone or Virtual Emulator)

#### Option A: Physical Android Phone (USB or Wi-Fi)
1. On your Android phone, go to **Settings** > **About Phone**.
2. Tap **Build Number** **7 times** until you see *You are now a developer!*.
3. Go back to **Settings** > **Developer Options** (or *System > Developer options*).
4. Turn on **USB Debugging**.
5. Connect your phone to your PC via a USB cable.
6. When prompted on your phone screen with *Allow USB debugging?*, check **Always allow from this computer** and tap **Allow**.
7. *(Optional)* Switch to Wi-Fi mode in the **Devices** page by typing your phone's IP address (e.g. `192.168.1.24:5555`) and clicking **Connect over Wi-Fi**.

#### Option B: Android Virtual Device / Emulator (v1.0.1 New!)
1. Navigate to **Devices** in the left sidebar.
2. DroidDesk automatically links to your local Android SDK (click the **Android SDK Ready** button to view SDK root, toolchain status, and installed system images).
3. Click **+ Create Emulator** to launch the 4-step wizard (Device Profile ➔ Android Version ➔ Configuration ➔ Create).
4. Under **Virtual Devices (Emulators)**, click **Start / Boot** on your configured emulator (e.g., Pixel 8). The emulator will boot up right beside DroidDesk!

---

### Step 3: Start Analyzing & Testing!
- **Drop an APK**: Drag and drop any `.apk` file directly into DroidDesk to inspect its package details, activities, permissions, certificates, and secrets.
- **Screen Mirror & Record**: Go to **Device Control** or **Screen Mirror** to interact with your physical phone or virtual emulator in real-time and record test sessions.
- **Logcat**: Monitor live system and app logs with color-coded severity levels and instant regex search.
- **Automated Smoke Test**: Push the active APK to your target hardware or virtual emulator for autonomous install, launch, crash observation, and screenshot validation.

---

## 📸 Visual Tour & Demo Walkthrough (From Home to Settings)

Explore DroidDesk's complete interface step-by-step. Each page below follows the exact sidebar menu flow from **Home** down to **Settings**, complete with interface breakdowns, live feature tours, and actionable demo instructions.

| # | Page Name | Menu Category | Key Highlights Visible in Screenshot |
| :-: | :--- | :--- | :--- |
| **01** | [🏠 Home Dashboard](#1--home-overview--quick-launcher) | `OVERVIEW` | Active project summary, quick-launch actions, 1-click APK installer, device history |
| **02** | [📱 Device & Emulator Manager](#2--device--emulator-manager-physical-phones--virtual-avds) | `CONNECT` | Dual physical & virtual device roster, Android SDK diagnostics, 4-step AVD wizard, emulator lifecycle |
| **03** | [🖥️ Screen Mirror](#3-️-live-screen-mirroring--remote-control) | `CONNECT` | 60 FPS low-latency scrcpy mirror, touch gestures, keyboard forwarding, stream presets |
| **04** | [⚡ Logcat Viewer](#4--real-time-logcat-stream--query-engine) | `CONNECT` | Columnar log parser, multi-level severity filters (V/D/I/W/E/F), regex search, export |
| **05** | [📸 Screenshots Gallery](#5--screenshot-gallery--inspector) | `CONNECT` | On-demand screen capture, resolution metadata, one-click copy to clipboard, explorer sync |
| **06** | [🎥 Screen Recordings](#6--video-recordings-manager--player) | `CONNECT` | Video capture archive, integrated MP4 player, metadata inspector, folder launcher |
| **07** | [🔍 APK Analyzer](#7--deep-apk-analyzer--permissions-audit) | `INSPECT` | SDK targets, component counts, high-risk permission breakdown, signature verification |
| **08** | [🧪 Test Runner](#8--automated-smoke-testing-pipeline) | `INSPECT` | Millisecond-timed automated install-launch-observe-capture-clean cycle, pass verdict |
| **09** | [🛡️ Secret Scanner](#9-️-offline-secret--credential-leak-scanner) | `PROTECT` | Built-in Gitleaks engine, leaked token detection, syntax-highlighted code context, remediation |
| **10** | [🗂️ File Organizer](#10-️-smart-file-organizer--batch-renamer) | `PROTECT` | Suggested standardized names, 3-tier xxhash64 deduplication, transactional undo journal |
| **11** | [🚀 Build Commands](#11--commands-selection--security-audit-hub) | `SHIP` | 50 built-in commands, simulated APK string extraction & hot data leak test, live console |
| **12** | [⚙️ Settings & About](#12-️-settings-inspection-history--credits) | `SETTINGS` | APK inspection history, developer attribution, team recognition, native tool locator |

---

### 1. 🏠 Home Overview & Quick Launcher
> **Sidebar Route:** `OVERVIEW > Home`

![01 Home Overview](docs/screenshots/01_home.png)

#### 🔍 What You See on Screen
- **Active Project Banner:** Highlights the active APK (`2753915a059f_Taskify.apk`) and package name (`com.example.to_do_list_app`) along with quick metadata tags: `v0.1.0 (1)`, `min 24 (Android 7.0)`, `target 36 (Android 16)`, and file size (`57.2 MB`).
- **Quick-Action Shortcuts:** One-click shortcuts to jump directly to **Inspect in analyzer**, **Run tests**, or **Scan secrets**.
- **1-Click APK Installer:** Choose the active APK or browse external files, select your target hardware (`CPH2159`) or virtual emulator, and click **Install to device** without touching the command line.
- **Emulator & Device History Table:** Displays live connection status (green `ONLINE`), device model, Android platform (`Android 13 / API 33`), and timestamp of last connection.
- **Native Tool Status Strip (Bottom Bar):** Real-time health indicators verifying that `adb`, `emulator`, `avdmanager`, `sdkmanager`, `aapt2`, `apksigner`, `apkanalyzer`, `bundletool`, `gitleaks`, `scrcpy`, and `git` are ready.

#### Demo User Instructions
1. Drag and drop any `.apk` file anywhere into DroidDesk or click **Upload APK** in the top bar.
2. Verify that the project card updates with package identifier, SDK levels, and file size.
3. Select your target device from the dropdown and click **Install to device**.
4. Use the quick action buttons to instantly transition into static analysis, testing, or credential audits.

---

### 2. 📱 Device & Emulator Manager (Physical Phones & Virtual AVDs)
> **Sidebar Route:** `CONNECT > Devices`

![02 Devices & Emulator Running](docs/screenshots/02_devices.png)

#### 🔍 What You See on Screen
DroidDesk v1.0.1 elevates device management into a unified command center managing both physical Android phones and Android SDK virtual emulators side-by-side:

- **Dual Device Roster:**
  - **Physical Devices Section:** Displays connected physical phones (e.g. `CPH2159 (e36401e6)`), Android OS version (`Android 13 · API 33`), architecture (`arm64-v8a`), and live battery indicator (`Battery: 100%`).
  - **Virtual Devices (Emulators) Section:** Catalogs all configured Android Virtual Devices (e.g., `Pixel 8 (emulator-5554)`), system image edition (`Google Play · google_apis_playstore/x86_64`), and real-time state badge (`Ready`, `Booting`, or `Offline`).
- **Quick Action Bar:** Direct 1-click shortcuts for both physical and virtual devices:
  - `Screen`: Launches ultra-low latency screen mirroring.
  - `APK`: Installs the active APK directly to the selected phone or emulator.
  - `Logs`: Opens the real-time Logcat stream filtered to the device.
  - `Restart`: Reboots the virtual emulator.
  - `Stop`: Gracefully stops the running emulator process.
  - `Delete`: Removes the AVD configuration from disk.
- **Top Utility Header:**
  - `Android SDK Ready` indicator: One-click access to the Android Environment & Toolchain Diagnostics modal.
  - `+ Create Emulator` button: Launches the 4-step virtual device creation wizard.
  - Wireless Wi-Fi input (`192.168.1.24:5555`) with instant **Connect Wi-Fi** and **Refresh** buttons.
- **Device Details Inspector (Right Panel):** Comprehensive device metrics including Model, Manufacturer, Android version, API Level, CPU ABI (`google_apis_playstore/x86_64` or `arm64-v8a`), Pixel Density (`420 dpi`), and Connection type.
- **Floating Native Emulator Window:** High-performance native Android emulator window running simultaneously with live Android home screen, apps, and hardware navigation keys.

---

#### 🛠️ Deep Dive: Android SDK Diagnostics & AVD Creation Wizard

DroidDesk v1.0.1 includes two purpose-built diagnostic and creation tools integrated into the Devices page:

| Android Toolchain Diagnostics | 4-Step AVD Creation Wizard |
| :---: | :---: |
| ![02 SDK Diagnostics](docs/screenshots/02_sdk_diagnostics.png) | ![02 Create Emulator Wizard](docs/screenshots/02_create_emulator_wizard.png) |
| *Auto-detects Android SDK Root (`C:\Android\sdk`), validates ADB, Emulator, AVD Manager, and inventories installed system images (API 37, 35, 29).* | *Select hardware profiles (Pixel, Phone, Tablet, Automotive) with live search, configure Android versions, adjust RAM/storage, and create AVDs.* |

- **Android Environment & Toolchain Diagnostics:**
  - **Android SDK Root Directory:** Configurable root path (e.g., `C:\Android\sdk`) with `Browse...` and `Save Revalidate` buttons.
  - **Toolchain Components Status:** Real-time health validation for:
    - *Android SDK*: Verified install path.
    - *ADB (Platform-Tools)*: Version detection (e.g. `35.0.2`).
    - *Android Emulator*: Version detection (e.g. `35.3.11`).
    - *AVD Manager*: Command-line binary verification (`cmdline-tools/latest/bin/avdmanager.bat`).
  - **Installed System Images Table:** Catalogs available OS versions, API Levels, Editions/Tags (`Google Play`, `Google APIs`), and ABIs (`x86_64`, `arm64-v8a`).
- **4-Step Virtual Device Creation Wizard:**
  - **Step 1: Choose Device Profile:** Searchable hardware definitions catalog covering Pixel phones, general smartphones, tablets, and automotive displays with exact screen dimensions and resolutions.
  - **Step 2: Android Version:** Choose your target system image and API level.
  - **Step 3: Configuration:** Set RAM allocation, heap size, internal storage, and device orientation.
  - **Step 4: Create:** Instant creation and initialization without opening heavy IDEs.

#### Demo User Instructions
1. **Connect a Physical Phone:** Plug in your phone via USB with USB Debugging enabled. The green `READY` badge and hardware properties populate automatically.
2. **Launch an Emulator:** Click **Start / Boot** on any configured virtual device (e.g., Pixel 8). Watch the status badge transition from `Offline` ➔ `Booting` ➔ `Ready`.
3. **Inspect SDK Health:** Click the green **Android SDK Ready** button in the header to review your installed SDK tools, ADB version, and available Android system images.
4. **Create a New Virtual Device:** Click **+ Create Emulator**, search for your favorite hardware profile (e.g., `Pixel 8`), select your Android version, and complete the wizard.
5. **Mirror or Install with 1 Click:** Click **Screen** to mirror the emulator or physical device screen, or click **APK** to deploy your test build instantly!

---

### 3. 🖥️ Live Screen Mirroring & Remote Control
> **Sidebar Route:** `CONNECT > Screen mirror`

![03 Screen Mirror](docs/screenshots/03_screen_mirror.png)

#### 🔍 What You See on Screen
- **Embedded Scrcpy Mirror:** 60 FPS hardware-accelerated interactive view of your Android phone screen. Full support for mouse clicks, swipes, taps, and keyboard text entry.
- **Device Navigation Virtual Toolbar:** Dedicated hardware buttons on the right: `Back`, `Home`, `Recents`, `Power / Lock`, `Rotate`, `Vol -`, `Vol +`, and `Capture`.
- **Window Shortcuts & Gestures Guide:** Handy reference for desktop productivity:
  - `Resize Window`: Freely drag window borders.
  - `Alt + F`: Toggle true Fullscreen mode.
  - `Alt + G`: Scale view to 1:1 pixel-accurate ratio.
  - `Alt + W`: Eliminate black letterboxing bars.
  - `Drag & Drop APK`: Drag any APK directly onto the mirrored screen to trigger an immediate install.
- **Stream Presets & Display Tuning:**
  - Max Size: `1080p (Recommended)`
  - Framerate: `60 FPS (Fluid)`
  - Bitrate: `8 Mbps (Balanced)`
  - Convenience toggles: `Keep mirror window on top`, `Keep device awake`, `Turn device screen off` (saves phone battery while testing), `Show touch indicators`, and `Forward device audio`.
- **Live Session Status:** Real-time stream indicator and duration counter (`Streaming (Live) · 00:31`).

#### Demo User Instructions
1. Navigate to **Screen mirror** and click **Bring Window to Front** if minimized.
2. Click and swipe across the mirrored phone display using your mouse just like physical touchscreen gestures.
3. Type using your physical PC keyboard into text fields on your phone.
4. Try dragging an APK file from Windows Explorer directly onto the phone screen to test instant drag-and-drop installation.

---

### 4. ⚡ Real-Time Logcat Stream & Query Engine
> **Sidebar Route:** `CONNECT > Logcat`

![04 Logcat Viewer](docs/screenshots/04_logcat.png)

#### 🔍 What You See on Screen
- **Parsed Log Columns:** High-throughput streaming table with clean columns: `Time`, `PID` (Process ID), `TID` (Thread ID), `Level`, `Tag`, and `Message`.
- **Severity Level Filter:** Instant filter buttons for log severities: `V` (Verbose), `D` (Debug), `I` (Info), `W` (Warning), `E` (Error), and `F` (Fatal).
- **Multi-Field Search Bar:** Targeted query boxes for filtering by specific **Tag**, **PID**, and real-time **Regular Expression (Regex)** over the message body.
- **Stream Buffer Controls:**
  - `Pause`: Freezes screen inspection without dropping incoming log events in the background.
  - `Clear`: Flushes current table display.
  - `Export view`: Exports current filtered log records to file for bug attachments.
  - `Stop stream` / `Start stream`: Halts or resumes logcat listener.
- **Buffer Counter:** Tracks total parsed records (e.g., `16,262 lines`).

#### Demo User Instructions
1. Click **Logcat** in the sidebar. Streaming begins automatically for the active physical device or virtual emulator.
2. In the **Tag** box, enter `ActivityManager` or your application's tag to isolate relevant entries.
3. Switch severity level to `W` (Warn) or `E` (Error) to immediately spot exceptions, crashes, or deadlocks.
4. Click **Pause** to inspect a stack trace in peace, then click **Export view** to save the log excerpt.

---

### 5. 📸 Screenshot Gallery & Inspector
> **Sidebar Route:** `CONNECT > Screenshots`

![05 Screenshots Gallery](docs/screenshots/05_screenshots.png)

#### 🔍 What You See on Screen
- **Saved Screenshots Archive:** Chronological list of captures with timestamp, file name, and file size metadata (e.g., `Sep 29, 15:22 · 2.47 MB`) with dynamic search filter.
- **High-Definition Preview Pane:** High-res preview showing exact image pixel dimensions (`1080 x 2400 px`), file size, and creation date.
- **Export & Clipboard Actions:**
  - `Copy Image`: Instantly copies the full image bitmap to your Windows clipboard - ready to paste (`Ctrl + V`) into Slack, Figma, GitHub, or Jira.
  - `Copy Path`: Copies the exact absolute file path (`C:\Users\...\Pictures\DroidDesk\...`).
  - `Open in Window`: Launches in default desktop photo viewer.
  - `Show in Folder`: Opens the destination folder in Windows File Explorer.
  - `Delete`: Removes unwanted test captures.
- **Header Actions:** One-click `Take Screenshot` button, `Open Folder`, and `Refresh`.

#### Demo User Instructions
1. Click the blue **Take Screenshot** button in the top right.
2. Notice the new capture appears immediately in the list with a crisp thumbnail preview.
3. Click **Copy Image** and press `Ctrl + V` into your chat or documentation to share proof of test results instantly.

---

### 6. 🎥 Video Recordings Manager & Player
> **Sidebar Route:** `CONNECT > Recordings`

![06 Recordings Manager](docs/screenshots/06_recordings.png)

#### 🔍 What You See on Screen
- **Saved Recordings Library:** List of `.mp4` video recordings captured during device test runs (`recording_e36401e6_*.mp4`), complete with date and size (`4.98 MB`).
- **Integrated Video Player Preview:** Video thumbnail with playback overlay, encoding format (`MP4 Video (H.264)`), and recording timestamp.
- **Playback & Management Controls:**
  - `Play Video`: Opens the video in DroidDesk's media player.
  - `Open in Window`: Launches playback in your system media player (e.g. VLC or Windows Media Player).
  - `Show in Folder`: Reveals the `.mp4` file in File Explorer.
  - `Copy Path`: Copies the video path to clipboard.
  - `Delete`: Deletes the file from disk.
- **Header Tools:** `Open Folder` button to browse all captured video files directly on disk.

#### Demo User Instructions
1. Start a recording session anytime from the **Screen Mirror** page using the **Record Screen** button.
2. Perform your app test flow, then stop recording.
3. Head over to **Recordings** in the sidebar.
4. Click the recording from the list and hit **Play Video** to review the captured QA test run.

---

### 7. 🔍 Deep APK Analyzer & Permissions Audit
> **Sidebar Route:** `INSPECT > APK analyzer`

![07 APK Analyzer](docs/screenshots/07_apk_analyzer.png)

#### 🔍 What You See on Screen
- **Comprehensive APK Metadata:** Displays filename (`2753915a059f_Taskify.apk`), Package (`com.example.to_do_list_app`), Version Code & Name (`0.1.0 (1)`), `min 24 (Android 7.0)`, `target 36 (Android 16)`, file size (`57.2 MB`), and build flavor (`Release build`).
- **Audit Tabs:**
  - `Signature`: Audit APK Signature Scheme (v1, v2, v3, v4) and cryptographic hashes (MD5, SHA-1, SHA-256).
  - `Permissions`: Inspect all declared manifest permissions with risk-level categorization.
  - `Components`: Audit declared Activities, Services, Broadcast Receivers, and Content Providers.
- **Permission Risk Metric Cards:**
  - Total Permissions: `12`
  - High-Risk / Sensitive: `3` (Flagged in red alerts)
  - Normal Permissions: `9`
- **Security Assessment Flags:** Highlights sensitive permissions (e.g. `HIGH RISK: Read Shared Storage - android.permission.READ_EXTERNAL_STORAGE`) with human-readable explanations of privacy and security risks.
- **Filters & One-Click Copy:** Fast filtering by risk group (`All (12)`, `High-Risk (3)`, `Normal (9)`) with dedicated `Copy` buttons for each permission string.

#### Demo User Instructions
1. Load any target `.apk` file into DroidDesk.
2. Click **APK analyzer** and select the **Permissions** tab.
3. Click the **High-Risk (3)** filter button to immediately review potentially dangerous permissions (e.g. storage access, exact alarms, boot startup).
4. Switch to the **Signature** tab to verify that the APK is properly signed with modern v2/v3 signing schemes before release.

---

### 8. 🧪 Automated Smoke Testing Pipeline
> **Sidebar Route:** `INSPECT > Test runner`

![08 Test Runner](docs/screenshots/08_test_runner.png)

#### 🔍 What You See on Screen
- **Artifact Under Test:** Target APK, package name, version, and target SDK ready for validation.
- **Granular Millisecond-Accurate Execution Sequence:** Complete automated smoke test pipeline compatible with both physical phones and virtual emulators:
  - ⏱️ **Validate** (`454 ms`): In-process manifest and integrity verification using androguard.
  - ⏱️ **Install** (`8,757 ms`): Pushes APK to target phone or emulator (`adb -s $S install -r -t app.apk`).
  - ⏱️ **Launch** (`1,898 ms`): Spawns main launcher activity via monkey runner (`PID: 30090`).
  - ⏱️ **Observe** (`21,888 ms`): Monitors live logcat for crashes, fatal signals, and warnings (111 lines analyzed, 5 warnings tracked).
  - ⏱️ **Screenshot** (`569 ms`): Takes automatic post-launch screencap to confirm UI rendered properly.
  - ⏱️ **Permissions** (`215 ms`): Verifies runtime permissions granted (9 of 12 granted).
  - ⏱️ **Static hosts** (`1 ms`): Extracts declared network endpoints and hostnames.
  - ⏱️ **Clean up** (`566 ms`): Silently uninstalls test package from phone or emulator (`adb -s $S uninstall $PKG`).
- **Test Verdict & Summary Panel:**
  - High-visibility verdict banner: `PASS WITH WARNINGS` (Completed all steps in `34,351 ms`).
  - Thumbnail preview of the captured launch screen.
  - Inline log snippet highlighting captured warnings.
  - `Open report` link for full audit export.

#### Demo User Instructions
1. Select your target device (physical phone or virtual emulator) and test profile (`Default`).
2. Click the blue **Run test** button.
3. Watch the automated agent execute the entire install, launch, observation, screenshot capture, and cleanup sequence autonomously.
4. Review the final verdict badge and view the auto-captured screenshot of the launched app.

---

### 9. 🛡️ Offline Secret & Credential Leak Scanner
> **Sidebar Route:** `PROTECT > Secret scanner`

![09 Secret Scanner](docs/screenshots/09_secret_scanner.png)

#### 🔍 What You See on Screen
- **Vulnerability Metric Badges:** Immediate severity summary: `0 Critical`, `0 High`, `2 Needs review`, `0 Informational`.
- **Detected Secrets Table:** Detailed findings showing Severity (`REVIEW`), Key Name (`FIREBASE_API_KEY`), Environment (`Android Resource`), File (`strings.xml`), Line number (`63`), and matched Token.
- **Deep Context & Remediation Inspector (Right Panel):**
  - **Location & Environment:** File path breadcrumb with `Copy path`.
  - **Full Token Value:** Complete exposed token string with `Copy token` button.
  - **Syntax-Highlighted Code Snippet:** Context viewer centering on Line 63 of `strings.xml`.
  - **Actionable Remediation Guidance:** Specific, practical security instructions: *"Restrict this Firebase API key in Google Cloud Console by Android application package name and SHA-1 certificate fingerprint, and limit to enabled APIs."*
  - `Show in File Explorer` button.

#### Demo User Instructions
1. Navigate to **Secret scanner** and click **Scan APK** (or select a local source folder).
2. Scan runs locally and 100% offline via the pre-bundled Gitleaks engine - zero cloud telemetry or data sharing.
3. Click any row in the findings table to inspect the exact line of code where the credential was found.
4. Follow the **Recommended Action** advice to lock down API keys before shipping to the Play Store.

---

### 10. 🗂️ Smart File Organizer & Batch Renamer
> **Sidebar Route:** `PROTECT > File organizer`

![10 File Organizer](docs/screenshots/10_file_organizer.png)

#### 🔍 What You See on Screen
- **Target Folder Selection:** Path selector with `Browse...`, `View folder`, `Smart Clean (Remove copies & junk)`, and `Suggest renames`.
- **Subfolder Categorization Toggle:** Option to auto-organize files into category folders (`APKs/`, `Images/`, `Documents/`, etc.).
- **Interactive Suggested Renames Table:** Side-by-side preview showing `Original File` alongside `Suggested Rename (Editable)` (transforms messy lowercase filenames with underscores into clean, professional title case), `What Changed` description, and individual `Accept` buttons or batch `Accept all (8)`.
- **Three-Tier Deduplication Engine:** Examines file size, 8 KB edge hash, and full xxhash64 to detect duplicate copies with zero false positives. Displays examined files count, duplicate sets, redundant copies, and recoverable disk space (`141 B`).
- **Crash-Resilient Undo Journal:** Logs each batch with unique transaction ID (`batch c384a647...`) and offers a 1-click **Undo last batch** button that restores original file names even if interrupted or closed.

#### Demo User Instructions
1. Click **Browse...** and select any messy folder with APK builds, test screenshots, or documents.
2. Click **Suggest renames** to see clean, standardized name suggestions.
3. Double-click any name in the table to make custom edits if desired.
4. Click **Accept all** to rename all files in one batch.
5. If you change your mind, click **Undo last batch** to instantly roll back every change!

---

### 11. 🚀 Commands Selection & Security Audit Hub
> **Sidebar Route:** `SHIP > Build commands`

![11 Commands & Security Audit](docs/screenshots/11_build_commands.png)

#### 🔍 What You See on Screen
- **Built-in Command Catalog:** Access to **50 built-in commands** covering builds, testing, security audits, ADB operations, and APK analysis.
- **Instant Search & Filter:** Filter bar with typeahead search (e.g., `audit`, `debug`, `adb`, `test`, `secret`).
- **Active Command Configuration:** Shows selected command `[Audit] APK API Keys & Secrets` (`audit:apk-keys`) with detailed description: *"Extracts resources.arsc strings and assets to detect extractable API keys."*
- **Execution Bar:** `Run Security Audit`, `Stop`, and `Clear` console.
- **Live Output Console:** Formatted security penetration test terminal output:
  - Simulating APK string extraction (`resources.arsc`).
  - Total files/resources inspected (`21`).
  - Exposed credentials detected (`0`).
  - Security verdict: `VERDICT: [SAFE & PROTECTED] No exposed credentials detected!`.

#### Demo User Instructions
1. Navigate to **Build commands** in the left sidebar.
2. In the Search box, type `audit` and select `[Audit] APK API Keys & Secrets`.
3. Click **Run Security Audit** to test whether third parties can reverse-engineer secrets out of your compiled binary.
4. Review the simulated extraction output directly inside the embedded console.

---

### 12. ⚙️ Settings, Inspection History & Credits
> **Sidebar Route:** `SETTINGS > Settings`

![12 Settings](docs/screenshots/12_settings.png)

#### 🔍 What You See on Screen
- **APK Inspection History:** Persistent local log tracking all analyzed APK files (`com.example.to_do_list_app`, `2753915a059f_Taskify.apk`, `0.1.0 (1)`, `API 36`, `57.2 MB`, timestamp) with `Remove`, `Clear All APKs`, and `Refresh` buttons.
- **About DroidDesk Card:**
  - **Developer:** Winner Yun
  - **Team:** Khansha Team
  - **Date Created:** 30/9/2026
  - **Repository:** [https://github.com/Winner-Yun](https://github.com/Winner-Yun)
- **Special Contributor Recognition:** Highlights contributor **Leave Sovatnak** (*He also work on the device functional*).
- **Global Native Tool Indicators (Footer):** Persistent status strip verifying `adb`, `emulator`, `avdmanager`, `sdkmanager`, `aapt2`, `apksigner`, `apkanalyzer`, `bundletool`, `gitleaks`, `scrcpy`, and `git`.

#### Demo User Instructions
1. Click **Settings** in the lower-left corner of the sidebar.
2. Review your historical APK audit logs or click **Clear All APKs** to reset cache.
3. Access developer links and project repository details.

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🤖 **Android Emulator & AVD Manager** *(v1.0.1 New)* | Full virtual device lifecycle: create AVDs with a 4-step wizard, auto-detect SDK tools & system images, boot, restart, stop, and mirror emulators. |
| 📱 **Dual Physical & Virtual Device Control** | Connect physical Android phones over USB / Wi-Fi ADB alongside Android emulators with instant device switching. |
| 🔍 **Deep APK Inspector** | Inspect manifest details, target/min SDKs, component counts (Activities, Services, Receivers), and dangerous permission alerts. |
| 🔏 **Certificate & Signature Audit** | Verify APK Signature Schemes (v1, v2, v3, v4) and display MD5, SHA-1, and SHA-256 signing fingerprints. |
| 🖥️ **Live Screen Mirroring** | Low-latency Android device screen mirroring powered by pre-bundled scrcpy for both physical phones and emulators. |
| 🎥 **Video Recording & Gallery** | Record device screen video clips during testing and browse recordings with generated thumbnails. |
| 🛡️ **Offline Secret Scanner** | Pre-bundled gitleaks engine to detect exposed API keys, private tokens, and credentials in APK files and source code. |
| ⚡ **Real-Time Logcat Viewer** | High-performance log streaming with quick filtering by level (Verbose, Debug, Info, Warn, Error, Fatal) and regex search. |
| 🧪 **Automated Smoke Testing** | Automatic install, launch, screenshot capture, crash detection, and uninstall cycle on real or virtual devices. |
| 🔒 **100% Offline & Private** | Zero telemetry, zero tracking, no login required. Your code and APKs never leave your workstation. |

---

## 🛠️ System Requirements

- **Operating System:** Windows 10 or Windows 11 (64-bit / x64).
- **RAM:** Minimum 4 GB (8 GB or 16 GB recommended for running Android emulators).
- **Disk Space:** ~500 MB for DroidDesk (+ additional space for Android SDK system images if using emulators).
- **Android SDK & Emulation:**
  - Auto-detected if Android SDK or Android Studio is installed (`C:\Android\sdk` or `C:\Users\<User>\AppData\Local\Android\Sdk`).
  - Configurable directly from the **Android SDK Ready** diagnostics modal in the Devices header.
  - Hardware virtualization (WHPX / Hyper-V or Intel HAXM) enabled in BIOS/UEFI for emulator acceleration.
- **Pre-bundled Tools:** Both `scrcpy` and `gitleaks` are packaged with the installer - **no manual tool installation required!**

---

## ❓ Troubleshooting & FAQ

<details>
<summary><b>1. Windows SmartScreen says "Windows protected your PC"</b></summary>
Because this is a freshly published installer without an enterprise EV certificate, Windows may show a SmartScreen warning.  
Simply click <b>More info</b> and then click <b>Run anyway</b> to proceed with the setup.
</details>

<details>
<summary><b>2. DroidDesk says "No Device Connected" or "Device Unauthorized"</b></summary>
1. Unplug and replug your USB cable.  
2. Make sure USB Debugging is turned on in your phone's Developer Options.  
3. Unlock your phone and look for the popup prompt: <i>Allow USB debugging from this computer?</i>. Check <i>Always allow</i> and press <b>Allow</b>.  
4. In DroidDesk, click the <b>Refresh</b> button in the top navigation bar.
</details>

<details>
<summary><b>3. How do I configure my Android SDK or fix "Android SDK / Emulator Not Found"?</b></summary>
1. Click the <b>Android SDK Ready</b> button at the top of the <b>Devices</b> page (or go to <b>Settings > Tool Locator</b>).  
2. In the <b>Android SDK Root Directory</b> field, click <b>Browse...</b> and select your SDK root (e.g., <code>C:\Android\sdk</code> or <code>C:\Users\&lt;YourUser&gt;\AppData\Local\Android\Sdk</code>).  
3. Click <b>Save Revalidate</b>. DroidDesk will verify ADB, Emulator, AVD Manager, and list all installed system images.
</details>

<details>
<summary><b>4. How do I create and run a new Android Virtual Device (Emulator)?</b></summary>
1. On the <b>Devices</b> page, click the blue <b>+ Create Emulator</b> button.  
2. Follow the 4-step wizard: select your device hardware profile (e.g. Pixel 8), choose your installed Android system image (e.g. API 35), customize specs, and click <b>Create</b>.  
3. Under <b>Virtual Devices (Emulators)</b>, click <b>Start / Boot</b>. The emulator will boot and become ready for 1-click APK installation, screen mirroring, and log streaming!
</details>

<details>
<summary><b>5. Tool Locator shows red status icons</b></summary>
Go to <b>Settings</b> > <b>Tool Locator</b> inside DroidDesk:
- If ADB or Emulator is not found automatically, enter your Android SDK path.
- Scrcpy and Gitleaks are pre-bundled in the application folder and will display green indicators automatically.
</details>

---

## 📄 License & Documentation

- [Step-by-Step Setup Guide](SETUP_GUIDE.md)
- [Release Notes & Changelog](CHANGELOG.md)
- [Checksum Verification (SHA256)](installer/SHA256SUMS.txt)
- [License](LICENSE.txt)

---
*Created with ❤️ for Android Developers and Security Testers.*
