# Alien Movie Typography Fonts

This directory contains the font configuration for the Weyland-Yutani Home Assistant theme, inspired by the typography analysis from [Typeset in the Future: Alien](https://typesetinthefuture.com/2014/12/01/alien/).

## Font Selections

Based on the detailed typographic analysis of the Alien movie, we've selected Google Fonts alternatives that capture the aesthetic of the original fonts:

### Display Font: Audiowide
**Original**: Thedus (custom display font)  
**Purpose**: Large headers, titles, and emphasis text  
**Why**: Audiowide captures the bold, geometric, retro-futuristic feel of Thedus with its wide letterforms and distinctive style.

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

All fonts are loaded from Google Fonts CDN via the `alien-fonts.css` file. This approach:
- Requires no local font files
- Provides automatic caching and optimization
- Falls back to system fonts for instant rendering
- Uses the `display=swap` parameter for better loading performance

## Typography Hierarchy

1. **Titles/Headers**: Audiowide (Thedus-style)
2. **Interface/Technical**: Orbitron (Eurostile-style)
3. **Body/Readable**: Montserrat (Futura-style)
4. **Code/Terminal**: IBM Plex Mono
5. **Captions/Small**: Rajdhani

## Licensing

All fonts used are open-source and available under the SIL Open Font License (OFL):
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
