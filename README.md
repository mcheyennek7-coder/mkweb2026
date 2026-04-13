# merrillkeating.com

Personal portfolio site for Merrill Keating — engineer, civic tech founder, author, and speaker.

## Stack

Pure HTML/CSS/JS — no framework, no build step. Hosted on Vercel, DNS via Cloudflare.

## Structure

```
/
├── index.html          # Homepage
├── about.html          # Full bio, work history, media, activities
├── convexus.html       # Convexus civic tech platform
├── books.html          # Nine published works
├── blog.html           # Writing index
├── speaking.html       # Speaking topics, history, request form
├── contact.html        # General contact form
├── blog/
│   ├── children-in-the-dark.html
│   ├── beyond-the-prompt.html
│   ├── sanctuary-ai.html
│   └── ai-thinking.html
├── css/
│   ├── style.css       # Global styles, nav, hero, homepage sections
│   ├── inner.css       # Shared inner page components
│   └── post.css        # Blog post reading layout
├── images/
│   └── mk-logo.png     # MK monogram (navy, #1e3a5f)
└── vercel.json         # Clean URLs, security headers
```

## Adding a Blog Post

1. Copy any existing file from `/blog/` as a template
2. Update the `<title>`, `<meta name="description">`, eyebrow tag, `<h1>`, date, and essay body
3. Add a link to it in `blog.html` under the essays list
4. Add it to the Media & Features section in `about.html`
5. Commit and push — Vercel deploys automatically

> A CMS (Netlify/Decap CMS) can be added later to make this step visual. See `#blog-cms` in issues if that's been set up.

## Contact & Speaking Forms

Forms use `data-netlify="true"` by default. To switch to Formspree:

1. Create a form at [formspree.io](https://formspree.io)
2. Replace `data-netlify="true"` with `action="https://formspree.io/f/YOUR_ID" method="POST"` on each `<form>` tag
3. Remove the hidden `<input type="hidden" name="form-name">` if present

## Deploying

Connected to Vercel via GitHub. Every push to `main` triggers a deploy. No build command needed — Vercel serves static files directly.

**Custom domain:** set in Vercel dashboard → Project → Settings → Domains. Point `merrillkeating.com` and `www.merrillkeating.com` to Vercel's nameservers or add CNAME records via Cloudflare.

## Design Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `--ink` | `#1a1a2e` | Primary text, dark backgrounds |
| `--ink-soft` | `#2e2e4a` | Footer, secondary dark |
| `--ivory` | `#faf8f4` | Page background |
| `--ivory-warm` | `#f3efe8` | Section alternates, aside panels |
| `--ivory-mid` | `#e8e2d8` | Borders, dividers |
| `--amber` | `#c8820a` | Accent, links, highlights |
| `--amber-light` | `#f5c842` | Accent on dark backgrounds |
| `--navy` | `#1e3a5f` | MK logo color |
| `--serif` | DM Serif Display | Headlines, display text |
| `--sans` | Instrument Sans | Body, UI, navigation |

## Logo

The MK monogram (`images/mk-logo.png`) should be a 64×64px or larger PNG with a navy (`#1e3a5f`) rounded square background and white MK lettering. The site displays it at 32×32px — a higher resolution source prevents blurriness on retina screens.

## License

Site design and code: private. Content © 2018–2026 Merrill Keating. All rights reserved.
