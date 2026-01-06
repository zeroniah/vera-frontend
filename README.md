# VERA Frontend

Public-facing token detail pages for the VERA (Validation Ecosystem for Research Artifacts) system.

## Overview

This repository contains the production-ready frontend for VERA manuscript tokens. It serves individual research validation pages with citation generators, reproducibility package requests, and NFT holder benefits.

**Live Deployment:** https://vera-tokens.vercel.app

## Architecture

- **Pure HTML/CSS/JavaScript** - Zero build step, instant deployment
- **API Integration** - Fetches token data from backend.vitalgnosis.com
- **SEO Optimized** - Schema.org structured data, Open Graph tags, X Cards
- **Zero Cost Infrastructure** - Deployed on Vercel Hobby tier

## Usage

Each VERA token has a dedicated detail page accessible via:
```
https://vera-tokens.vercel.app/vera?token=VERA-M045-20260101
```

## Features

- **Dynamic Token Loading** - Fetches manuscript data from backend API
- **Citation Generator** - APA, BibTeX, MLA, Chicago formats with copy-to-clipboard
- **Reproducibility Requests** - Academic researchers can request full validation packages
- **Related Tokens** - Suggests additional research in the same domain
- **Ecosystem Integration** - Showcases VitalGnosis dual-pillar architecture (Health Sciences + VERA Validation)
- **Analytics Ready** - Event tracking for citations, downloads, form submissions

## Technology Stack

- **Frontend:** Vanilla JavaScript (ES6+)
- **Styling:** CSS3 with CSS Variables
- **API:** RESTful JSON (backend.vitalgnosis.com)
- **Deployment:** Vercel Edge Network
- **CDN:** Global edge caching with 1-hour TTL

## Development

This is a **public-facing production repository**. Development happens in the private `morphographs` repo, and vetted changes are published here.

### Local Preview

```bash
# Serve locally
npx serve public

# Or use any static server
python -m http.server 8000
```

Visit http://localhost:8000/vera?token=VERA-M045-20260101

## Repository Structure

```
vera-frontend/
├── public/
│   └── vera/
│       └── index.html          # Token detail page template
├── vercel.json                 # Deployment configuration
└── README.md                   # This file
```

## Related Repositories

- **Backend API:** [morphographs-backend](https://github.com/zeroniah/morphographs-backend) - Flask API serving token metadata
- **Main Site:** [VitalGnosis.com](https://vitalgnosis.com) - Health sciences + validator ecosystem

## Deployment

Automatically deployed to Vercel on push to `main` branch.

**Vercel Configuration:**
- Framework: Other
- Build Command: (none)
- Output Directory: `public`
- Node Version: (not required)

## Environment

No environment variables required. All configuration is in `vercel.json`.

## License

MIT License - See LICENSE file for details.

## Contact

**VitalGnosis Research Team**
- Website: https://vitalgnosis.com
- VERA Dashboard: https://vitalgnosis.com/vera-validators
- Backend API: https://backend.vitalgnosis.com

---

*Part of the VitalGnosis ecosystem: Synthesizing Biological Vitality with Digital Truth.*
