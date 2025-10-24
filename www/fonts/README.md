# Alien Movie Typography Fonts

This directory contains the font configuration for the Weyland-Yutani Home Assistant theme, inspired by the typography analysis from [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/).

## Font Selections

Based on the detailed typographic analysis of the Alien movie, this theme now includes the authentic fonts and carefully selected alternatives:

### Display Font: Thedus (Authentic)
**Type**: Original Alien movie display font  
**Purpose**: Large headers, titles, and emphasis text  
**Why**: Thedus is the actual custom display font used in the Alien film, providing authentic movie typography. The theme includes multiple variants:
- Thedus Wide (regular and light)
- Thedus Condensed (regular and light)
- Thedus Stencil (wide and condensed)

**Fallback**: Audiowide provides a similar aesthetic if the local font fails to load.

### Technical Interface: Orbitron
**Original**: Eurostile Extended  
**Purpose**: Technical displays, UI elements, primary interface text  
**Why**: Orbitron is a geometric sans-serif with a distinctly technical, space-age feel similar to Eurostile, which was heavily used in the film's computer displays.

### Body Text: Montserrat
**Original**: Futura  
**Purpose**: General body text, descriptions, readable content  
**Why**: Montserrat is a geometric sans-serif inspired by Futura, offering excellent readability while maintaining the clean, modernist aesthetic.

### Terminal/Code: IBM Plex Mono
**Original**: Various monospace fonts  
**Purpose**: Code blocks, terminal displays, technical data  
**Why**: IBM Plex Mono provides excellent readability for technical content with a slightly retro feel appropriate for 1970s-era computer terminals.

### Alternative Technical: Rajdhani
**Original**: Various sans-serif fonts  
**Purpose**: Captions, small text, additional technical styling  
**Why**: Rajdhani offers a condensed, technical appearance perfect for secondary UI elements.

### Alternative Terminal: Share Tech Mono
**Original**: Terminal displays  
**Purpose**: Alternative monospace option  
**Why**: Share Tech Mono has a distinct retro-terminal feel ideal for code and technical displays.

## Font Loading

The theme uses a hybrid approach for font loading:
- **Thedus**: Loaded locally from the `www/fonts/` directory in OTF format
- **Google Fonts**: Orbitron, Montserrat, IBM Plex Mono, Rajdhani, and Share Tech Mono are loaded from Google Fonts CDN
- **Audiowide**: Kept as a fallback for Thedus if local font fails to load

This approach:
- Provides the authentic Alien movie font experience
- Maintains automatic caching and optimization for web fonts
- Falls back to system fonts for instant rendering
- Uses the `display=swap` parameter for better loading performance

## Typography Hierarchy

1. **Titles/Headers**: Thedus (authentic Alien display font) with Audiowide fallback
2. **Interface/Technical**: Orbitron (Eurostile-style)
3. **Body/Readable**: Montserrat (Futura-style)
4. **Code/Terminal**: IBM Plex Mono
5. **Captions/Small**: Rajdhani

## Licensing

Fonts used in this theme:

### Thedus Font
- **License**: Free for desktop use (see `Desktop Commercial Use License.pdf`)
- **Source**: Original Alien movie display font
- **Files**: 6 variants included (Wide, Condensed, Stencil in regular and light weights)

### Google Fonts (SIL Open Font License)
All Google Fonts used are open-source and available under the SIL Open Font License (OFL):
- Audiowide by Astigmatic
- Orbitron by The League of Moveable Type
- Montserrat by Julieta Ulanovsky
- IBM Plex Mono by IBM
- Rajdhani by Indian Type Foundry
- Share Tech Mono by Carrois Type Design

## References

- [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/) - Comprehensive typography analysis
- [Google Fonts](https://fonts.google.com/) - Font source
- Alien (1979) - Original film
