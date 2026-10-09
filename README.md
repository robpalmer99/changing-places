# Changing Places Realty — demo site

Demonstration site for Peter Kelly's Pattaya real estate business, built from the
2026-10 discovery call. Static HTML, GitHub Pages.

- `PRODUCT.md` — who this is for, positioning, verified contact facts.
- `DESIGN.md` — palette, type, layout rules (derived from the printed business card).
- `index.html` — the whole site; no build step.
- `assets/img/` — licensed Pexels photography (free for commercial use, no
  attribution required). Placeholder listings only; swap for real inventory photos
  with owner/agent permission before anything goes properly live.

Pexels photo IDs used: 6663044 (hero), 27626186, 28054849, 2476632, 32870,
6538930, 11262197, 15334534.

## Publishing

GitHub Pages serves from `main`. Before any push someone outside will open, run:

```
~/dev/bin/pages-fresh ~/dev/projects/changing-places --stamp
```

## Still to come (from Peter)

- Real listings (area, price, description, beds/baths, photos with rights).
- LINE ID or add-friend link (QR exists on the card only).
- Facebook page URL once the page is fleshed out.
- Decision on domain pointing (changingplacesrealty.com is owned).
