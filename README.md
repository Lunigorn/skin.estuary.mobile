# Estuary Mobile — Mobile-optimized Estuary skin (fork)

Estuary Mobile is a compact, touch-friendly fork of the default Estuary skin for [Kodi](https://github.com/xbmc/xbmc). It retains Estuary's familiar appearance while adjusting layout and controls for reliable use on phones and other small, touch-driven devices.

**Overview:** This fork focuses on improving ergonomics on small screens: controls are larger, visual targets are spaced for fingers, and video playback includes dedicated quick-seek buttons.

**Features:**
- **Larger touch targets:** Buttons and interactive items are scaled and spaced to reduce mis-taps.
- **Bigger progress bar:** The video progress/scrub control is taller and easier to interact with by touch.
- **Dedicated quick-seek controls:** Two on-screen buttons added during playback — one to jump forward +10 seconds, and one to jump backward -10 seconds — for convenient skipping.
- **Preserves Estuary look:** Visual design and most behaviours are unchanged unless necessary for mobile usability.

**Installation**
- Copy this skin folder into Kodi's `addons` directory for your platform and restart Kodi. Then select the skin in `Settings -> Interface -> Skin`.
- Or package the repository root as a ZIP archive (ensure `addon.xml` is at the top level) and install it from Kodi via `Add-ons -> Install from zip file`.

**Usage notes**
- The quick-seek buttons are visible in the video playback controls. Tap the right seek button to move forward 10 seconds; tap the left seek button to move back 10 seconds. Repeated taps apply the action repeatedly.
- The enlarged progress bar responds to drag and tap gestures for faster and more accurate seeking with a finger.

**Customization**
- Swap color themes in the `colors/` directory to change palettes.
- To fine-tune spacing, sizes or behaviour, edit the skin XML files under `xml/` and `resources/`. Look for playback and control definitions to adjust dimensions and positions.

**Changelog**
- v0.1.0 — Initial mobile release
	- Increased button and control sizes for touch devices.
	- Enlarged video progress bar.
	- Added +10s and -10s on-screen seek buttons for video playback.
	- Increased height of context menus buttons.

**Contributing**
- Issues and pull requests are welcome. For larger UI changes, open an issue first to discuss intended behaviour and testing on devices.

**Maintainers**
- Maintained by the repository owner. Please include a description of the screen resolution, the screen size and Kodi version when reporting mobile-specific issues.

**Credits & License**
- This project is a derivative of the Estuary skin bundled with Kodi; original credits belong to the Kodi project and contributors.
- See `LICENSE.txt` for license information.

**Backporting upstream changes**

If you want to pull updates from the original Estuary skin (the upstream `xbmc` repository) into this fork, one convenient method is to create a subtree split of `addons/skin.estuary` in a local clone of `xbmc` and then pull that branch into this repository. Example commands:

```powershell
git clone https://github.com/xbmc/xbmc.git
cd xbmc
git subtree split --prefix=addons/skin.estuary -b master-estuary

cd ../skin.estuary.mobile
git pull ../xbmc master-estuary
```

Notes:

Replace `../skin.estuary.mobile` with the actual path to this repository.

**Note about included upstream commits**

This repository incorporates commits from the original Estuary skin. Keeping those upstream commits in history makes it simpler to merge or rebase later updates from the official `xbmc` source and reduces the amount of manual conflict resolution when backporting improvements.
