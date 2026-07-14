# Lunevo — Releases

Public releases for **Lunevo**, the whole-boat synchronized audio system:

- **Server SD image** — flash this onto a Raspberry Pi to create a Lunevo device
- **Android app** — sideload builds of the Lunevo client

More at [getlunevo.com](https://getlunevo.com)

---

## Flashing the Lunevo Server image

You'll need a Raspberry Pi (3, 4, or 5), a microSD card (8 GB or larger), and
[Raspberry Pi Imager](https://www.raspberrypi.com/software/) (free, Windows/macOS/Linux).

### Option A — Add Lunevo to Raspberry Pi Imager (recommended)

Do this once and Imager will always offer the latest Lunevo release:

1. Open Raspberry Pi Imager (version 2.0 or newer)
2. Click **App Options** in the bottom-right corner
3. Next to **Content Repository**, click **EDIT**
4. Select **Use Custom URL** and paste:

   ```
   https://getlunevo.com/os_list.json
   ```

5. Click **Apply & Restart**
6. **Choose OS** → select **Lunevo Server**, pick your SD card, and write

> To go back to the standard OS list later, open App Options again and reset
> the Content Repository.

### Option B — Manual download

1. Download `lunevo-server.img.xz` from the
   [server-latest release](../../releases/tag/server-latest)
   (don't extract it — Imager reads `.img.xz` directly)
2. In Raspberry Pi Imager: **Choose OS** → **Use custom** → select the file
3. Pick your SD card and click **Next**
4. When asked **"Would you like to apply OS customisation settings?" choose NO** —
   the Lunevo image configures itself during setup

### After flashing

Insert the card, power the Pi, and wait about a minute. The device appears as
**Lunevo-Setup** in the Lunevo app's setup wizard (Bluetooth) — no keyboard,
monitor, or network configuration needed.

Devices flashed from this image receive future software updates automatically
through the Lunevo app, even without onboard internet.

---

## Android app (sideload)

1. Download `lunevo-<version>.apk` from the [Releases](../../releases) page
   onto your Android device
2. Open it and allow installation from unknown sources when prompted
3. Requires Android 8.0 (API 26) or newer

> These are test builds signed with a development key. When Lunevo arrives on
> Google Play, you will need to **uninstall this version** before installing
> the Play Store release.
