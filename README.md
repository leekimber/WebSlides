# WebSlides Vanilla

A self-contained, offline-ready fork of [WebSlides](https://github.com/webslides/webslides) — a minimal HTML/CSS/JS framework for creating beautiful presentations and landings.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## What's Different

This fork modifies the original WebSlides to be **fully self-contained**:

| Feature | Original WebSlides | WebSlides Vanilla |
|---------|-------------------|-------------------|
| **Fonts** | Google Fonts (CDN) | Local webfonts |
| **Assets** | Some hotlinked to webslides.tv | All local |
| **Dependencies** | External CDN calls | Zero external dependencies |
| **Offline** | Requires internet | Works offline |

## Quick Start

### Option 1: Development Server (with auto-reload)

```bash
# Install reloadserver (if not already installed)
pip install reloadserver

# Or for better long-term consistency:
pipx install reloadserver

# Create a combined self-signed key+certificate for HTTPS:
openssl req -x509 -newkey rsa:2048 -nodes -out ~/projects/dev-server.pem -keyout ~/projects/dev-server.pem -days 365 -subj "/CN=localhost" 

# Start server with HTTPS
reloadserver 8444 --certificate ~/projects/dev-server.pem

# Browse to: https://localhost:8444/demos/
```

### Option 2: Simple HTTP Server

```bash
# Python 3
python3 -m http.server 8000

# Browse to: http://localhost:8000/demos/
```

### Option 3: Open Locally

Simply open `demos/index.html` in your browser (some features may be limited without a server).

## Structure

```
webslides-vanilla/
├── demos/              # 11 corrected demo HTML files
│   ├── index.html      # Demo index / landing page
│   ├── components.html # Component documentation
│   ├── classes.html    # CSS classes reference
│   ├── media.html      # Media examples
│   └── ...             # Other demos (keynote, landings, portfolios, etc.)
├── static/
│   ├── css/            # webslides.css, svg-icons.css
│   ├── js/             # webslides.js, svg-icons.js
│   ├── images/         # Favicons, logos, demo images
│   └── webfonts/       # Roboto, Maitree, Cousine, San Francisco
├── LICENSE             # MIT License
└── README.md           # This file
```

## Usage

### Creating a New Presentation

1. Copy `demos/index.html` as your starting point
2. Customize the content in each `<section>` (each section is a slide)
3. Add classes for styling (see `demos/classes.html` for reference)
4. Use components from `demos/components.html`

### Basic Slide Structure

```html
<article id="webslides">
  <section>
    <div class="wrap">
      <h1>Slide Title</h1>
      <p>Slide content here</p>
    </div>
  </section>
  <section>
    <!-- Next slide -->
  </section>
</article>
```

### Enable Auto-Slide

```javascript
// Auto-advance every 10 seconds
window.ws = new WebSlides({ autoslide: 10000 });
```

## Demos

| Demo | Description |
|------|-------------|
| [index.html](demos/index.html) | Demo index with gallery |
| [components.html](demos/components.html) | 40+ reusable components |
| [classes.html](demos/classes.html) | CSS classes reference |
| [media.html](demos/media.html) | Images, video, audio examples |
| [keynote.html](demos/keynote.html) | Apple Keynote style |
| [landings.html](demos/landings.html) | Landing page examples |
| [portfolios.html](demos/portfolios.html) | Portfolio layouts |
| [why-webslides.html](demos/why-webslides.html) | Feature showcase (auto-sliding) |

## Fixes Applied

This fork includes the following corrections to the original demos:

- Added `id="webslides"` to `<article>` tags (fixes JavaScript initialization errors)
- Applied community pull request fixes from the original repository
- Updated all asset paths for local serving
- Removed Google Fonts links (replaced with local webfonts)
- Fixed internal navigation links

## Original WebSlides

- **Author:** José Luis Antúnez (@jlantunez)
- **Repository:** https://github.com/webslides/webslides
- **Website:** https://webslides.tv
- **License:** MIT

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*WebSlides Vanilla is a community-maintained fork. Not affiliated with the original WebSlides project.*
