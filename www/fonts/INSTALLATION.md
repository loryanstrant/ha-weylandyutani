# Font Installation and Usage Guide

## Automatic Font Loading (Recommended)

The Weyland-Yutani theme includes automatic font loading via the `card-mod-root` directive in the theme YAML. When you apply the theme, fonts will automatically load from Google Fonts CDN.

### What You Need

No additional installation is required! Simply:

1. Install the theme via HACS or manually
2. Apply the theme in your Home Assistant profile
3. Fonts will load automatically from Google Fonts

### Font Files Location

- CSS file: `www/fonts/alien-fonts.css`
- This file is automatically referenced by the theme
- Fonts are loaded from Google Fonts CDN (no local font files needed)

## Manual Installation (Alternative Method)

If you prefer to manually add the fonts or if automatic loading doesn't work, you can add the fonts as a Lovelace resource:

### Step 1: Ensure Files Are In Place

Make sure the `www/fonts/alien-fonts.css` file exists in your Home Assistant config directory:
```
/config/www/fonts/alien-fonts.css
```

### Step 2: Add Lovelace Resource

Add to your `configuration.yaml`:

```yaml
lovelace:
  mode: yaml  # or storage
  resources:
    - url: /local/fonts/alien-fonts.css
      type: css
```

Or, if using Lovelace UI mode, go to:
1. Settings → Dashboards → Resources (top right menu)
2. Click "+ Add Resource"
3. URL: `/local/fonts/alien-fonts.css`
4. Resource type: Stylesheet

### Step 3: Restart Home Assistant

Restart Home Assistant to load the new resources.

## Verifying Font Installation

To verify fonts are loading correctly:

1. Apply the Weyland-Yutani theme
2. Open browser developer tools (F12)
3. Go to Network tab
4. Look for requests to `fonts.googleapis.com`
5. Headers and card titles should appear in the Audiowide and Orbitron fonts

## Font Fallbacks

The theme includes system font fallbacks, so even if Google Fonts fails to load:
- **Helvetica/Arial** will be used for sans-serif text
- **Courier New** will be used for monospace/code text

This ensures the theme always looks good, even with limited connectivity.

## Troubleshooting

### Fonts Not Loading

1. **Check browser console** for errors
2. **Verify the CSS file exists** at `/config/www/fonts/alien-fonts.css`
3. **Clear browser cache** and reload
4. **Check internet connectivity** (fonts load from Google Fonts CDN)
5. **Try manual installation** using the Lovelace resources method above

### Content Security Policy Issues

If you see CSP errors in the console:

1. Add to `configuration.yaml`:
```yaml
http:
  use_x_forwarded_for: true
  trusted_proxies:
    - 127.0.0.1
```

2. Or, download the fonts locally and host them from the `www` directory instead of using Google Fonts CDN

### Fonts Look Different

- **Font weights may vary** depending on which weights are available
- **Browser rendering** can affect font appearance
- **System fonts** may be used as fallbacks if Google Fonts doesn't load

## Performance Considerations

- Fonts load asynchronously with `display=swap`
- System fonts appear instantly while custom fonts load
- Fonts are cached by the browser after first load
- Minimal performance impact on Home Assistant

## Disabling Custom Fonts

If you prefer to use system fonts only:

1. Edit `themes/weylandyutani.yaml`
2. Remove or comment out the font-family definitions (lines 13-21)
3. Remove or comment out the `card-mod-root` section (lines 171-176)
4. Restart Home Assistant

## Font Licensing

All fonts are open-source and free to use:
- Licensed under SIL Open Font License (OFL)
- No attribution required for end users
- Safe for personal and commercial use
- Hosted on Google Fonts infrastructure

For more details on each font, see `www/fonts/README.md`.
