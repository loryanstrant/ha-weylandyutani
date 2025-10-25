![License](https://img.shields.io/github/license/loryanstrant/ha-weylandyutani)
![HACS](https://img.shields.io/badge/HACS-Default-orange.svg)


# Weyland-Yutani Theme for Home Assistant

A dark, industrial Home Assistant theme inspired by the computer terminals and aesthetic from the Alien film series, themed around the Weyland-Yutani corporation.

Pairs nicely with the [MU/TH/UR 6000 series of cards](https://github.com/loryanstrant/ha-MU-TH-UR-6000-cards).

## Overview

Transform your Home Assistant interface into a Weyland-Yutani corporation terminal with this retro-futuristic theme. Features terminal green text on authentic CRT-style brown-tinted backgrounds, reminiscent of the iconic computer screens from the USCSS Nostromo and other Weyland-Yutani installations.

<img width="707" height="191" alt="image" src="https://github.com/user-attachments/assets/1afbf466-27f0-4632-bfee-c686998db578" />


## Features

- 🎨 **Authentic Terminal Design**: Dark brown-tinted backgrounds like vintage CRT monitors
- 💚 **Terminal Green Interface**: Bright green (#00ff00) text and accents with active state highlighting
- 🏢 **Corporate Aesthetic**: Clean, professional look fitting for the Weyland-Yutani corporation
- 🚀 **Retro-Futuristic Feel**: Combines 1970s/80s computer terminal aesthetics with modern UI design
- 🔤 **Film-Accurate Typography**: Complete Thedus font family with intelligent hierarchy
- 🖼️ **Industrial Borders**: Card borders with glowing effects and technical separators
- ✅ **Complete Coverage**: All Home Assistant UI elements themed consistently
- 🎨 **Enhanced Typography System**: Complete font hierarchy using authentic Thedus variants inspired by [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/)
- 🖥️ **Authentic CRT Background**: Dark brown/sepia tint mimicking vintage monochrome terminals
- 🟢 **Unified Icon Coloring**: All icons now properly colored in terminal green
- 📐 **Visual Hierarchy**: Different font sizes and weights for titles, values, and content
- 🔲 **Terminal Borders**: Card borders with green glow effects like classic displays
- ⚡ **Card-Mod Integration**: Advanced styling using HACS card-mod for shadow DOM piercing


## Installation

### Prerequisites

**Required**: [card-mod](https://github.com/thomasloven/lovelace-card-mod) must be installed via HACS for full theme functionality.

1. Open HACS → Frontend
2. Search for "card-mod"
3. Install and restart Home Assistant

### HACS Installation (Recommended)

1. Open HACS in your Home Assistant instance
2. Go to "Frontend" section
3. Click the "+" button
4. Search for "Weyland-Yutani"
5. Click "Install"
6. Restart Home Assistant

### Manual Installation

1. Copy the `themes` folder to your Home Assistant configuration directory
2. Copy the `www` folder to your Home Assistant configuration directory
3. Add the following to your `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

4. Add font CSS to Lovelace resources:

```yaml
lovelace:
  resources:
    - url: /local/weylandyutani/fonts/alien-fonts.css
      type: css
```

5. Restart Home Assistant

## Usage

### Applying to a View

The theme works best when applied to specific views (recommended):

1. Edit your dashboard
2. Click on a view (tab)
3. Click "Edit View"
4. Under "Theme", select "weylandyutani"
5. Save

### Setting as Profile Default

1. Go to your Home Assistant profile (click your username)
2. Under "Theme", select "weylandyutani"
3. The theme applies immediately

### Setting as System Default

To set as default for all users, add to `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
  default_theme: weylandyutani
```

## Typography System

### Font Hierarchy (Alien-Inspired)

The theme implements a sophisticated typography system based on the [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/) analysis:

| Element | Font | Size | Purpose |
|---------|------|------|---------|
| **Heading Cards** | Thedus Stencil Wide | 3em | Large section titles (WEYLAND-YUTANI CORPORATION) |
| **Card Headers** | Thedus Wide | 1.8em | Card titles (Environmental Systems) |
| **Entity Names** | Thedus Wide Light | 1.2em | Sensor/device labels |
| **State Values** | Thedus Stencil Condensed | 1.4em | Bold technical readouts |
| **Secondary Info** | Thedus Condensed | 0.9em | Supporting information |
| **Buttons** | Thedus Stencil Wide | 1.1em | Industrial action buttons |
| **Body Text** | Thedus Condensed | 1em | Main content |

### Thedus Font Variants

The authentic Alien display font comes in 6 variants:

- **Thedus Wide** (Regular & Light) - Main display font for prominence
- **Thedus Condensed** (Regular & Light) - Space-efficient data readouts
- **Thedus Stencil** (Wide & Condensed) - Technical/industrial elements

All fonts load automatically via card-mod when the theme is applied to a view.

### Fallback Fonts

- **Audiowide** - Alternative display font
- **Orbitron** - Technical interface fallback
- **sans-serif** - System fallback

## Visual Design

### Color Palette

- **Primary**: Terminal Green `#00ff00`
- **Accent**: Bright Green `#33ff33` (active states)
- **Background**: Dark Brown `#0d0a08` (CRT monitor tint)
- **Cards**: Brown-tinted `#1a1410`
- **Borders**: Dark Brown `#2a1f15`
- **Inactive**: Dark Green `#004400`

### Design Elements

**Terminal Borders:**
- 2px green borders on all cards
- Glowing box-shadow effects (rgba(0, 255, 0, 0.3))
- Square corners (no border-radius)
- Header separators with gradient backgrounds

**CRT Aesthetic:**
- Dark brown/sepia background (not pure black)
- Mimics vintage monochrome terminal phosphor
- Authentic 1970s-80s spacecraft computer look

**Icon System:**
- All icons colored terminal green (#00ff00)
- Active/on states use brighter green (#33ff33)
- Square state badges (no rounded corners)


## Card Type Support

The theme includes specialized styling for:

- ✅ **Heading Cards** - Large stencil titles with top/bottom borders
- ✅ **Markdown Cards** - Condensed body text with borders
- ✅ **Entities Cards** - Full typography hierarchy with row separators
- ✅ **Button Cards** - Industrial stencil styling
- ✅ **Gauge Cards** - Green-themed visualizations
- ✅ **Graph Cards** - Terminal green plot lines
- ✅ More card types automatically inherit base styling

## Technical Details

### card-mod Integration

The theme uses advanced card-mod features:

```yaml
card-mod-theme: weylandyutani
card-mod-view-yaml: |
  # View-level styling
card-mod-card-yaml: |
  # Universal card styling
card-mod-card-type-heading-yaml: |
  # Heading card specific
card-mod-card-type-entities-yaml: |
  # Entities card specific
```

Shadow DOM piercing ensures styling applies deep into Home Assistant components.

### Browser Compatibility

- **Chrome/Edge**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Mobile**: Full support (responsive design)

### Performance

- Fonts load from local files (no external CDN)
- Minimal CSS overhead
- No JavaScript required
- Optimized for fast rendering

## Troubleshooting

### Fonts Not Loading

1. Verify card-mod is installed via HACS
2. Check that theme is applied to your view
3. Hard refresh browser (Ctrl+Shift+R / Cmd+Shift+R)
4. Check browser console (F12) for errors
5. Verify `/local/weylandyutani/fonts/` is accessible

### Icons Not Green

1. Reload themes: Developer Tools → YAML → Reload Themes
2. Clear browser cache
3. Check that view has theme applied (not just profile setting)

### Styling Not Applied

1. Confirm card-mod is loaded: Check Lovelace resources
2. Restart Home Assistant after installation
3. Apply theme to view (not just profile)
4. Check for YAML errors in theme file

## Compatibility

- **Home Assistant**: 2024.1.0 or newer (tested on beta)
- **card-mod**: Required (latest version via HACS)
- **HACS**: Recommended for installation
- **Browsers**: All modern browsers with shadow DOM support

## Development

### Repository Structure

```
ha-weylandyutani/
├── themes/
│   └── weylandyutani.yaml          # Main theme file
├── www/
│   └── fonts/
│       ├── alien-fonts.css         # Font declarations
│       ├── Thedus-Wide.otf
│       ├── Thedus-WideLight.otf
│       ├── Thedus-Condensed.otf
│       ├── Thedus-CondensedLight.otf
│       ├── Thedus-StencilWide.otf
│       └── Thedus-StencilCondensed.otf
├── screenshots/                     # Theme screenshots
├── README.md
└── LICENSE
```

### Testing

Recommended test cards for development:

```yaml
- type: heading
  heading: "WEYLAND-YUTANI CORPORATION"
- type: markdown
  content: "**SYSTEM STATUS:** OPERATIONAL"
- type: entities
  title: "Environmental Systems"
  entities:
    - sun.sun
    - sensor.time
```

### Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test with multiple card types
5. Submit a pull request

## About Weyland-Yutani

The Weyland-Yutani Corporation (often called "The Company") is the fictional mega-corporation from the Alien film series, known for its advanced technology and distinctive green-screen computer terminals aboard spacecraft like the USCSS Nostromo and Sulaco.

## Development Approach
<img width="256" height="256" alt="Vibe Coding with GitHub Copilot 256x256" src="https://github.com/user-attachments/assets/bb41d075-6b3e-4f2b-a88e-94b2022b5d4f" />

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the Alien film series and the Weyland-Yutani corporation
- Typography inspired by [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/) by Dave Addey
- Thedus font: Authentic Alien movie display font
- Created for the Home Assistant community
- Built with [card-mod](https://github.com/thomasloven/lovelace-card-mod) for advanced styling

## Support

If you encounter any issues or have suggestions:
- [Open an issue](https://github.com/loryanstrant/ha-weylandyutani/issues) on GitHub
- Check existing issues for solutions
- Include Home Assistant version and browser details

---

**Note**: This is a fan-made theme inspired by the Alien franchise. Not affiliated with or endorsed by 20th Century Studios or Disney.

**"Building Better Worlds"** - Weyland-Yutani Corporation
