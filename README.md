# Lusaka Hair Studio — Storefront Demo

> **Concept demo — not a client project.** This site was built to show a
> hair retail business in Lusaka what a real storefront looks like when
> it's built for WhatsApp-first selling. It is not a live business. Every
> product, price, review, and phone number on the page is fictional.

---

## What this is

A single-page, mobile-first demo website for a fictional hair retail
business in Lusaka. It sells wigs, human hair bundles, closures, and
frontals. The business currently sells only through Instagram DMs and
WhatsApp. This demo shows what a real storefront would look like — and
specifically, what it looks like when the entire buying flow is designed
around WhatsApp instead of a shopping cart.

| | |
|---|---|
| **Fictional client** | Lusaka Hair Studio |
| **Niche** | Hair retail — wigs, bundles, closures, frontals |
| **Primary outcome sold** | WhatsApp orders and enquiries |
| **Design system** | Claude DESIGN.md (from `VoltAgent/awesome-design-md`) |
| **Stack** | Single HTML file, embedded CSS + JS, Inter fallback, no build step |
| **Hosting** | Free tier (Vercel / Netlify) |
| **Status** | Concept demo — placeholder content throughout |

---

## Why this demo exists

A hair customer on Instagram has four questions before they send a DM:

1. **Is this real human hair, or a synthetic blend?**
2. **What does it cost?** (Not "DM for price.")
3. **What length and origin is it?**
4. **How do I actually order and pay?**

Most hair sellers on Instagram answer none of these questions on their
profile. The price is hidden behind a DM. The origin is a hashtag. The
ordering flow is "send us a message and we'll figure it out." The demo
answers all four on the page, then hands the visitor a WhatsApp button
with the product name and price already filled in.

The sales line for this demo is:

> *"I built a concept for a hair business. Prices are on every product,
> the lengths and origins are on the card, and every WhatsApp button
> comes pre-filled with what the customer wants. Want me to build the
> real one with your products?"*

It replaces "do you have a portfolio?" with a live, clickable answer to
the only question a hair seller will have: *"will this actually get me
more orders?"*

---

## Key features

### 1. Prices on every product card
- Every product shows a **prominent ZMW price**, hair length, and
  origin (e.g., "18/20/22 inch, Brazilian").
- No "DM for price." No hidden pricing. The single biggest friction
  point in Instagram hair selling is removed.
- The visitor who can't afford the price self-selects out, and the one
  who can arrives already warm.

### 2. WhatsApp-first ordering
- Every product card has an **"Order on WhatsApp"** button.
- The button opens WhatsApp with a **pre-filled message** containing the
  product name and price, so the seller knows exactly what the customer
  wants before they reply.
- A **sticky bottom bar on mobile** keeps the WhatsApp button
  thumb-reachable at all times.
- No shopping cart. No online payment. The transaction happens where it
  already happens — in WhatsApp — and the demo just makes the path to
  it frictionless.

### 3. Trust strip (not fake star ratings)
- Three short proof points below the hero: **"100% human hair"**,
  **"Same-day Lusaka delivery"**, **"4.8★ from 300+ orders"**.
- Small text, no icons, no badges. The aggregate rating does the job;
  individual testimonials don't need stars.
- Testimonials are named with **neighbourhoods** (e.g., "— Chanda M.,
  Kabulonga"), because specific locations build more trust than
  "Happy Customer, Lusaka."

### 4. Clear "How ordering works" section
- Three numbered steps in plain prose:
  1. Browse and pick.
  2. Message us on WhatsApp with the product name.
  3. Pay on delivery in Lusaka, or pay upfront for courier.
- No icons, no illustrations. The steps are the trust signal — the
  customer can see exactly what happens next.

### 5. Enquiry form that opens WhatsApp
- The contact section has a short form: name, phone, product interested
  in, delivery area, message.
- The submit button **opens WhatsApp with the form contents pre-filled**
  as a message. There is no dead-end email form.
- A secondary plain phone number and email are shown for customers who
  don't use WhatsApp.
- Reassurance line: "We reply within 30 minutes during business hours
  (08:00–20:00 CAT)."

### 6. Mobile-first, fast
- The page is **built for a phone first**. The demo loads in under two
  seconds on a 3G connection (no heavy images, no external scripts
  beyond fonts).
- Page weight under 500KB excluding product images.
- The full flow is tested on a phone: browse → tap product → tap
  WhatsApp → message pre-filled.

---

## Design decisions

The page is built on the **Claude DESIGN.md** system. Why Claude:

| Requirement | Why Claude fits |
|---|---|
| Customer is buying sight-unseen | Warmth (cream canvas, coral accent) counteracts hesitation |
| Product photography should feel premium | Editorial layout makes product images the hero, not decoration |
| WhatsApp CTAs must stand out | Coral accent is distinct without being jarring |
| Mobile reading must be comfortable | Editorial typography tuned for long-form reading on small screens |
| Business is a small Lusaka seller | Warmth reads as "real business," not "fintech startup" |

**Constraints carried over from the design system:**

- **Canvas**: cream (`#faf9f5`), not pure white. This is the single
  biggest trust signal on the page — it reads as a small business, not
  a SaaS product.
- **Accent**: coral (`#cc785c`), used only for the primary CTA, price
  highlights, and the sticky WhatsApp bar. No other color appears on
  the page except text and borders.
- **Typography**: StyreneB (Inter fallback). Body at 16px weight 400.
  Headings at weight 500 — not bold. Bold reads as aggressive;
  weight 500 reads as confident.
- **Rounded corners**: 8px on buttons, 12px on product cards. Soft
  enough to feel approachable, not so soft it looks like a toy.
- **No shadows** on cards. Depth comes from the cream-vs-white surface
  contrast and a hairline border.

**What was deliberately avoided:**

- Stock photos of smiling models wearing wigs (the single biggest
  "AI-generated local business site" tell, and a trust-killer — real
  sellers show the actual hair, not a stock photo)
- Star ratings on every testimonial (one aggregate line is enough)
- A "Contact Us" section that doesn't lead to WhatsApp
- Hidden prices or "DM for price"
- "Luxury" and "premium" as adjectives unless attached to a specific
  product claim
- Icons on every feature or service
- A generic "About Us" section that says nothing specific
- A shopping cart (implies online payment the seller doesn't have set up)

---

## File structure

```
/
├── index.html        # The entire demo — single file, embedded CSS + JS
└── README.md         # This file
```

No build step. No dependencies beyond the Inter font. Open
`index.html` in a browser, or deploy the folder to any static host.

The WhatsApp click-to-chat links are generated with the standard
`https://wa.me/<number>?text=<url-encoded-message>` pattern. Replace the
placeholder number in `index.html` with the real one when you hand the
demo over.

The product filter (All / Bundles / Wigs / Closures / Frontals) and the
pre-filled WhatsApp messages are handled in a single `<script>` tag at
the bottom of `index.html`.

---

## How to use this demo in a sales conversation

1. **Identify a hair retail prospect** with an active Instagram and no
   website — prices hidden, no product catalogue, ordering only via DM.
2. **Send the link** with a one-liner referencing something specific:
   *"I noticed your prices are 'DM for price' — here's a concept that
   puts them on every product card."*
3. **Say the line:** *"Prices on every card, lengths and origins visible,
   and every WhatsApp button comes pre-filled with what the customer
   wants. Want me to build this with your products?"*
4. **If they reply,** book a call and use the demo as the visual brief.

The demo is **not** sent cold to every business. It is sent to hair
sellers, and only after you've looked at their current Instagram or
website and found a specific gap the demo closes.

---

## Roadmap (next build steps)

- [ ] **Replace placeholder images** with real product photography
  (licensed or from the client). The demo currently uses image blocks
  with descriptive alt text.
- [ ] **Wire the WhatsApp links** to a real number and test the
  pre-filled messages on iOS and Android.
- [ ] **Wire the enquiry form** to a real endpoint (Formspree, Google
  Sheets via Apps Script, or a simple serverless function) with an
  auto-reply. The WhatsApp pre-fill already works; a backup email path
  is useful for customers who don't use WhatsApp.
- [ ] **Add a Google Business Profile** for the fictional business as
  a proof-of-concept, so the demo can show how the site and the
  profile work together in local search.
- [ ] **Add a "sold out" state** to product cards, with a "Notify me
  on WhatsApp" button, so the seller can mark unavailable products
  without deleting them.
- [ ] **Build a variant** for a different product niche (e.g., makeup,
  skincare) to A/B the pitch.

---

## Reusing this demo for other retail niches

The structure is deliberately generic enough to retarget:

| Element | Change for a new niche |
|---|---|
| Brand name | Swap `Lusaka Hair Studio` |
| Hero H1 | Rewrite around that niche's product and delivery promise |
| Featured products | Replace with the new niche's hero products |
| Filter categories | Change to the new niche's product types |
| Trust strip | Rewrite the three proof points for that niche |
| WhatsApp messages | Change the pre-filled text to match the new product |
| Testimonials | Rewrite with neighbourhoods and product-specific detail |

Keep the design system. Change the content. The demo is the **shell**;
the niche is the **fill**.

---

## Honesty note

This is a **concept demo**, not a real business. Every product, price,
review, phone number, and email address on the page is fictional. The
WhatsApp button in the demo opens a placeholder chat.

The footer carries the line *"Concept demo — not a client project"* so
that anyone landing on it understands what they're looking at.

If you reuse this demo for a real client, remove that line, replace
every placeholder, wire the WhatsApp links and the enquiry form to real
destinations, and test the full ordering flow on a phone before
publishing.

