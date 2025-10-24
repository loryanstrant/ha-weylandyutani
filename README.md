# Weyland-Yutani Theme for Home Assistant

A dark, industrial Home Assistant theme inspired by the computer terminals and aesthetic from the Alien film series, themed around the Weyland-Yutani corporation.

![License](https://img.shields.io/github/license/loryanstrant/ha-weylandyutani)
![HACS](https://img.shields.io/badge/HACS-Default-orange.svg)

## Overview

Transform your Home Assistant interface into a Weyland-Yutani corporation terminal with this retro-futuristic theme. Features terminal green text on dark industrial backgrounds, reminiscent of the iconic computer screens from the Alien movies.

## Features

- 🎨 **Dark Industrial Design**: Deep blacks and grays reminiscent of spacecraft and corporate facilities
- 💚 **Terminal Green Interface**: Bright green (#00FF41) text and accents like classic CRT monitors  
- 🏢 **Corporate Aesthetic**: Clean, professional look fitting for a mega-corporation
- 🚀 **Retro-Futuristic Feel**: Combines 1970s/80s computer terminal aesthetics with modern UI design
- 🔤 **Authentic Typography**: Fonts inspired by the actual Alien movie design (based on Typeset in the Future analysis)
- ✅ **Complete Coverage**: All Home Assistant UI elements are themed consistently

## Installation

### HACS (Recommended)

1. Open HACS in your Home Assistant instance
2. Go to "Frontend" section
3. Click the "+" button
4. Search for "Weyland-Yutani"
5. Click "Install"
6. Restart Home Assistant

### Manual Installation

1. Copy the `themes` folder to your Home Assistant configuration directory
2. Add the following to your `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. Restart Home Assistant

## Usage

1. Go to your Home Assistant profile (click your username in the bottom left)
2. Under "Theme", select "weylandyutani" from the dropdown
3. The theme will be applied immediately

### Setting as Default Theme

To set this theme as the default for all users, add to your `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
  # Set default theme
  default_theme: weylandyutani
```

## Theme Details

### Color Palette

- **Primary Color**: Terminal Green `#00FF41`
- **Background**: Deep Black `#121212` and `#1A1A1A`
- **Accent**: Dark Green `#00B32E`
- **Warning**: Amber `#FFAA00`
- **Error**: Alert Red `#FF0000`

### Design Philosophy

This theme recreates the look and feel of the Weyland-Yutani corporation's computer systems from the Alien franchise:

- **Nostalgic CRT Aesthetic**: Green monochrome terminal displays common in 1970s-80s sci-fi
- **Industrial Design**: Dark, utilitarian interface fitting for a spacecraft or research facility  
- **High Contrast**: Excellent readability with bright text on dark backgrounds
- **Subtle Effects**: Green-tinted shadows and glows for depth
- **Authentic Typography**: Fonts inspired by the [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/) analysis

### Typography

The theme includes authentic typography inspired by [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/), providing an authentic recreation of the film's iconic computer displays:

- **Display Headers**: **Thedus** (the actual custom display font from Alien) with 6 variants (Wide, Condensed, Stencil in regular and light weights)
- **Technical Interface**: **Orbitron** (similar to Eurostile, used extensively in the film's technical displays)
- **Body Text**: **Montserrat** (similar to Futura, used throughout the film)
- **Terminal/Code**: **IBM Plex Mono** (monospace font for technical readability with a retro feel)
- **Alternative Technical**: **Rajdhani** (additional sci-fi styling option for captions and small text)
- **Alternative Terminal**: **Share Tech Mono** (retro-terminal monospace option)

The Thedus font files are loaded locally from the theme, while other fonts load from Google Fonts CDN with system font fallbacks for optimal performance.

#### Font Details

The Thedus font provides the authentic Alien movie display typography with 6 variants:
- **Thedus Wide** (regular and light weights) - The main display font
- **Thedus Condensed** (regular and light weights) - Narrower variant for space-constrained layouts
- **Thedus Stencil** (wide and condensed) - Stylized variant with stencil cutouts

These fonts are loaded locally from the theme's `www/fonts/` directory, while other fonts (Orbitron, Montserrat, IBM Plex Mono, Rajdhani, Share Tech Mono) are loaded from Google Fonts CDN.

#### Using the Fonts

The fonts are **automatically loaded** when you apply the theme - no additional configuration needed! The theme uses the `card-mod-root` directive to inject the font CSS automatically.

**Font hierarchy:**
- **Large headers/titles**: Thedus (with Audiowide fallback) for that authentic Alien movie look
- **Interface elements**: Orbitron for technical displays and buttons
- **Body text**: Montserrat for readable content
- **Code/terminal**: IBM Plex Mono for monospace displays

#### Manual Font Installation (Optional)

If automatic loading doesn't work in your setup, you can manually add fonts as a Lovelace resource:

1. Go to Settings → Dashboards → Resources (top right menu)
2. Click "+ Add Resource"
3. URL: `/local/fonts/alien-fonts.css`
4. Resource type: Stylesheet
5. Restart Home Assistant

Or add to your `configuration.yaml`:

```yaml
lovelace:
  resources:
    - url: /local/fonts/alien-fonts.css
      type: css
```

#### Verifying Fonts Are Working

To verify fonts loaded correctly:
1. Apply the Weyland-Yutani theme
2. Open browser developer tools (F12)
3. Go to Network tab and look for requests to `fonts.googleapis.com` and `/local/fonts/`
4. Headers and titles should display in Thedus and Orbitron fonts

#### Troubleshooting Fonts

**Fonts not loading?**
- Check browser console for errors (F12 → Console)
- Clear browser cache and hard reload (Ctrl+Shift+R or Cmd+Shift+R)
- Verify internet connectivity (Google Fonts require internet access)
- Try the manual installation method above

**Content Security Policy (CSP) errors?**
Add to your `configuration.yaml`:
```yaml
http:
  use_x_forwarded_for: true
  trusted_proxies:
    - 127.0.0.1
```

#### Disabling Custom Fonts

To use system fonts instead:
1. Edit `themes/weylandyutani.yaml`
2. Remove or comment out the font-family definitions
3. Remove or comment out the `card-mod-root` section
4. Restart Home Assistant

#### Font Licensing

**Thedus Font:**
- License: Free for desktop use (see `www/fonts/Desktop Commercial Use License.pdf`)
- Source: Original Alien movie display font

**Google Fonts:**
All Google Fonts used are open-source under the SIL Open Font License (OFL):
- Audiowide, Orbitron, Montserrat, IBM Plex Mono, Rajdhani, Share Tech Mono

## Screenshots

![Weyland-Yutani Theme Preview](https://github.com/user-attachments/assets/b87cab23-3196-4555-a2a3-0736c6d4dd67)

![Typography Demonstration](https://github.com/user-attachments/assets/370ffeea-e1ee-4804-a327-234b3baa7225)

The theme features:
- Dark industrial backgrounds with terminal green text
- Authentic Alien movie typography
- High contrast for excellent readability
- Retro CRT monitor aesthetic
- Complete theming of all UI components

## Compatibility

- **Home Assistant**: 2024.1.0 or newer
- **Devices**: Desktop, tablet, and mobile
- **Browsers**: All modern browsers

## About Weyland-Yutani

The Weyland-Yutani Corporation (often called "The Company") is the fictional mega-corporation from the Alien film series, known for its advanced technology and distinctive green-screen computer terminals aboard spacecraft like the Nostromo and Sulaco.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the Alien film series and the Weyland-Yutani corporation
- Typography inspired by [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/) by Dave Addey
- Thedus font: Authentic Alien movie display font (free for desktop use)
- Fonts sourced from Google Fonts (Audiowide, Orbitron, Montserrat, IBM Plex Mono, Rajdhani, Share Tech Mono)
- Created for the Home Assistant community

## Support

If you encounter any issues or have suggestions, please [open an issue](https://github.com/loryanstrant/ha-weylandyutani/issues) on GitHub.

---

**Note**: This is a fan-made theme inspired by the Alien franchise. Not affiliated with or endorsed by 20th Century Studios or Disney.
