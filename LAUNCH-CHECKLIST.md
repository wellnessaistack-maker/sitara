# Sitara — launch / drop checklist

The site is intentionally a **free reservation** right now. It flips to a **paid drop**
once samples are in hand and photographed. Here is everything that has to happen, in order.

## 1. Before the drop (unblocks everything)
- [ ] Send UR SILK (Caitlyn) the spec + sample-request email (90×90, 16mm, hand-rolled, 2 designs, quotes at 20 and 50)
- [ ] Approve pre-production samples:
  - [ ] Burn test a loose thread (real silk smells like burning hair, leaves fine ash)
  - [ ] Check colours against Pantone, not screen (send Pantone codes for the lapis and madder up front)
  - [ ] Measure it (true 90 × 90)
  - [ ] Inspect the hand-rolled hem and the print registration
  - [ ] Check how the design reads on the reverse
- [ ] Shoot real photos: hero (draped on a person), each design flat, 2–3 worn/lifestyle shots, one hem/corner detail
- [ ] Confirm final cost and lock production quantity (20 or 50 per design)

## 2. Swap photos into the site (fast once photos exist)
Search `PHOTO SLOT` in `index.html` — there are six markers:
- [ ] Hero image (`img/draped.jpg`) + update `og:image` and alt text
- [ ] Peacock Night (`img/peacock.jpg`)
- [ ] Saffron Crocus (`img/crocus.jpg`)
- [ ] Lookbook ×3 (`img/hanging.jpg`, `img/corner.jpg`, `img/draped.jpg`)
- [ ] Reserve image (`img/hanging.jpg`)
- [ ] Delete the now-unused `img/floral.jpg` (old third design)

## 3. Turn on payment (the drop)
- [ ] Create a Stripe account, add payout bank details
- [ ] Create a Payment Link / Checkout for the founding price ($95) with a clear "ships by November" note
- [ ] Wire the form to it (keep email capture, then a "Complete your order" button to Stripe)
- [ ] Set the drop date; turn the countdown into a "drop opens" countdown
- [ ] Decide sell-out behaviour (mark sold out at 50, or show "X of 50 left")

## Still open / decisions
- [ ] **Formspree form ID** — the form action is still `YOUR_FORM_ID`, so reservations are NOT being collected yet. Set this before driving any traffic.
- [ ] Single vs double-sided print (waiting on Caitlyn's quote)
- [ ] Numbered edition: confirm the factory can print `01/50` etc., or number by hand
- [ ] US care/composition label (fiber content, care, country of origin)
