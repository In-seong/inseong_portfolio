# inseong_portfolio

Personal developer portfolio — a single-file interactive site.

**Live:** https://inseong.revuplan.com

## Stack
- Single-file `index.html` (no build step)
- Three.js — interactive 3D node-network hero (WebGL)
- GSAP + ScrollTrigger — load sequence, count-ups, scroll reveals
- Vanilla JS — hash routing (detail pages), EN/KO i18n, 3D tilt cards, custom cursor
- Space Grotesk + Inter (Google Fonts)

## Structure
```
index.html      # the whole site (markup + CSS + JS + data)
img/            # project screenshots (safe / anonymized)
```

## Deploy
Static files served by nginx at `/var/www/portfolio` (→ inseong.revuplan.com).
```bash
rsync -az -e "ssh -o BatchMode=yes" ./index.html ./img root@<server>:/var/www/portfolio/
ssh <server> 'chmod -R a+rX /var/www/portfolio'
```

## Notes
- Client names are anonymized; no internal/live admin links or sensitive screenshots are included.
