<p align="center">
  <img src="https://i.postimg.cc/mD5X9kkL/banner.png" alt="PinTop Window Utility — Pin Any Window Always-on-Top & Control Opacity on Windows" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Window%20Pin%20%26%20Opacity-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-pintop--v1.2-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# PinTop Window Utility — Pin Any Window Always-on-Top & Control Opacity on Windows

**Playing on a single monitor and want a YouTube guide, Discord chat, calculator, or notes window pinned visibly above your work? Press Ctrl+Space to pin any active window Always-on-Top and scroll to adjust its transparency.**

PinTop Window Utility adds missing window-management controls to Windows 10 and 11 in a tiny 10 MB tray app: **toggling `WS_EX_TOPMOST` on any window via hotkey, adjusting window alpha transparency (`20%–100%`), and enabling click-through mode for overlay references**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) single-monitor gamers, developers, and office users** who want instant window pinning without installing heavy 300 MB utility suites.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Reference browser or calculator hides behind active full-window apps | Windows lacks a built-in hotkey to pin arbitrary windows on top | Press `Ctrl+Space` on any active window to lock it Always-on-Top |
| Pinned window blocks content underneath it | Standard windows are 100% opaque even when pinned | Use `Ctrl+Shift+MouseWheel` to set 40%–80% transparency |
| Accidentally clicking a pinned overlay video while working | Pinned windows still intercept mouse clicks | Toggle Click-Through (`WS_EX_TRANSPARENT`) from the tray menu |
| Heavy multi-module utility suites consume 250+ MB RAM | Installing massive shell suites just for one window hotkey | Run a single lightweight ~10 MB portable tray executable |

## Download for Windows

[**Download PinTop.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/PinTop.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `PinTop.exe`? (Key features)

- Pins or unpins any active window Always-on-Top with a customizable global hotkey (`Ctrl+Space` default).
- Adjusts window transparency (`20%` to `100%`) smoothly using `Ctrl+Shift+ScrollWheel`.
- Supports Click-Through mode so mouse clicks pass right through semi-transparent reference windows.
- Automatically unpins all windows cleanly when exiting the tray app.

### Sample Output

```text
[PinTop] Tray Utility Active (Pin Hotkey: Ctrl+Space | Opacity: Ctrl+Shift+Wheel)
[OK]   Pinned Window    : "Boss_Map_Guide - Google Chrome" [Topmost: ON | Opacity: 85%]
[INFO] Active Pinned    : 1 window currently pinned above standard windows
```

The release ZIP is named `PinTop.zip`; the Windows executable inside is named `PinTop.exe`.

1. Close PinTop before updating or replacing executable files.
2. Click **Download PinTop.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `PinTop.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `PinTop.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Single-monitor multitasking without constant Alt-Tabbing

Keep guides, build planners, timers, or chat windows visible while working in another app.

### Translucent overlays for tracing, notes, and dashboards

Adjusting window opacity lets you read both the pinned window and the workspace behind it.

### Zero shell hooks or registry clutter

Uses standard Win32 `SetWindowPos` and `SetLayeredWindowAttributes` APIs.

### Instant unpin safety

Pressing the hotkey again or closing PinTop restores normal window Z-order immediately.

## Default folders and configuration paths

PinTop runs from any folder and saves hotkey preferences in `%APPDATA%\PinTop`:

```text
%APPDATA%\PinTop\settings.json
```

Typical directory layout:

```text
System Tray -> PinTop
├── Toggle Topmost Hotkey : Ctrl + Space
├── Adjust Opacity        : Ctrl + Shift + MouseWheel
└── Unpin All Windows     : Tray Menu / Exit
```

Exclusive fullscreen games take direct display ownership; use Borderless Windowed mode if pinning a guide window over a game.

## Quick start guide

Follow these steps to get started:

1. **Extract `PinTop.zip` to a local folder and launch `PinTop.exe`.** Look for the pin icon in your Windows system tray.
2. **Click the window you want to keep visible and press `Ctrl+Space`.** A brief toast confirms the window is pinned Always-on-Top.
3. **Hold `Ctrl+Shift` and scroll the mouse wheel to adjust opacity.** Scroll back up to restore 100% opacity.
4. **Press `Ctrl+Space` again to unpin the window.** Returns the window to normal desktop behavior.

### Data safety note

PinTop modifies only runtime window flags and never alters files on disk.

## What the status summary shows

PinTop displays **currently pinned window titles, opacity percentages, and active global hotkeys**.

## FAQ

**Does PinTop work over games?**

Yes, when the game is running in Borderless Windowed or Windowed mode (exclusive fullscreen bypasses standard desktop windows).

**What happens to pinned windows if I close PinTop?**

PinTop automatically unpins all windows back to normal Z-order when exiting.

**Can I change the default Ctrl+Space hotkey?**

Yes—right-click the PinTop tray icon and select Hotkey Settings.

## Useful reading

- [Microsoft Docs — SetWindowPos (HWND_TOPMOST)](https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-setwindowpos)

## More Windows Desktop Utilities

- [ClipVault-OfflineClipboardHistory](../ClipVault-OfflineClipboardHistory) — Offline Windows clipboard history & plain-text snippet manager
- [SnipText-ScreenOCRClipboard](../SnipText-ScreenOCRClipboard) — Instant hotkey screen region OCR text extractor to clipboard
- [AudioSwitch-HotkeyToggle](../AudioSwitch-HotkeyToggle) — One-key headphones, speakers & microphone switcher
- [Win11-GamingDebloatGuard](../Win11-GamingDebloatGuard) — Windows 11 gaming optimizer & background process cleaner

*Independent open-source desktop utility for Windows.*
