# Installation notes

This isn't intended as a one-click installer.

These are just the notes I'd follow if I had to rebuild the setup from scratch. I would still recommend taking the parts you like rather than copying everything at once.

A lot of Windows customization tools are version-sensitive, so back up any config you already have before replacing it.

## Rough order

1. Fonts
2. GlazeWM
3. YASB
4. Windhawk
5. Nilesoft Shell + Flow Launcher
6. Rainmeter
7. Windows Terminal + PowerShell + terminal tools
8. Spicetify
9. Vencord
10. Optional extras such as CKFlip3D

---

## 1. Fonts

Most of the setup uses **JetBrains Mono** and **JetBrainsMono Nerd Font**.

- JetBrains Mono: https://www.jetbrains.com/lp/mono/
- Nerd Fonts: https://www.nerdfonts.com/font-downloads

Install the fonts before setting up YASB, Windhawk, Nilesoft, Terminal, Spotify or Discord so the UI doesn't fall back to another font.

### Rainmeter clock font

My `NordClock.ini` currently uses:

```text
Sharp Grotesk 23
```

That font is **not included in this repo**. If you don't already have it, change the `Font=` value in the Rainmeter config to a font you own/have installed.

---

## 2. GlazeWM

Official project:

https://github.com/glzr-io/glazewm

My config is here:

```text
configs/glazewm/config.yaml
```

GlazeWM normally reads it from:

```text
%USERPROFILE%\.glzr\glazewm\config.yaml
```

Before copying it, check the `bind_to_monitor` values in the workspace section. My current physical layout is:

```text
monitor 0 = main landscape display
monitor 1 = portrait display
```

Workspaces `1–5` are bound to the main display and `6–9` to the portrait display.

If your monitor order is different, swap those bindings.

I also use `Alt+Shift+P` to pause/resume GlazeWM, which is useful when another app or game needs a lot of Alt-based shortcuts.

---

## 3. YASB

Official project / installation:

https://github.com/amnweb/yasb

My files:

```text
configs/yasb/config.yaml
configs/yasb/styles.css
```

They normally go in:

```text
%USERPROFILE%\.config\yasb\config.yaml
%USERPROFILE%\.config\yasb\styles.css
```

Before using the config on another machine:

- replace `YOUR_USERNAME` in the Home menu paths
- replace `HP E231` with the name of your own secondary display, or remove the portrait bar
- make sure the Nerd Font is installed

One slightly confusing bit: the `windows_workspaces` widget in my YASB config shows **Windows virtual desktops**. It is separate from the GlazeWM workspace system even though I use both.

The YASB Cava widget is the small visualizer in the top bar. The larger visualizer on the desktop is a separate Rainmeter skin.

---

## 4. Windhawk

Official project:

https://windhawk.net/

I use Windhawk for most of the native Windows styling: taskbar, Start, Explorer, fonts, borders and rounded-corner removal.

See:

```text
configs/windhawk/README.md
configs/windhawk/current-settings.json
```

`README.md` is the readable overview. `current-settings.json` is a snapshot of the settings for the **11 enabled mods** in this setup.

I would **not** blindly import registry settings from someone else's PC. Install the matching mods in Windhawk, then copy the settings into the relevant mod while checking that the version still matches closely enough.

The current setup uses, among other things:

```text
Taskbar Styler          RosePine base + square/Frost overrides
Start Menu Styler       SideBySideMinimal base + Nord overrides
File Explorer Styler    NoCommandBar + Nord header styling
Taskbar size            36px / 18px icons / 50px buttons
```

Windhawk mods can break or change after Windows updates, so this is one of the areas where I'd copy carefully rather than all at once.

---

## 5. Nilesoft Shell + Flow Launcher

### Nilesoft Shell

Official site:

https://www.nilesoft.org/

My two relevant files are:

```text
configs/nilesoft/shell.nss
configs/nilesoft/theme.nss
```

Read `configs/nilesoft/README.md` before copying them. `shell.nss` still references some of Nilesoft's normal bundled import files, which are intentionally not duplicated in this repo.

Back up your own Nilesoft files before replacing anything.

### Flow Launcher

Official site:

https://www.flowlauncher.com/

I use the existing **Nord Darker** theme without modifying or redistributing it.

There isn't much to copy from this repo for Flow Launcher; install Flow Launcher and select Nord Darker in its theme settings.

---

## 6. Rainmeter

Official site:

https://www.rainmeter.net/

I use Rainmeter for two desktop elements.

### NordClock

My clock config is included here:

```text
configs/rainmeter/NordClock.ini
```

Put it in your own Rainmeter skin folder and adjust position/font/size for your monitor if needed.

### Fountain of Colors

Original project:

https://github.com/alatsombath/Fountain-of-Colors

I don't redistribute the third-party skin itself. Install Fountain of Colors from the original project, then use the values documented in:

```text
configs/rainmeter/fountain-of-colors/README.md
```

My local audio-device ID is deliberately not included, so select the correct output device on your own PC.

---

## 7. Terminal + system info

### Windows Terminal

Official documentation:

https://learn.microsoft.com/windows/terminal/install

### PowerShell 7

Official documentation:

https://learn.microsoft.com/powershell/scripting/install/install-powershell-on-windows

My current Terminal appearance is documented in:

```text
configs/terminal/README.md
```

At the time of this snapshot I use:

```text
JetBrainsMono Nerd Font
10pt
One Half Dark
90% opacity
Acrylic enabled
```

### Fastfetch

https://github.com/fastfetch-cli/fastfetch

Config:

```text
configs/fastfetch/config.jsonc
```

### btop4win

https://github.com/aristocratos/btop4win

I use it in screenshots, but I haven't included a finished custom btop theme in this snapshot yet.

### Cava

https://github.com/karlstav/cava

Standalone config:

```text
configs/cava/nord.conf
```

YASB also has its own Cava widget settings in `configs/yasb/config.yaml`.

---

## 8. Spotify / Spicetify

Official Spicetify getting-started guide:

https://spicetify.app/docs/getting-started

I use the community **Sleek** theme with its **Nord** color scheme:

https://github.com/spicetify/spicetify-themes/tree/master/Sleek

I don't redistribute the complete Sleek theme. My repo only contains the extra CSS I added on top:

```text
configs/spicetify/rocky-nord-overrides.css
```

So the rough setup is:

1. install Spicetify using its official guide
2. install/use Sleek
3. select the Nord color scheme
4. add my overrides on top if you want the same sharper/compact look

Spotify's internal class names change, so CSS fixes may occasionally need updating.

---

## 9. Discord / Vencord

Official installer:

https://vencord.dev/download/

My current QuickCSS:

```text
configs/vencord/rocky-nord.css
```

The short setup guide is in:

```text
configs/vencord/README.md
```

The CSS uses Vencord's **ThemeAttributes** plugin for a small amount of message-specific styling:

https://vencord.dev/plugins/ThemeAttributes

Discord changes its internal classes fairly often, so parts of the CSS may need small fixes after updates.

---

## 10. Optional extras

### CKFlip3D

https://github.com/CYMERKAROL/CKFlip3D

I mostly use its default appearance and only changed mouse-hover behavior, so there isn't a custom theme to copy.

### Wallpapers

The screenshots use **Kagurabachi** artwork. I don't redistribute those files here.

General source:

https://wallhaven.cc/

I also use artwork shared through official Kagurabachi X posts. See `wallpapers/README.md` for the note about wallpaper sourcing.

---

## If I were only borrowing a few parts

If you don't want the whole setup, the easiest pieces to take independently are probably:

- the Nord palette / design-system notes
- Fastfetch config
- Vencord QuickCSS
- Spicetify overrides
- YASB styling
- individual Windhawk values

GlazeWM is the part that changes the workflow most, so I'd only add that if you actually want tiling/workspaces rather than just the visual style.

That's also more or less how this setup grew in the first place: one small change at a time.
