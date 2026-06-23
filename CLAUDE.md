# Y2K Garage Sale

Curated rare/nostalgic Y2K tech deals — Game Boys, iPods, Furbys, Pokemon cards, and more.

## Repository

- **GitHub:** tiobenito/y2k-garage-sale
- **Account:** personal (tiobenito)
- **Token env var:** `$GITHUB_PERSONAL_ACCESS_TOKEN_TIOBENITO`
- **Deploy:** Vercel (static site, auto-deploy on push to main)
- **Live URL:** https://y2k-garage-sale.vercel.app

## Tech Stack

- **Frontend:** Static HTML/CSS/JS (single `index.html`)
- **Database:** Supabase (PostgreSQL) — public read via anon key, RLS enabled
- **Images:** Local product photos in `images/` folder

## Key Files

| File | Purpose |
|------|---------|
| `index.html` | Entire frontend — fetches listings from Supabase, renders grid |
| `images/` | Product photos (Game Boy, iPod, Furby, etc.) |

## Supabase

- **Project ref:** wmcentdwysgbfbdfvfnb
- **Anon key:** In `index.html` (~line 1139)
- **RLS:** Public SELECT only. Writes/deletes require service key or SQL Editor.

## Notes

- This is the **deploy repo** (static site for Vercel)
- The scraper code lives separately at `~/cc/personal/pc/vibing/garage-sale/`
- Image mappings are in `SEARCH_TERM_IMAGES` and `CATEGORY_FALLBACK_IMAGES` objects in index.html
