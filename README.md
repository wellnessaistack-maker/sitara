# Sitara — landing / vote page

Static single-page site (`index.html` + `img/`). No build step. Deployed on Vercel.

## Live test
The page lets visitors reserve/vote on one of three silk-square designs
(Peacock Night, Saffron Crocus, Champa Dusk). The design with the most
reservations on **30 September** is the one produced first.

## Two things to finish wiring
1. **Vote form** — `index.html` posts to Formspree. Replace `YOUR_FORM_ID`
   (line ~345, `action="https://formspree.io/f/YOUR_FORM_ID"`) with a real
   endpoint from https://formspree.io (free tier = 50 submissions/mo).
   Until then the vote button submits nowhere.
2. **Domain** — production domain is `sitaraatelier.com` (purchased via Vercel).
   Attach it to this project in Vercel → Settings → Domains if not already live.

## Images
The `img/` files here are **web-optimized** (≤1000px) for fast loading.
The full-resolution originals are kept offline and are what the mills need
for print — do not use these compressed versions for production sampling.
