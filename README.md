# Tactyl — releases

**Tactyl** is a 4" touch screen for your desk that becomes a live dashboard
and control deck for your computer: system stats, shortcuts, your open apps,
browser tabs and bookmarks, calendar, notifications, media, a trackpad, a
keyboard, home automation and more, all laid out by you in a visual editor.

More at **[tactyl.site](https://tactyl.site)**.

This public repository holds the **app installers** and the **add-on
catalogue**. The source code is private.

## Download

Get the latest version from
**[Releases](https://github.com/tactylsite/tactyl-releases/releases/latest)**:
`Tactyl-<version>.dmg`.

| Platform | Status |
|---|---|
| macOS 11 or later (Intel and Apple silicon) | Available |
| Windows 10 or later | In development |

## Install (macOS)

1. Open the `.dmg` and drag **Tactyl** to the Applications folder.
2. The first time, macOS says it cannot check who made the app (it is not
   signed with an Apple developer account). To open it:
   - Right-click (or Ctrl-click) **Tactyl** › **Open** › **Open**.
   - If that does not work: **System Settings › Privacy & Security**, and at
     the bottom, next to **Tactyl**, click **Open Anyway**.

   You only need to do this once.
3. Connect the board with the USB cable. The app lives in the menu bar (the
   board icon, top right): a green dot means the board is connected.

### Permissions

macOS asks for them the first time they are needed:

- **Accessibility**: so the board's keyboard, trackpad and key buttons can
  type and move the pointer.
- **Automation**: so the app can read browser tabs and open apps.
- **Calendars**: to show your upcoming events on the board.

## Updates

The app checks this repository and tells you, in the menu bar and in the
editor, when a new version is out. Download it and drag the app to
Applications again. If it brings new firmware, the editor offers to flash it
to the board (**Settings › Firmware**), by cable or over Wi-Fi.

## Signatures

Every installer has a `.sig` file next to it, and every add-on a `.zip.sig`.
They are **Ed25519** signatures made with keys that never leave the
publisher's computer. The app refuses updates, firmware and add-ons whose
signature does not match its built-in public key.

## Add-ons

`addons/` is the catalogue the app reads:

| File | Content |
|---|---|
| `addons/index.json` | The list of add-ons: id, name, version, descriptions in 7 languages. |
| `addons/<id>-<version>.zip` | The add-on package (actions, screens, icons, texts). |
| `addons/<id>-<version>.zip.sig` | Its signature. |

Add-ons are installed and activated from the app (**Settings › Add-ons**). They
only contain safe actions (key combinations and https links), never commands.

## Licence

The installers are free to download. Using Tactyl is subject to its licence
(see [tactyl.site](https://tactyl.site)). © 2026 Tactyl. All rights reserved.
