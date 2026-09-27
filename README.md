<div align="center">

# Pink Horizon

**A hot-pink and neon-cyan theme for [Omarchy](https://omarchy.org)**

Pink skies, neon cities, glowing labs, on a calm charcoal background. Five 4K wallpapers.

![Omarchy](https://img.shields.io/badge/Omarchy-4-ea5195?style=flat-square&labelColor=141618)
![Hyprland](https://img.shields.io/badge/Hyprland-themed-3fd6db?style=flat-square&labelColor=141618)
![Wallpapers](https://img.shields.io/badge/wallpapers-5×_4K-f463ac?style=flat-square&labelColor=141618)
![License](https://img.shields.io/badge/license-MIT-f0c987?style=flat-square&labelColor=141618)

![Pink Horizon desktop screenshot](preview.png)

</div>

---

## Contents

- [Installation](#installation)
- [Screenshots](#screenshots)
- [Wallpapers](#wallpapers)
- [What gets themed](#what-gets-themed)
- [Extras: cliamp, Zen Browser, foot](#extras)
- [Palette](#palette)
- [Updating and removing](#updating-and-removing)
- [Troubleshooting](#troubleshooting)
- [Credits and license](#credits-and-license)

---

## Installation

> Requires a recent version of [Omarchy](https://omarchy.org) (tested on Omarchy 4).

### Option 1: Omarchy menu (recommended)

1. Press <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>Space</kbd> to open the Omarchy menu.
2. Go to **Install → Style → Theme**.
3. Paste this URL and press <kbd>Enter</kbd>:

   ```
   https://github.com/padou-dev/omarchy-pink-horizon-theme.git
   ```

The theme is downloaded to `~/.config/omarchy/themes/pink-horizon` and applied right away.

### Option 2: Terminal

```bash
omarchy-theme-install https://github.com/padou-dev/omarchy-pink-horizon-theme.git
```

### Switching themes later

Open the theme picker with <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Space</kbd> and choose **Pink Horizon**.

> **Looking for the teal forest theme?** It's now called **[Teal Horizon](https://github.com/padou-dev/omarchy-teal-horizon-theme)**.

---

## Screenshots

| Desktop | Boot / unlock screen |
| :--: | :--: |
| ![Desktop](preview.png) | ![Unlock screen](preview-unlock.png) |

---

## Wallpapers

All wallpapers are **3840 × 2160**. Switch between them with the background picker: <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>Space</kbd>.

| | |
| :--: | :--: |
| ![Power Lines](media/1-power-lines-thumb.webp) | ![Neon Blaze](media/2-neon-blaze-thumb.webp) |
| **1 · Power Lines** | **2 · Neon Blaze** |
| ![Pink Flame](media/3-pink-flame-thumb.webp) | ![Cyan Lab](media/4-cyan-lab-thumb.webp) |
| **3 · Pink Flame** | **4 · Cyan Lab** |
| ![Pink Corridor](media/5-pink-corridor-thumb.webp) | |
| **5 · Pink Corridor** | |

---

## What gets themed

Omarchy generates every app's colors from this theme's single `colors.toml`, so all of these match automatically:

| Area | Apps |
|---|---|
| Desktop | Hyprland window borders (pink → cyan gradient), Omarchy shell: bar, launcher, notifications, OSD, lock screen |
| Terminals | Alacritty, Ghostty, Kitty, Foot |
| Editors | Neovim, VS Code, Helix, Obsidian |
| Browsers | Chromium, Brave, Brave Origin (toolbar color) |
| System | btop, GTK icons (Yaru-magenta), Plymouth boot screen |

---

## Extras

Some apps aren't themed by Omarchy itself. For these the repo ships ready-made files in [`extras/`](extras). Each needs a one-time setup.

<details>
<summary><b>cliamp</b> (terminal music player)</summary>

<br>

Link cliamp to the active Omarchy theme. This theme ships a `cliamp.toml`, so cliamp gets Pink Horizon's colors:

```bash
mkdir -p ~/.config/cliamp/themes
ln -sf ~/.local/state/omarchy/current/theme/cliamp.toml ~/.config/cliamp/themes/omarchy.toml
```

Then open cliamp, press <kbd>t</kbd> and pick **omarchy**, or set `theme = "omarchy"` in `~/.config/cliamp/config.toml`.

If you'd rather not link it, copy the file directly:

```bash
cp ~/.config/omarchy/themes/pink-horizon/extras/cliamp/pink-horizon.toml ~/.config/cliamp/themes/
```

</details>

<details>
<summary><b>Zen Browser</b></summary>

<br>

1. Open `about:config` and set `toolkit.legacyUserProfileCustomizations.stylesheets` to **true**.
2. Open `about:support`, then click **Profile Folder → Open Folder**.
3. Create a folder named `chrome` inside the profile folder.
4. Copy both CSS files into it:

   ```bash
   cp ~/.config/omarchy/themes/pink-horizon/extras/zen/*.css /path/to/zen/profile/chrome/
   ```

5. Make sure Zen is in dark mode, then restart it.

</details>

<details>
<summary><b>foot</b> (outside Omarchy)</summary>

<br>

On Omarchy, foot is themed automatically. For foot on another system, copy `extras/foot/pink-horizon.ini` to `~/.config/foot/` and add this line to `~/.config/foot/foot.ini`:

```ini
include=~/.config/foot/pink-horizon.ini
```

</details>

---

## Palette

| | Role | Hex | | Role | Hex |
|:-:|---|---|:-:|---|---|
| ![](https://placehold.co/18x18/141618/141618.png) | background | `#141618` | ![](https://placehold.co/18x18/f25f6b/f25f6b.png) | red | `#f25f6b` |
| ![](https://placehold.co/18x18/e6e1e4/e6e1e4.png) | foreground | `#e6e1e4` | ![](https://placehold.co/18x18/f39a6b/f39a6b.png) | orange | `#f39a6b` |
| ![](https://placehold.co/18x18/ea5195/ea5195.png) | accent | `#ea5195` | ![](https://placehold.co/18x18/f0c987/f0c987.png) | yellow | `#f0c987` |
| ![](https://placehold.co/18x18/3a2433/3a2433.png) | selection | `#3a2433` | ![](https://placehold.co/18x18/39c2ab/39c2ab.png) | green | `#39c2ab` |
| ![](https://placehold.co/18x18/6a6f75/6a6f75.png) | muted | `#6a6f75` | ![](https://placehold.co/18x18/3fd6db/3fd6db.png) | cyan | `#3fd6db` |
| ![](https://placehold.co/18x18/f9eff5/f9eff5.png) | bright foreground | `#f9eff5` | ![](https://placehold.co/18x18/5aa2d8/5aa2d8.png) | blue | `#5aa2d8` |
| | | | ![](https://placehold.co/18x18/f463ac/f463ac.png) | magenta | `#f463ac` |

---

## Updating and removing

| Task | Omarchy menu | Terminal |
|---|---|---|
| Update to the latest version | **Update → Extra Themes** | `omarchy-theme-update` |
| Remove the theme | **Remove → Theme** | `omarchy-theme-remove pink-horizon` |

---

## Troubleshooting

<details>
<summary><b>Install fails with "Failed to clone theme repo"</b></summary>

Check your internet connection and that the URL is exactly `https://github.com/padou-dev/omarchy-pink-horizon-theme.git`.
</details>

<details>
<summary><b>Updating fails with "refusing to merge unrelated histories"</b></summary>

You installed the *old* Pink Horizon (now [Teal Horizon](https://github.com/padou-dev/omarchy-teal-horizon-theme)) before it was renamed. Remove it and install this one fresh:

```bash
omarchy-theme-remove pink-horizon
omarchy-theme-install https://github.com/padou-dev/omarchy-pink-horizon-theme.git
```
</details>

<details>
<summary><b>A terminal didn't change color</b></summary>

Close and reopen it. Some terminals only read their colors at launch.
</details>

<details>
<summary><b>Icons didn't change</b></summary>

Check that the icon set is installed: `ls /usr/share/icons | grep -i yaru`.
</details>

<details>
<summary><b>cliamp shows its default colors</b></summary>

Check that the link points to a real file: `ls -l ~/.config/cliamp/themes/omarchy.toml`. It only resolves while a theme that ships `cliamp.toml` is active.
</details>

---

## Repository layout

```
.
├── backgrounds/          4K wallpapers (+ omarchy.webp logo backdrop)
├── extras/               manual-setup themes: cliamp, Zen Browser, foot
├── media/                README screenshots and wallpaper thumbnails
├── colors.toml           the palette every themed app is generated from
├── cliamp.toml           cliamp colors
├── icons.theme           icon set name
├── preview.png           theme-picker thumbnail
├── preview-unlock.png    boot/unlock screen preview
└── unlock.png            boot/unlock logo
```

---

## Credits and license

- Theme and wallpapers by **[p@nos](https://github.com/padou-dev)**. Wallpapers were upscaled to 4K with [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN).
- Built on the theme system of [basecamp/omarchy](https://github.com/basecamp/omarchy). The Zen styling follows the approach of [catppuccin/zen-browser](https://github.com/catppuccin/zen-browser).
- Sister theme: **[Teal Horizon](https://github.com/padou-dev/omarchy-teal-horizon-theme)**.

Released under the [MIT License](LICENSE).
