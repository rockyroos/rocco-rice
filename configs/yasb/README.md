# YASB

The files in this folder are a public-safe copy of my current YASB setup.

## Files

```text
config.yaml
styles.css
```

YASB normally reads these from:

```text
%USERPROFILE%\.config\yasb\config.yaml
%USERPROFILE%\.config\yasb\styles.css
```

## Things to change on another PC

- Replace `YOUR_USERNAME` in the Home menu paths.
- Replace `HP E231` with the name of your own portrait/secondary monitor, or remove the second bar if you only use one screen.
- The `windows_workspaces` widget in this config is YASB's **Windows virtual desktop** widget. It is not a GlazeWM workspace widget, even though I use GlazeWM alongside it.

The main bar is 28px high and includes clock, traffic, CPU/RAM, active-window info, media and a 16-bar Cava visualizer. The portrait bar is intentionally much simpler.
