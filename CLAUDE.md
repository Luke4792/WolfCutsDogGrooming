# CLAUDE.md

Single-page site for WolfCuts Dog Grooming (Harri Pick, Norton Fitzwarren, Taunton), served at https://wolfcutsdoggrooming.com via GitHub Pages (`CNAME`). Plain HTML/CSS/JS, no build step: pushing to the default branch deploys.

- Harri is a solo groomer and the whole site is her talking to the customer: write all copy, including form/status messages, in first person ("I", "me", "Find me"). Never "we"/"us", and never refer to "Harri" in the third person.
- `index.html`: the whole site. Inline SVG icon sprite at the top of `<body>` (Lucide paths); one inline script at the bottom (mobile menu, `--nav-offset` for anchor jumps, Behold Instagram feed, contact form).
- `style.css`: all styles. Brand colours are `:root` variables sampled from the logo. Bump `?v=` on the stylesheet link when changing it, since GitHub Pages caches CSS for 10 min.
- `images/`: logo assets cut from `reference images/` (which is gitignored and must stay out of git).
- Contact form posts to FormSubmit (`formsubmit.co/ajax/wolfcutsgrooming@gmail.com`). The first submission sends an activation email to that inbox; nothing arrives until it's clicked.
- Instagram feed: set `BEHOLD_FEED_ID` in the bottom script. While it's empty the section shows a plain link to Instagram.
- Prices live only in the `#prices` table. The site is meant to need no regular updates: no gallery, the feed comes from Instagram.
- Check changes at ~390px wide. Headless Chrome clamps small window widths, so screenshot the page inside a 390px iframe instead.
