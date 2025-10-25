# Enhanced Typography System with Authentic CRT Styling

## 🎨 Overview

This PR introduces a comprehensive typography overhaul and visual enhancements that bring the Weyland-Yutani theme closer to the authentic Alien movie aesthetic, inspired by [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/).

## ✨ Key Features

### Typography System
- **Complete font hierarchy** using all 6 Thedus variants (Wide, Condensed, Stencil in regular and light weights)
- **Intelligent sizing**: Heading cards (3em), card headers (1.8em), entity names (1.2em), values (1.4em), etc.
- **Film-accurate styling**: Letter spacing, uppercase transforms, and weight adjustments matching the Nostromo displays

### Visual Enhancements
- **Authentic CRT background**: Dark brown/sepia tint (#0d0a08, #1a1410) mimicking vintage monochrome terminals
- **Terminal borders**: 2px green borders with glowing effects on all cards
- **Unified icon system**: All icons properly colored in terminal green (#00ff00) with brighter active states (#33ff33)
- **Industrial separators**: Entity row borders and card header gradients

### Technical Improvements
- **card-mod integration**: Advanced shadow DOM piercing for deep styling
- **Type-specific styling**: Specialized configurations for heading, markdown, and entities cards
- **Performance optimized**: Local font loading, minimal CSS overhead

## 🖼️ Screenshots

**Note**: Please add screenshots of the weyland2 view showing:
- Full dashboard overview
- Typography hierarchy in action
- Card styling details with borders and icons

Screenshots should be saved in the `screenshots/` directory as:
- `overview.png`
- `typography.png`
- `cards.png`

## 📝 Changes

### Modified Files
- `themes/weylandyutani.yaml` - Complete theme rewrite with card-mod integration
- `www/fonts/alien-fonts.css` - Fixed font paths for proper loading
- `README.md` - Comprehensive documentation update for v2.0
- `screenshots/README.md` - Added placeholder with instructions

### Typography Hierarchy

| Element | Font | Size | Purpose |
|---------|------|------|---------|
| Heading Cards | Thedus Stencil Wide | 3em | Large section titles |
| Card Headers | Thedus Wide | 1.8em | Card titles |
| Entity Names | Thedus Wide Light | 1.2em | Sensor/device labels |
| State Values | Thedus Stencil Condensed | 1.4em | Bold technical readouts |
| Secondary Info | Thedus Condensed | 0.9em | Supporting information |
| Buttons | Thedus Stencil Wide | 1.1em | Industrial buttons |

### Color Updates

- **Background**: `#0d0a08` (primary), `#1a1410` (secondary) - Dark brown CRT tint
- **Borders**: `#2a1f15` - Subtle brown separation
- **Icons**: `#00ff00` (default), `#33ff33` (active)

## 🧪 Testing

Tested with:
- Home Assistant Beta version
- Multiple card types (heading, markdown, entities)
- Multiple browsers (confirmed font loading and styling)
- card-mod integration verified

## 📚 Documentation

- Complete README rewrite with v2.0 features
- Added typography hierarchy table
- Added troubleshooting section
- Added installation prerequisites (card-mod requirement)
- Added usage instructions for view-level theme application

## 🎯 Breaking Changes

**None** - This is a visual enhancement that maintains backward compatibility. Existing installations will automatically benefit from the improvements after update.

## 📋 Requirements

- **card-mod** must be installed via HACS for full functionality
- Home Assistant 2024.1.0 or newer

## 🚀 Next Steps

After merging:
1. Add actual screenshots from the weyland2 view
2. Consider creating a HACS submission for wider distribution
3. Potential future enhancements:
   - Additional card type styling (gauge, graph, button cards)
   - Animated scanline effects
   - Custom UI sounds (Nostromo beeps?)

---

**"Building Better Worlds"** - Weyland-Yutani Corporation

Inspired by the iconic computer terminals from Alien (1979) and the comprehensive typographic analysis by [Typeset in the Future](https://typesetinthefuture.com/2014/12/01/alien/).
