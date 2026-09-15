# Vencord

Discord in this setup uses **Vencord** with my current QuickCSS in `rocky-nord.css`.

The goal is to keep Discord visually consistent with the rest of the desktop: Nord colors, JetBrains Mono, sharp corners, compact spacing and Frost accents.

## Setup

1. Install Vencord using the official installer:
   https://vencord.dev/download/
2. Open Discord → Settings → Vencord → Plugins.
3. Search for **ThemeAttributes** and enable it:
   https://vencord.dev/plugins/ThemeAttributes
4. Enable **Custom CSS** in Vencord settings.
5. Open QuickCSS and paste the contents of `rocky-nord.css`.
6. Restart/reload Discord if needed.

## Notes

- `ThemeAttributes` is used for a small amount of attribute-based styling, such as the subtle styling for my own messages.
- If Discord's `ClientTheme` overrides the custom palette, disable it.
- Discord changes class names fairly often, so parts of the CSS may need small fixes after updates.
- This repo only includes my QuickCSS and setup notes. Vencord itself is not redistributed here.

## Official resources

- Vencord download / installer: https://vencord.dev/download/
- ThemeAttributes plugin: https://vencord.dev/plugins/ThemeAttributes
- Vencord site: https://vencord.dev/
