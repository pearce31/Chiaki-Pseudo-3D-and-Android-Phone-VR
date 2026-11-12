# Chiaki 3D — stereoscopic PlayStation Remote Play (SBS · Anaglyph · VR)

On-device mods of **Chiaki** (PlayStation Remote Play client) that add stereoscopic
3D output, in three flavors. Pick the download that matches your setup.

> ⚠️ **Unofficial fan mod.** Not affiliated with, endorsed by, or certified by
> Sony Interactive Entertainment, nor by the Chiaki authors. "PlayStation" and
> "PS5" are trademarks of Sony Interactive Entertainment; used here only to
> describe compatibility.

## The three versions
| Version | What it does | Get |
|---|---|---|
| **VR** | Head-tracked floating widescreen for a lensed headset — barrel-distortion lens pass, in-headset gamepad calibration, saved settings. L3 + R3 then d pad to adjust/navigate and A or X to recenter | `chiaki-vr.apk` |
| **SBS** | Plain side-by-side 3D output, no head tracking | `chiaki-sbs.apk` |
| **Anaglyph** | Green/magenta anaglyph 3D (I use trioviz inficolor glasses off amazon and it's probably the best there is as far as Anaglyph goes) | `chiaki-anaglyph.apk` |

**Downloads:** grab the APK for your version from the **[Releases](../../releases)** tab.

## Lume Pad 2 — glasses-free 3D
A fourth variant that weaves the PS5 stream into **glasses-free 3D** on the **Lume Pad 2**'s Leia lightfield panel — no glasses, no headset, no viewer mount. Head tracking steers the views. Same Chiaki base and GPLv3 as the versions above.

**Download:** `chiaki-lumepad.apk` — from the **[Releases](../../releases)** tab.

## Based on / credits
Derivative works of the **Chiaki** project by **Florian Märkl**, licensed under
the GNU General Public License v3.0.
- Upstream (original): https://github.com/thestr4ng3r/chiaki
- Active fork: https://github.com/streetpea/chiaki-ng
- **Base I modified:** the original Chiaki, installed from **F-Droid**
  (https://f-droid.org/packages/com.metallic.chiaki/). All 3D work here is my own,
  built on top of that base.

## License
**GPL-3.0-or-later** — required, because Chiaki is GPLv3 and these build on it.
All modifications in this repo are released under the same license. See `LICENSE`.

## Source (one zip per version)
Each zip is the complete **smali** source of that build, decompiled with
MT Manager / apktool — the human-readable source those tools edit, not a raw binary.
- `smali-vr.zip` → source for `chiaki-vr.apk`
- `smali-sbs.zip` → source for `chiaki-sbs.apk`
- `smali-anaglyph.zip` → source for `chiaki-anaglyph.apk`

The VR version's main classes live under `com/metallic/chiaki/stream/`:
`AnaglyphRenderer.smali` (stereo renderer + lens-warp + calibration),
`HeadTracker.smali` (head tracking), `StreamActivity.smali` (wiring).

## How to build / apply (on-device)
1. Decompile the F-Droid Chiaki APK with **MT Manager** / **apktool**.
2. Replace its `smali/` folder with the contents of the matching `smali-*.zip`.
3. Rebuild and **sign** with your own key, then install.

Built and maintained entirely on-device — no PC toolchain required.

---

## P5M (modified) — PS5 Remote Play in VR on Quest 3
A separate app, not a Chiaki Remote Play flavor: a modified build of **P5M**, which streams PS5 Remote Play to a floating VR screen on the **Meta Quest 3**. This build uses my own custom depth 3D in place of the default.

**Download:** `p5m-modified.apk` — from the **[Releases](../../releases)** tab.

**Based on / credits:** [P5M](https://github.com/beecrepaldi-afk/P5M) by beecrepaldi-afk, which builds on [chiaki-ng](https://github.com/streetpea/chiaki-ng) and [Chiaki](https://github.com/thestr4ng3r/chiaki) by Florian Märkl.

**License:** AGPL-3.0 (inherited from chiaki-ng / Chiaki).
