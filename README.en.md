# TwoTile

[日本語](README.md)

**A Windows system tray utility that arranges your windows for you, so you don't have to decide where each one goes.**

Every time a new window opens, you decide where it goes. You nudge it aside, fix the overlap, and lose your train of thought. You do this dozens of times a day. TwoTile was made to take that decision off your hands. It runs in the system tray, and whenever you open or close a window, it moves each window to the cell nearest to where you left it. **There's nothing to set up or learn.**

The author originally wrote it for personal use and **has used it every day, at work and at home, for more than 20 years.** Not having to rearrange windows was such a relief that the author rebuilt it so that others can use it too.

## Two windows in view is usually enough

Most of the time, only the top two windows really need to be visible: **one you refer to, and one you work in.** TwoTile was built on that idea, and that's where its name comes from. It lines up those two windows side by side, filling the screen.

When you work from instructions, you can switch to 3x1 or 2x2. You can give a fixed width to windows that don't work without one, and leave out windows you don't want touched. **The exceptions are there when you need them, so most of the time you don't have to think about it.**

## What it does

- **Auto arrange**: Lines up your open windows in a grid that fits your screen. The number of divisions is chosen automatically from the screen size.
- **Respects where you put things**: Each window goes to the cell closest to where it is now. TwoTile doesn't push windows into a corner on its own.
- **Stays out of your way**: When it rearranges windows, it doesn't come to the front, take the focus, or make sounds.
- **Exclusions and fixed widths**: You can choose windows not to arrange, or windows to place at a fixed width.
- **Pause**: Stop it anytime from the system tray.

For details, select **Help** in the app's system tray menu. Help also has the full Terms of Use and Third-Party Notices.

TwoTile is shown in English when the Windows display language isn't Japanese.

## What it doesn't do

For your windows to just stay arranged, TwoTile has to stay out of your way.

- **It doesn't come to the front,** so it never covers the window you're working in.
- **It doesn't take the focus,** so it never interrupts your typing.
- **It doesn't make sounds or show notifications** when it rearranges windows.
- **It doesn't connect to the internet** or collect your information. Your settings are saved only in a file on your PC.

> **TwoTile is currently a free public beta.** If you notice anything, let us know through the support contact on the official website. Known limitations are listed in [Known Issues](known_issues.en.md). This repository is where the **portable version** of TwoTile is distributed. You can get the Microsoft Store version at <https://apps.microsoft.com/detail/9NFM07C9TNPS>. The official website is <https://poola-vii.github.io/twotile/index.en.html>.
>
> This repository is for distributing the portable version, and **it doesn't contain the source code of TwoTile** (the source code isn't public).

## Requirements

| | |
|---|---|
| OS | Windows 11 (64-bit) |
| CPU | x64. ARM and 32-bit aren't supported |
| .NET | **Not needed.** Everything required is included |
| Help | WebView2 Runtime, which comes with Windows 11 |
| Display | Designed for 1920x1080 or larger. Only windows on the main display are arranged |

## Get TwoTile

### Microsoft Store version (recommended)

<https://apps.microsoft.com/detail/9NFM07C9TNPS>

Install it from the Microsoft Store. The Store lets you know about updates. **On PCs where Smart App Control is on, use the Store version.**

### Portable version (this repository)

**For PCs that can't use the Microsoft Store.** No installation is needed. Put `TwoTile.exe` anywhere you like and run it.

- Download: [Releases](https://github.com/poola-vii/TwoTile-releases/releases) in this repository
- Update notices: the Releases Atom feed (`https://github.com/poola-vii/TwoTile-releases/releases.atom`), watching this repository, or the [Changelog](CHANGELOG.en.md). **The app doesn't communicate over the internet, so it doesn't tell you about updates.**
- When you tell others about TwoTile, give them this page or the official website instead of the file (the rules for passing it on are in §4 of the [Terms of Use](terms.en.md)).

**The portable version isn't signed.** Because of that:

- **The first time you run it, you see a "Windows protected your PC" warning.** Select **More info**, and then **Run anyway**.
- It can't run on PCs where Smart App Control is on. Use the Store version.

### Check the file you downloaded

After you download it, check that it's the same as the one from the download source. Run the following in PowerShell, and check that the value shown matches the one published in the Release.

```pwsh
Get-FileHash .\TwoTile.exe -Algorithm SHA256
```

| Version | File | SHA-256 |
|:---|:---|:---|
| 1.0.9 | `TwoTile.exe` | `3D04577B7AE37C7B7399EDC9DA6E9DF6197966B9DDC8FDBE12E13A755614C680` |
| 1.0.6 | `TwoTile.exe` | `E7C1C65086C6B2AE1A3F1197C35ED00535A2614AE64AF0EF628A9AE8E83B63B9` |
| 1.0.4 | `TwoTile.exe` | `1B061625589ED62FCBF638554DD6FAF7B2C8EC95C4281E9DC638F576A42EDEE1` |
| 1.0.3 | `TwoTile.exe` | `247A165D48689C2EF3E07046E7CDA4233CACCB10DEAE841A34200A4BA7B227CF` |
| 1.0.2 | `TwoTile.exe` | `53CA0DF4CDF9EDCAE19F4E5CE5098CA2677FE7E80749F5873B881E9D9347ED8F` |
| 1.0.1 | `TwoTile.exe` | `44C461CD82A0A6989F2702DD915119C3A23EF5EBC775EBC3AF13838228CD4F1D` |

If the value is different, don't use the file.

### Go back to an earlier version

If something goes wrong with a new version, you can go back to an earlier one.

1. Select **Exit** in the system tray menu to close TwoTile.
2. Download the `TwoTile.exe` of the version you want from the download source (<https://github.com/poola-vii/TwoTile-releases/releases>), and check that it's genuine with "Check the file you downloaded" above.
3. Replace the `TwoTile.exe` you're using with the downloaded file, and run it. The version number you went back to appears at the top of the system tray menu.

Your settings (`config.json`) are kept. However, settings added in the newer version aren't used by the earlier version, and they're removed when the earlier version saves settings (other settings stay). If you replaced the file in the same place, **Start with Windows** keeps working.

You can't go back to an earlier version of the Store version yourself. If you have a problem, let us know through the [support contact](https://poola-vii.github.io/twotile/support.en.html). If you went back to an earlier version, please tell us what happened.

## Getting started

1. Run `TwoTile.exe` (start the Store version from the Start menu).
2. A two-color icon appears in the system tray. Any open windows are arranged within a few seconds.
3. Right-click the icon to open the menu.
4. To pause, clear the check mark next to **Auto arrange**. To quit, select **Exit**.

**TwoTile doesn't start automatically at first.** To start it when you sign in to Windows, use **Start with Windows** on the **General** tab of **Settings...** in the menu. (For the Store version, select **Open Windows Settings...** in the same place, and turn it on in Startup in Windows Settings.)

Settings are saved in `%APPDATA%\TwoTile\config.json`. They stay after you remove the app, so delete them yourself if you don't need them.

## If you have trouble

- [Known Issues](known_issues.en.md): known limitations, and the environments it has been tested in
- [Support](https://poola-vii.github.io/twotile/support.en.html): how to report a problem. You can contact us at <https://github.com/poola-vii/support> (recommended), or by email if you don't have a GitHub account
- [How to Collect Logs](https://poola-vii.github.io/twotile/log_collection.en.html): how to get the information to include with your report

## More

- [Changelog](CHANGELOG.en.md)
- [Terms of Use](terms.en.md)
- [Privacy Policy](https://poola-vii.github.io/twotile/privacy_policy.en.html): **This app doesn't communicate over the internet.**
- [Third-Party Notices](third_party_notices.en.md)
- Official website: <https://poola-vii.github.io/twotile/index.en.html>

---

© 2026 poola-vii
