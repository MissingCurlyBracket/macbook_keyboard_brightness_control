# Keyboard Brightness Control for macOS

A [Karabiner-Elements](https://karabiner-elements.pqrs.org/) configuration that maps **⌘ + F1** and **⌘ + F2** to decrease and increase your MacBook's keyboard backlight brightness.

## Why?

Modern MacBooks make it surprisingly annoying to adjust keyboard backlight on the fly. This config restores a quick shortcut.

| Shortcut | Action |
| --- | --- |
| `⌘ + F1` | Decrease keyboard brightness |
| `⌘ + F2` | Increase keyboard brightness |

## Requirements

- macOS
- [Karabiner-Elements](https://karabiner-elements.pqrs.org/) installed and running

If you don't have Karabiner-Elements yet, install it with Homebrew:

```bash
brew install --cask karabiner-elements
```

Or download it directly from the [official site](https://karabiner-elements.pqrs.org/).

On first launch, macOS will ask you to grant Karabiner-Elements several permissions (Input Monitoring, Accessibility, and a driver extension). Follow the prompts — the app walks you through it.

## Installation
 
1. Open Karabiner-Elements.
2. Go to the **Complex Modifications** tab.
3. Click **Add your own rule**.
4. Paste the contents of `keyboard-brightness.json` from this repo into the text field.
5. Save, then click **Enable** on the rule.
## Verifying it works
 
1. Make sure Karabiner-Elements is running (you'll see its icon in the menu bar).
2. Press **⌘ + F2**. Your keyboard backlight should get brighter.
3. Press **⌘ + F1**. It should dim.
If nothing happens, check the **Devices** tab in Karabiner-Elements and make sure your keyboard is enabled.
 
## Troubleshooting
 
**The shortcut does nothing.**
Some apps capture `⌘ + F1`/`F2` themselves (older Microsoft Office, some remote desktop tools). Try the shortcut from Finder to confirm the mapping works, then check app-specific keybindings.
 
**F1/F2 already trigger brightness without holding ⌘.**
That's expected on MacBooks where "Use F1, F2, etc. keys as standard function keys" is **off** in System Settings → Keyboard. This config is designed to coexist with that default — holding ⌘ is what activates the keyboard backlight mapping.
 
**Karabiner-Elements isn't capturing key events at all.**
Open System Settings → Privacy & Security → Input Monitoring, and confirm `karabiner_grabber` and `karabiner_observer` are both enabled. A restart of Karabiner-Elements (or your Mac) usually resolves lingering permission issues.
