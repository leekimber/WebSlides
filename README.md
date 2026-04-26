# WebSlides (Vanilla Fork)

A localized, self-contained fork of [WebSlides](https://github.com/webslides/webslides) by José Luis Antúnez.

## What's Different

This fork modifies the original WebSlides demos to:

1. **Fix errors** - Applied community pull requests and bug fixes to the original demo HTML files
2. **Localize all assets** - All CSS, JavaScript, fonts, and images are served locally
3. **Remove external dependencies** - Google Fonts replaced with local webfonts; no CDN calls for framework assets

## Quick Start

### Development Server (with auto-reload)

```bash
# Requires reloadserver installed
reloadserver 8444 --certificate reference/server.pem
```

Then browse to: **https://localhost:8444/demos/**

### Alternative: Python HTTP Server

```bash
# Without HTTPS/auto-reload
python3 -m http.server 8000
```

Then browse to: **http://localhost:8000/demos/**

## Structure

```
webslides/
├── demos/           # Corrected HTML demo files
├── static/
│   ├── css/         # webslides.css, svg-icons.css
│   ├── js/          # webslides.js, svg-icons.js
│   ├── images/      # Favicons and demo images
│   └── webfonts/    # Roboto, Maitree, Cousine, San Francisco
├── reference/       # Backup of corrected files (not in git)
├── LICENSE          # MIT License (original + fork modifications)
└── README.md        # This file
```

## Original WebSlides

- **Author:** José Luis Antúnez (@jlantunez)
- **Repository:** https://github.com/webslides/webslides
- **License:** MIT

## License

MIT License - see [LICENSE](LICENSE) for details.
