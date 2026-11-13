<h1 align="center">✦ minimal dusk ✦</h1>

<p align="center">
  <i>a quiet, dark purple dwm rice for Arch Linux</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/WM-dwm-6a2fb0?style=for-the-badge&labelColor=120a1f" alt="dwm">
  <img src="https://img.shields.io/badge/Terminal-st-9d4edd?style=for-the-badge&labelColor=120a1f" alt="st">
  <img src="https://img.shields.io/badge/Launcher-rofi-6a2fb0?style=for-the-badge&labelColor=120a1f" alt="rofi">
  <img src="https://img.shields.io/badge/OS-Arch_Linux-9d4edd?style=for-the-badge&labelColor=120a1f" alt="arch">
</p>

<p align="center">
  <img src="screenshots/desktop.png" alt="desktop" width="90%">
</p>

---

## ◈ about

A minimal setup built around one idea: deep purple, low noise, nothing extra.
Gaps, a slim bar, Nerd Font tag icons, and a moody black hole wallpaper.

## ◈ details

|            |                                          |
| ---------- | ---------------------------------------- |
| **OS**     | Arch Linux                               |
| **WM**     | dwm                                      |
| **Term**   | st 0.9.3                                 |
| **Launcher** | rofi (drun)                            |
| **Files**  | pcmanfm                                  |
| **Font**   | JetBrainsMono Nerd Font · Noto Color Emoji |
| **Compositor** | xcompmgr                             |
| **Wallpaper** | feh · [source](#)                     |

## ◈ palette

| Color | Hex | Role |
| :---: | --- | --- |
| ![](https://img.shields.io/badge/-%20%20%20-120a1f) | `#120a1f` | bar background |
| ![](https://img.shields.io/badge/-%20%20%20-2a1a47) | `#2a1a47` | inactive border |
| ![](https://img.shields.io/badge/-%20%20%20-cdbfe8) | `#cdbfe8` | inactive text |
| ![](https://img.shields.io/badge/-%20%20%20-6a2fb0) | `#6a2fb0` | active tag |
| ![](https://img.shields.io/badge/-%20%20%20-9d4edd) | `#9d4edd` | active border |
| ![](https://img.shields.io/badge/-%20%20%20-f0e6ff) | `#f0e6ff` | active text |

## ◈ patches

**dwm**
- bar padding (`vertpad`, `sidepad`) — *fill in the patch name*

**st**
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [scrollback-mouse](https://st.suckless.org/patches/scrollback/)

## ◈ install

```sh
git clone git@github.com:Diavalga/minimal-dusk-dwm.git
cd minimal-dusk-dwm

cd dwm && sudo make clean install
cd ../st && sudo make clean install
```

<details>
<summary><b>dependencies</b></summary>

```sh
sudo pacman -S base-devel libx11 libxft libxinerama \
    rofi feh xcompmgr pcmanfm scrot xclip \
    brightnessctl wireplumber \
    ttf-jetbrains-mono-nerd noto-fonts-emoji
```

</details>

<details>
<summary><b>~/.xinitrc</b></summary>

```sh
~/.fehbg &
xcompmgr &
exec dwm
```

</details>

## ◈ keybinds

`Mod` = Super key

<details open>
<summary><b>apps</b></summary>

| Keybind | Action |
| --- | --- |
| `Mod + t` | terminal |
| `Mod + p` | launcher |
| `Mod + e` | file manager |
| `Mod + Shift + s` | screenshot area to clipboard |

</details>

<details>
<summary><b>windows & layouts</b></summary>

| Keybind | Action |
| --- | --- |
| `Mod + j / k` | focus next / previous |
| `Mod + h / l` | shrink / grow master |
| `Mod + i / d` | more / fewer masters |
| `Mod + Enter` | swap with master |
| `Mod + Shift + c` | close window |
| `Mod + Shift + t` | tile |
| `Mod + f` | floating |
| `Mod + m` | monocle |
| `Mod + Space` | cycle layout |
| `Mod + Shift + Space` | toggle floating |
| `Mod + b` | toggle bar |

</details>

<details>
<summary><b>tags</b></summary>

| Keybind | Action |
| --- | --- |
| `Mod + 1-9` | view tag |
| `Mod + Shift + 1-9` | move window to tag |
| `Mod + 0` | view all tags |
| `Mod + Shift + q` | quit dwm |

</details>

<details>
<summary><b>function keys</b></summary>

| Keybind | Action |
| --- | --- |
| `F1 / F2 / F3` | mute / volume down / volume up |
| `F4 / F5` | brightness down / up |
| `F8` | mirror to HDMI *(edit output names in `config.h`)* |
| `F11` | full screenshot to `~/Pictures` |

</details>

## ◈ credits

- [suckless.org](https://suckless.org) for dwm and st
- Wallpaper by *add author*

## ◈ license

dwm and st are under the MIT/X Consortium license. See the `LICENSE` file in each folder.

<p align="center">
  <sub>✦ made with purple ✦</sub>
</p>
