# SHOPIFY STORE BUILD — CLAUDE CODE BRIEFING

## WHO THIS IS FOR
You are helping Dominik build a Shopify store for an infrared red light therapy belt targeting chronic pain sufferers (ages 45-70, US + AU markets). The store must follow Ben Fashani's direct response ecom framework and closely mirror the structure of irries.com/products/restore (our primary competitor doing ~$25K/month from Facebook ads alone).

---

## WHAT CLAUDE CODE CAN BUILD

Claude Code can generate all the **code files** (Liquid templates, CSS, JavaScript, JSON configs, HTML pages) that Dominik then pastes into Shopify's theme editor or deploys via Shopify CLI. Claude Code **cannot** directly access Shopify admin, upload images, install apps, or configure payment/shipping.

### The workflow:
1. Claude Code generates code → saves to files
2. Dominik copies into Shopify theme editor (Online Store → Themes → Edit Code)
3. Dominik uploads images manually
4. Dominik installs apps manually

---

## THEME: Dawn (free)

Ben's framework says: "Dawn (free) or Sense. Clean, fast, mobile-first. Speed = conversions. Fancy themes slow load times."

Use Dawn as the base. All customization happens through **custom sections** added to Dawn's existing structure.

---

## PRODUCT PAGE ARCHITECTURE

This is the #1 priority. Ben: "This is where 80% of purchases happen. Optimize here first."

The product page must follow the **90/10 Rule**: 90% functional product (what it DOES — the transformation), 10% physical product (what it IS — specs). Lead with dreams, support with features.

### Scroll sequence (modeled after irries.com):

**ABOVE THE FOLD:**
1. **Announcement bar** — "LIMITED TIME: Up to 50% Off + Free Gift" (trust + urgency)
2. **Trust strip** — 3 icons: Free Worldwide Shipping | 60-Day Money-Back Guarantee | 24/7 Support
3. **Image gallery** (left) + **Product info** (right):
   - Product title: "[Brand Name]™ Infrared Therapy Belt"
   - Star rating + review count (Judge.me widget)
   - Price: $119.99 ~~$249.99~~ (Save $130)
   - 3 benefit bullets with checkmark icons:
     - ✓ Penetrates 8mm deep — reaches muscles, joints & nerves (not just skin)
     - ✓ Clinically-proven 660nm + 850nm dual wavelength technology
     - ✓ Cheaper than a single PT session — use unlimited at home
   - Low stock urgency badge (optional)
   - **Add to Cart button** (large, high-contrast)
   - Trust badges below ATC: Free Shipping | 60-Day Guarantee
   - Free gift callout: "FREE [Gift Item] with your order today!"

**BELOW THE FOLD (scrolling sections — each is a custom Liquid section):**

4. **"How It Works" section** — 3-step visual
   - Step 1: Wrap it around your lower back/joint
   - Step 2: Choose your therapy mode (red light, infrared, or both)
   - Step 3: Relax for 20-30 minutes — infrared does the work

5. **"Why Everything Else Failed" section** — THE KEY DIFFERENTIATOR
   This is our UMP (Unique Mechanism Behind the Problem). irries doesn't have this. We do.
   - Visual: Depth penetration diagram
   - Heating pads: 2mm (skin only)
   - Creams/patches: 1mm (evaporates)
   - TENS units: 2-3mm (nerve distraction)
   - Our belt: 8mm (reaches the source — muscle, joint, nerve tissue)
   - Headline: "The reason nothing worked isn't that you haven't tried hard enough. It's that nothing went deep enough."

6. **"Relieving Many Forms of Pain" section** — 6 condition cards (grid)
   - Back pain → explanation + how belt helps
   - Sciatica → explanation + how belt helps
   - Arthritis/joint pain → explanation + how belt helps
   - Muscle strains → explanation + how belt helps
   - Post-surgery recovery → explanation + how belt helps
   - Stiffness & limited mobility → explanation + how belt helps

7. **"The Science" section** — mechanism explanation
   - 660nm red light: cellular repair, collagen production
   - 850nm near-infrared: deep tissue penetration, inflammation reduction
   - Combined effect: ATP production increases → cells heal faster → pain decreases
   - "Used in 4,000+ PT clinics for 30+ years. Now available at home."
   - Optional: Clinical stat — "Pain scores reduced from 6.9 to 3.0 out of 10 (>50% reduction)"

8. **Social proof / testimonials section**
   - Headline: "Join [X]+ finding relief at home"
   - Judge.me review widget (or manual testimonial cards)
   - Mix of: pain type diversity (back, sciatica, arthritis), age diversity, specific results

9. **Stats section** — 3 large stat blocks
   - "88% reported significant pain reduction in 1-2 weeks"
   - "92% reported improved mobility and less stiffness"
   - "91% reported better sleep, mood, and quality of life"
   - Small text: "based on customer survey of [X] users"

10. **Trust commitment section** — 4 badge cards
    - 60-Day Money-Back Guarantee
    - Free Worldwide Shipping
    - Easy Returns
    - Secure Encrypted Payments

11. **FAQ accordion** — 10+ questions
    - How quickly will I feel relief?
    - Will it help with [sciatica/arthritis/herniated disc]?
    - Is it comfortable? Can I move normally?
    - Does it actually fix the problem or just mask pain?
    - I've tried everything. Will this really help?
    - Is it rechargeable?
    - What size fits me?
    - How long should I use it per session?
    - Do you ship internationally?
    - What's your return policy?

12. **Final CTA section**
    - "Try It Risk-Free for 60 Days"
    - Brief guarantee reinforcement
    - Add to Cart button (repeated)

---

## ADVERTORIAL LANDING PAGES

These are **standalone pages** (not the product page). Ads link here → reader gets warmed up → clicks through to product page.

### Page A: "$4,000 Drawer" (Nightmare Personal Story — Prompt 10A from Desire #1)
- Format: Long-form article page, blog-style layout
- No navigation distractions (hide header nav or minimize)
- Content: Already written and in Google Drive (Desire #1 → advertorials → #A)
- Structure: Story → depth revelation → product discovery → CTA to product page
- Multiple CTA buttons throughout ("See the belt that finally worked →")
- Mobile-first (90%+ of Facebook traffic is mobile)

### Page B: "Margaret Chen" (Authority Revelation — Prompt 10B from Desire #2)
- Format: Editorial/news-style article page
- Content: Already written and in Google Drive (Desire #2 → advertorials → #B)
- Structure: Expert intro → medical revelation → why treatments fail → product as solution → CTA
- Multiple CTA buttons throughout
- Authority indicators (pull quotes, bold key stats)

### Technical implementation:
- Create as **Shopify custom pages** with a custom page template
- Template should have: minimal header, wide content area, no sidebar, sticky CTA on mobile
- Use Liquid + HTML/CSS — no need for page builder apps

---

## ESSENTIAL PAGES

Claude Code should generate all copy + basic Liquid templates for:

1. **About Us** — Brand story (empathy-led, not corporate)
   - Founded by someone who saw loved ones suffer with chronic pain
   - Mission: make clinical-grade therapy accessible at home
   - Values: science-backed, affordable, no-BS
   
2. **Contact Us** — Simple form + email
   - support@[brand].com
   - Contact form
   - Expected response time

3. **Shipping Policy**
   - Standard: 5-9 business days
   - Express: 3-7 business days
   - Free shipping over $100
   - Worldwide shipping

4. **Return/Refund Policy**
   - 60-day money-back guarantee
   - Easy process: email support → get return label → refund within 5-7 business days
   
5. **Privacy Policy** — Standard Shopify-compliant

6. **Terms of Service** — Standard Shopify-compliant

7. **FAQ Page** — Extended version of product page FAQ

---

## CART & CHECKOUT OPTIMIZATION

### Cart drawer (Ajax cart):
- "Bought frequently with..." cross-sell section (like irries)
- Show complementary products (neck massager, cushion, etc.)
- Free shipping progress bar ("You're $X away from free shipping!")
- Trust badges in cart

### Checkout:
- Shopify handles this natively
- Add trust badges via checkout customization
- Ensure Meta Pixel fires on checkout events

---

## POST-PURCHASE UPSELL (Diamond Flow)

**App needed:** AfterSell or Zipify OCU (Dominik installs manually)

**Claude Code can help with:** Writing the upsell page copy and designing the flow logic.

### Flow:
1. Customer completes checkout →
2. **Offer 1 (The Anchor):** "Complete Your Recovery System" — Bundle: Belt + Neck Massager + Cushion at 40% off (~$199 value for $119). High-ticket, captures whales.
3. **If accepted →** Offer 2 (Cross-sell): Low-ticket add-on ($15-25), herbal patches or eBook
4. **If declined →** Offer 2 (Downsell): Single add-on item at steep discount ($19.99)

Copy principles for upsell pages:
- "We can only include this in your current shipment if you add it now"
- Show retail price crossed out with one-time offer price
- Include one testimonial about the upsell product
- CTA: "Add to Order — $X" (not generic "Buy Now")

---

## META PIXEL + CAPI SETUP

Claude Code can generate:
- Meta Pixel base code for theme.liquid
- Event tracking code (ViewContent, AddToCart, InitiateCheckout, Purchase)
- Server-side CAPI setup guidance

**Note:** Shopify has native Meta/Facebook channel integration. For basic pixel, Dominik should use the Shopify Facebook channel app. Claude Code helps with any custom event tracking needed.

---

## CSS / DESIGN DIRECTION

### Color palette (similar to irries — clean, medical-trust feel):
- Primary: Deep navy/dark blue (#1a1a2e or similar)
- Accent: Green for CTAs and checkmarks (#2ecc71 or similar)
- Background: Clean white (#ffffff)
- Text: Dark gray (#333333)
- Sale/urgency: Red (#e74c3c)
- Trust badges: Soft gray backgrounds

### Typography:
- Clean sans-serif (system fonts for speed, or Inter/Plus Jakarta Sans)
- Headlines: Bold, clear hierarchy
- Body: 16px minimum for readability (older demographic)

### Mobile-first:
- 90%+ of Facebook ad traffic is mobile
- All sections must look great at 375px width
- Sticky ATC button on mobile scroll
- Large tap targets (48px minimum)
- Fast load times (compress images, minimal JS)

---

## IMAGES NEEDED (Dominik sources separately)

Claude Code **cannot** create product images, but can create:
- SVG icons (checkmarks, trust badges, condition icons)
- CSS-based visual elements
- Placeholder layouts that Dominik fills with real images

### Images Dominik needs to source:
1. **Hero product photo** — belt on white/lifestyle background (from supplier Zoe)
2. **In-use lifestyle photos** — person wearing belt while cooking, with grandkids, on couch (3-5 photos)
3. **Depth penetration diagram** — showing 2mm vs 8mm comparison (can be designed in Canva)
4. **How-to-use sequence** — 3 step photos (wrap, select mode, relax)
5. **Condition icons** — simple SVGs for back pain, sciatica, etc. (Claude Code can generate these)
6. **Trust/guarantee badges** — money-back, shipping, secure payment (Claude Code can generate SVG)
7. **Before/after lifestyle** — struggling vs. active (NOT medical before/after — Meta flags those)

---

## APPS TO INSTALL (Dominik does manually)

| App | Purpose | Priority |
|-----|---------|----------|
| Judge.me | Reviews/social proof | HIGH — install before launch |
| AfterSell or Zipify OCU | Post-purchase upsells | HIGH — Diamond Flow |
| Shopify Email or Klaviyo | Email capture + flows | MEDIUM — can add week 2 |
| Meta Facebook Channel | Pixel + catalog sync | HIGH — needed for ads |
| Track123 or AfterShip | Order tracking page | LOW — nice to have |

---

## SUGGESTED CLAUDE CODE SESSION SEQUENCE

### Session 1: Product Page Foundation
- Set up Dawn theme customization
- Create custom product page template (JSON)
- Build all custom Liquid sections:
  - Announcement bar
  - Trust strip
  - Benefit bullets section
  - "How it works" 3-step section
  - "Why everything else failed" depth comparison section
  - Condition cards grid
  - Science/mechanism section
  - Stats section
  - Trust commitment badges
  - FAQ accordion
  - Final CTA section
- Custom CSS for all sections
- Mobile responsiveness

### Session 2: Advertorial Pages
- Custom page template (minimal header, wide content)
- Advertorial A: $4,000 Drawer (paste copy from Google Drive)
- Advertorial B: Margaret Chen (paste copy from Google Drive)
- Styled for mobile reading (large text, clear hierarchy, multiple CTAs)
- Sticky mobile CTA bar

### Session 3: Essential Pages + Global Elements
- About Us page (copy + template)
- Contact page
- Shipping, Returns, Privacy, Terms pages
- Footer layout
- Cart drawer with cross-sells
- Meta Pixel integration code
- SVG icons/badges

### Session 4: Post-Purchase + Polish
- Upsell page copy for AfterSell/Zipify
- Email templates (order confirmation, abandoned cart)
- Final mobile QA pass
- Performance optimization (image loading, CSS cleanup)

---

## KEY FRAMEWORK RULES TO FOLLOW

From Ben Fashani's system:
1. **Simple. Trust-First. Conversion-Focused.** Don't over-design.
2. **The store has ONE job: convert the traffic your ads send.** The AD did the selling.
3. **90/10 Rule:** 90% functional product (transformation), 10% physical product (specs)
4. **One strong, specific, measurable claim beats ten weak ones.** Don't list 12 benefits.
5. **Hero image + benefit headline + 5-8 images + benefit-driven description + reviews + trust badges**
6. **Proven offers:** Buy 2 Get 1 Free, Free Gifts, or Subscribe & Save 20%

From our research:
- **UMP (why everything failed):** Surface-level treatments only reach 1-3mm. Pain lives at 8mm+. Nothing reached it until dual-wavelength infrared.
- **UMS (the fix):** 660nm + 850nm infrared light penetrates 8mm into tissue, reaching the actual source of pain — muscle, joint, and nerve tissue — for the first time at home.
- **Price:** $119.99 (matches irries.com)
- **Guarantee:** 60-day money-back
- **Primary competitor to mirror:** irries.com/products/restore

---

## WHAT SUCCESS LOOKS LIKE

A store that:
- Loads fast on mobile (<3 seconds)
- Looks professional and trustworthy (medical/wellness feel, not cheap dropship)
- Has a product page that converts cold Facebook traffic without needing the ad's context
- Has 2 advertorial landing pages ready for the 3-path test (ad→10A→product, ad→10B→product, ad→direct product)
- Has all legal/trust pages in place
- Is ready for Meta Pixel + ads launch with $50-100/day CBO

Brand name is TBD — Dominik will decide. Use "[BRAND]" as placeholder throughout.
