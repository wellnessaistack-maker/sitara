# Brief for Claude Code

Paste this whole file into Claude Code as your first message, from inside an empty folder.

---

I'm launching a small silk scarf brand called **Sitara**. I have a finished single-page site and I need you to get it live and set up so we can iterate quickly.

**Current state:**
- Domain `sitaraatelier.com` is already bought and sits in my Vercel account
- I have a folder containing `index.html` and an `img/` folder with six JPEGs
- Nothing is deployed yet
- I have a GitHub account

**What I want you to do:**

1. Initialise a git repo in this folder and make the first commit.
2. Create a **private** GitHub repo called `sitara` and push to it.
3. Deploy to Vercel. Use the Vercel CLI if it's installed, otherwise install it. Deploy to production.
4. Attach the domain `sitaraatelier.com` to the project. It was purchased through Vercel so DNS should resolve automatically.
5. Connect the Vercel project to the GitHub repo so future pushes deploy automatically.
6. Confirm the live URL works and the images load.

**The page takes deposits, so payment needs wiring up.** Right now the reserve form posts to `https://formspree.io/f/YOUR_FORM_ID`, which is a placeholder and collects nothing.

The intended setup is **three Stripe Payment Links**, one per design, each for a $25 refundable deposit:
- Peacock Night, Saffron Crocus, Champa Dusk
- Stripe collects the email and the payment, so Formspree is not needed at all

Once I give you the three URLs, please:
1. Point each "Reserve this one" button at its matching Stripe link
2. Point the main reserve form's submit at the Stripe link for whichever design is selected, or replace the form with three buttons if that is simpler and more robust
3. Remove the Formspree action entirely

Until this is done, remind me that the page promises a deposit flow that does not exist.

**Notes on the code:**
- Single self-contained HTML file, no build step, no framework. Please keep it that way.
- Styles are inline in a `<style>` block using CSS custom properties at the top. Palette variables are named after the historical dyes (`--madder`, `--lapis`, `--gold`). Don't rename them.
- Fonts come from Google Fonts. Cormorant Garamond for headings, Inter for body.
- **No em dashes anywhere in copy.** This is a hard rule.
- There's Open Graph markup and JSON-LD Organization schema in the head. Keep both current if the copy changes.
- Images are AI-generated concept art at 1254px. They're fine for web, nowhere near print resolution. Don't upscale them for anything.

**Ongoing:** I'll be working on copy, design direction and marketing in a separate Claude session and bringing you changes. Assume frequent small edits to text and occasional image swaps. Optimise for fast, safe iteration rather than architecture.

---

## Context you may find useful

The brand draws on a real historical lineage: Indian printed cottons reached Marseille in the early 1600s, France banned them in 1686 to protect domestic industry, broke the printing blocks in 1689, and lifted the ban in 1759. Toile de Jouy was founded the next year. The "Provençal" print is descended from Indian cloth.

The scarf layout is *lachak toranj*, the Safavid carpet structure of a central medallion with four corner quarter-copies inside a heavy border. The canonical example is the Ardabil Carpet of 1539 at the V&A.

Product spec: 90 × 90 cm, 16 momme mulberry silk twill, hand rolled edges, $110.

Three designs: **Peacock Night** (lapis ground), **Saffron Crocus** (madder ground), **Champa Dusk** (ink ground).

**Commitments the copy makes. Do not contradict any of these, and if one changes, grep for every occurrence because most appear in three or four places:**
- First edition is fifty scarves
- $25 refundable deposit now, $70 balance on shipping, $95 founding total against $110 retail
- Reservations close 30 September 2026
- Ships by 30 November 2026, with a full refund offered if it slips more than fourteen days
- Thirty day returns after delivery, return postage paid
- Full refund if the delivered scarf is under weight or machine hemmed

**Important constraint on copy:** phulkari, kalamkari, bagru and bandhani are all GI-protected craft names in India. The site must never describe the product using those words. Referring to a tradition by name in explanatory prose is fine. Naming the product after one is not.
