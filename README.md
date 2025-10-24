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

## Screenshots

![Weyland-Yutani Theme Preview](https://github.com/user-attachments/assets/b87cab23-3196-4555-a2a3-0736c6d4dd67)

The theme features:
- Dark industrial backgrounds with terminal green text
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
- Created for the Home Assistant community

## Support

If you encounter any issues or have suggestions, please [open an issue](https://github.com/loryanstrant/ha-weylandyutani/issues) on GitHub.

---

**Note**: This is a fan-made theme inspired by the Alien franchise. Not affiliated with or endorsed by 20th Century Studios or Disney.
