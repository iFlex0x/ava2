### 4. Drivers and software

You're at the desktop now. Windows is running but the hardware is kind of just sitting there confused, so we need to install drivers; which is basically just telling Windows what's actually inside the computer and how to talk to it.

**Before anything else: your RAM**

Your RAM (the G.Skill Trident Z5) has a profile called AMD EXPO that makes it run at the speed it was actually built for; 6000 MT/s. Out of the box Windows ignores this and runs it slower. Fixing it takes like thirty seconds and you do it in the BIOS before touching anything else.

- Restart and press `Delete` repeatedly as the PC is booting to get into the BIOS
- Find the **EXPO** option (it might be labeled XMP/EXPO) and enable it
- Press `F10` to save and exit

It'll restart on its own and boot back into Windows. Done, you never have to think about it again.

---

**Motherboard drivers**

Go to the [Gigabyte X870 EAGLE WIFI7 support page](https://www.gigabyte.com/Motherboard/X870-EAGLE-WIFI7-rev-1x/support) and click the Driver tab. You want these four, installed in this order:

1. **AMD Chipset Driver** — do this one first. It's the most foundational thing on the list and the rest of the drivers will behave better after it's in. Restart when it asks.
2. **Realtek HD Audio Driver** — for the audio ports on the back panel.
3. **WLAN/Bluetooth Driver** — for WiFi and Bluetooth. The board shipped with a WiFi antenna; if it's not already plugged in, there are two gold screw connectors on the back of the case and the antenna cables attach there.
4. **LAN Driver** — for the wired ethernet port.

Restart after each one when it asks you to. I know it's annoying but skipping restarts causes weird problems down the line.

While you're on that page, check the **BIOS** tab too and see if there's a newer version than what's on the board. Updating it isn't required right now but it's worth doing at some point; it usually improves memory compatibility and fixes things Gigabyte caught after launch. There are instructions on the page for how to flash it from a USB drive.

---

**GPU drivers**

NVIDIA's installer has a habit of bundling in things you genuinely do not want; GeForce Experience, a game capture tool, a screenshot app called Ansel, and multiple telemetry services that run in the background forever. The "custom install" option in NVIDIA's own installer doesn't actually let you remove most of it. We're going to use a free tool called NVcleanstall instead, which does.

- Download [NVcleanstall](https://www.techpowerup.com/download/techpowerup-nvcleanstall/) and run it
- It'll pull the latest driver for the RTX 5080 automatically
- Before clicking next, switch the driver type from **Game Ready** to **Studio Driver** in the dropdown. Studio drivers are tested against creative software specifically and are more stable for that use case; since this PC isn't for gaming there's no reason to use Game Ready.
- Click **Next** and you'll see the component list. Here's what to do with it:

Keep these:
- `Display Driver`
- `HD Audio via HDMI` (for audio through a monitor over DisplayPort or HDMI)
- `PhysX`

Remove everything else:
- `GeForce Experience` and/or `NVIDIA App`
- `Telemetry`
- `Ansel`
- `Shadowplay` / `Highlights`
- `USB-C Driver`
- `3D Vision`

Click through and install. Your screen will go black a couple times while it runs; that's normal.

---

**Corsair iCUE**

The AIO (the LINK TITAN 360) and all the fans; the six LL120s on intake, the LL140 exhausting out the back, and the three AIO fans going out the top; are all managed through Corsair's iCUE software. Without it they'll run at a fixed speed with no curve and no way to adjust them.

- Download and install [Corsair iCUE](https://www.corsair.com/us/en/s/downloads)
- It should pick up the AIO and fans automatically when it opens
- Head into **Cooling** to set up a fan curve. For a PC that's mostly sitting at a desk being used for work, something that holds around 30-40% until temperatures hit 60°C and ramps from there keeps things quiet without sacrificing cooling when it matters.
- **Lighting** is in there too if you want to set colors or just turn it all off

The LL120s and the LL140 all connect through the LINK hub inside the case so they show up together as one group in iCUE rather than individually. Should be pretty intuitive from there.

---

**WD Dashboard (optional)**

The SN850X doesn't need a driver, Windows handles it. But Western Digital has a free app called [WD Dashboard](https://support.wdc.com/downloads.aspx) that shows you drive health and temperature if you ever want to check. Worth having.