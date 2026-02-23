# Y2K Garage Sale

Curated marketplace for nostalgic Y2K-era tech and toys, scraped from Craigslist.

Built with vanilla HTML/CSS/JS + Supabase. Designed entirely through AI-assisted vibe coding.

**Live:** _Coming soon_

## How it works

- Python scraper finds Y2K listings across Craigslist (Game Boys, iPods, Furbys, Razr phones, etc.)
- Data stored in Supabase (PostgreSQL) with category tagging
- Frontend fetches listings via Supabase JS client (read-only, secured by RLS)
- Category images are curated product shots cycled across cards

## Tech

- **Frontend:** HTML/CSS (no framework — intentional) + Vanilla JS
- **Data:** Supabase JS SDK via CDN
- **Backend:** Python scraper (BeautifulSoup + requests)
- **Database:** Supabase (PostgreSQL + Row Level Security)
- **Deploy:** Netlify (static site, no build step)

## Design

"Pastel Punch" — soft pastels (lavender, peach, mint, butter, sky) with chunky black borders and offset shadows. Y2K aesthetic with modern UX.

- Fonts: DM Sans + Space Mono
- Responsive: mobile-first breakpoints at 700px and 1000px
- Sticky category navigation
- Product cards with hover lift effect

## Categories

| Category | What's in it |
|----------|-------------|
| Handheld Gaming | Game Boys, GBA SPs, Tamagotchis |
| Apple Classics | iPods, iMac G3s, iBooks |
| Toys & Collectibles | Furbys, Pokemon cards, Polly Pockets |
| Phones & PDAs | Razr phones, Nokia 3310s, Palm Pilots, Sidekicks |

## Setup

1. Clone this repo
2. Replace `YOUR_SUPABASE_URL` and `YOUR_SUPABASE_ANON_KEY` in `index.html`
3. Ensure your Supabase `listings` table has a `category` column and RLS enabled with public read
4. Open `index.html` in a browser or deploy to Netlify
