# Windhawk

These are the Windhawk mods currently used by this setup.

The list below was checked against the live Windhawk installation on 15 September 2026 and matches the current enabled mods shown in the app.

## Enabled mods

| Mod | Version | Notes |
|---|---:|---|
| Disable rounded corners in Windows 11 | 1.0.1 | Removes most native Windows rounding |
| Explorer Font Changer | 0.2 | `JetBrainsMono NFM` |
| Taskbar auto-hide when maximized | 1.2.6 | `mode = intersected` |
| Taskbar Clock Customization | 1.8 | Two-line JetBrains Mono clock/date |
| Taskbar height and icon size | 1.3.10 | 36px taskbar, 18px icons, 50px buttons |
| Taskbar Labels for Windows 11 | 1.4.5 | Compact labels + full-width running indicator |
| Taskbar Volume Control Per-App | 1.1.4 | 5% step, Ctrl-click to mute |
| Window Border Customizer | 1.0.1 | Transparent custom border |
| Windows 11 File Explorer Styler | 1.6 | `NoCommandBar` + Nord header colors |
| Windows 11 Start Menu Styler | 1.7 | `SideBySideMinimal` + square/Nord overrides |
| Windows 11 Taskbar Styler | 1.10 | `RosePine` base + square overrides + Frost indicators |

## Important disabled mods

A few installed mods are intentionally disabled and are not part of the current look:

- Explorer Details Better File Sizes
- Slick Window Arrangement
- Taskbar Dock Animation
- Taskbar Notification Icon Spacing
- Taskbar Start Button Position
- Taskbar Volume Control
- Windows 11 Notification Center Styler

Taskbar Dock Animation still has an old saved `MaxScale = 120`, but it is disabled in the current setup.

## Key current settings

### Taskbar size

```text
TaskbarHeight = 36
IconSize = 18
TaskbarButtonWidth = 50
IconSizeSmall = 24
TaskbarButtonWidthSmall = 40
```

### Taskbar labels

```text
mode = labelsWithCombining
maximumTaskbarItemWidth = 100
runningIndicatorStyle = fullWidth
progressIndicatorStyle = fullWidth
fontSize = 11
fontFamily = JetBrainsMono NF
leftAndRightPaddingSize = 10
spaceBetweenIconAndLabel = 10
```

### Taskbar clock

```text
TopLine = %time%
BottomLine = %date%
Width = 150
Height = 36
TextSpacing = -2
Time font = JetBrainsMono NFM / 9 / Medium
Date font = JetBrainsMono NFM / 8 / Normal
```

### Explorer

```text
theme = NoCommandBar
backgroundTranslucentEffect = none
explorerFrameContainerHeight = 0
NavigationBar background = #2e3440
Tab text = #d8dee9
Selected tab = #3b4252
```

### Start menu

The Start Menu Styler uses `SideBySideMinimal` as a base, with square corners, JetBrains Mono text and Nord resource colors. Font icons are left on the Windows icon fonts so glyphs keep working.

### Taskbar Styler

The Taskbar Styler uses `RosePine` as a base, but the visible task buttons, tray and running indicators are overridden toward the rest of this rice: square corners and `#88C0D0` Frost running indicators.

## Note

Windhawk settings are version-sensitive. I recommend copying the parts you want instead of importing a registry snapshot wholesale.
