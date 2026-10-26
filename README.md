# Bear Red Dark

A dark theme for [Bear](https://bear.app) on macOS, built from Bear's **Dark Graphite** theme. Bear's red replaces the blue accents, and the text is brighter for improved contrast.

## Colours

| Element | Colour |
|---|---|
| Accent (links, list bullets, cursor, ticks, pins, note-list stripe) | `#DD4C4F` |
| Editor background | `#1C1C1D` |
| Sidebar background | `#252627` |
| Sidebar icons | `#DD4C4F` (white when selected) |
| Body text | `#E8E8E8` |
| Headings | `#F4F4F4` |
| Completed to-do text | `#8A5A5F` (dim rose red) |
| Default highlight | `#7A2E31` |
| Text selection | `#5A2E30` |

## Installation

Bear does not support importing custom themes directly, so this theme replaces one of Bear's built-in themes. It uses the **Dark Notes** theme slot.

### 1. Back up and replace the original theme

Open Terminal and run:

```bash
R="/Applications/Bear.app/Contents/Frameworks/BearCore.framework/Versions/A/Resources"

# Back up the original Dark Notes theme
sudo cp "$R/Dark Notes.theme" ~/Downloads/"Dark Notes.original.theme"

# Install Bear Red Dark
sudo cp ~/Downloads/"Bear Red Dark.theme" "$R/Dark Notes.theme"
```

**Note:** Make sure `Bear Red Dark.theme` is in your `~/Downloads` directory before running these commands. You will be prompted for your password.

### 2. Restart Bear

Quit Bear completely using `⌘Q`, then reopen it.

### 3. Select the theme

Navigate to **Bear → Settings → Themes** and select **Dark Notes**.

If Bear provides a separate theme selection for dark mode, select it there as well.

## Notes

- **Bear updates:** App updates may restore the original Dark Notes theme. Repeat the installation steps after updating Bear.
- **App Store code signature:** Modifying a file inside the App Store version of Bear changes its code signature. Bear may continue to work normally, but if it refuses to open, reinstall it from the App Store.
- **Restoring the original theme:** Copy `Dark Notes.original.theme` back into the Resources directory as `Dark Notes.theme`, or reinstall Bear.
- **Completed to-dos:** Bear's themes can change the checkbox and text colours, but they cannot add strikethrough formatting to completed to-do items.

## Customisation

The theme is a JSON file. The following settings are useful when customising it:

| Setting | Purpose |
|---|---|
| `base` → accent colour | Controls the primary red accent. |
| `editor` → text font, text size, line height multiplier | Controls body typography and spacing. |
| `editor` → headers | Controls heading fonts, colours, size scales, and spacing. |
| `editor` → task → check color, border color | Controls to-do checkbox appearance. |
| `editor` → text light color | Controls completed to-do text colour. |
| `editor` → highlighter | Controls the six highlight colours. |
| `editor` → code → syntax highlight | Controls code-block syntax colours. |
| `sidebar` → icon color, background color | Controls sidebar icons and background. |

After editing the JSON file, reinstall the theme using the steps above and restart Bear for the changes to take effect.
