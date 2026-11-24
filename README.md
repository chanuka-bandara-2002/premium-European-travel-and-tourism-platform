# Velora &mdash; Premium European Travel &amp; Tourism Platform

An industry-level, fully responsive, modern luxury European tourism and journey planning website built with pure semantic **HTML5**, **CSS3** (CSS Grid & Flexbox), and **Vanilla JavaScript**.

Faithfully translated from the official Figma design specification, preserving the original design tokens, typography, color palette, responsive breakpoints, editorial photography, and rich interactive components.

---

## 1. Project Overview & Architecture

Velora is crafted around principles of **editorial restraint, destination-led photography, unhurried pacing, and transparent journey planning**. Designed specifically for discerning travellers from the UK, USA, and Europe seeking immersive cultural depth, scenic first-class rail connections, and handpicked boutique retreats.

### Key Metrics
- **24 Complete Pages**: Every screen and subpage specified in the Figma project.
- **Pure Vanilla Stack**: Zero framework dependencies (No React, Vue, or external frontend libraries).
- **Responsive System**: 12-column grid at 1440px desktop, 8-column grid at 768px tablet, 4-column reflow down to 320px mobile.
- **Accessibility**: Built to meet WCAG 2.2 AA standards (visible 3px `#174EA6` focus offset rings, skip links, semantic landmarks, ARIA-expanded accordions, and 44px+ touch targets).
- **Currency Engine**: Dynamic conversion across **GBP (£)**, **USD ($)**, **EUR (€)**, **CHF**, **AUD (A$)**, and **CAD (C$)** with live recalculation of all package, stay, and add-on pricing.

---

## 2. Directory Structure

```
tourism-website/
├── index.html                           # 01 Home Page
├── pages/
│   ├── about.html                       # 02 About Us & Guarantees
│   ├── destinations.html                # 03 Destinations Catalog
│   ├── destination-details.html         # 04 Destination Details (Rome & Environs)
│   ├── experiences.html                 # 05 Curated Experiences Catalog
│   ├── experience-details.html         # 06 Experience Details (Tuscan Cooking)
│   ├── tour-packages.html               # 07 Grand Tour Packages
│   ├── tour-package-details.html        # 08 Signature Tour Details (Italy by Rail)
│   ├── luxury-stays.html                # 09 Luxury Stays & Villas Catalog
│   ├── hotel-details.html               # 10 Hotel Details (Amalfi Coast Retreat)
│   ├── travel-planner.html              # 11 4-Step Interactive Personal Travel Planner
│   ├── search-results.html              # 12 Live Search & Filter Results
│   ├── booking-details.html             # 13 Itinerary Review & Add-on Calculator
│   ├── checkout.html                    # 14 Multi-Section Encrypted Checkout
│   ├── booking-confirmation.html        # 15 Booking Confirmation (Ref: VEL-270210)
│   ├── my-account.html                  # 16 Traveller Profile & Preferences
│   ├── my-bookings.html                 # 17 Active Bookings & Change/Cancel Modal
│   ├── travel-journal.html              # 18 The European Travel Journal
│   ├── journal-article.html             # 19 Editorial Essay (At the European Table)
│   ├── gallery.html                     # 20 Photography Gallery with Lightbox Modal
│   ├── contact.html                     # 21 Regional Offices & Specialist Enquiry
│   ├── faqs.html                        # 22 Categorized FAQ Accordion with Search
│   ├── privacy-policy.html              # 23 UK/EU GDPR Privacy Policy (8 Sections)
│   └── terms-conditions.html            # 24 Commercial Travel Terms (9 Sections)
├── assets/
│   ├── images/                          # High-resolution destination & retreat photography
│   │   ├── rome-colosseum.jpg
│   │   ├── matterhorn-zermatt.jpg
│   │   ├── paris-hero.jpg
│   │   ├── amalfi-retreat.jpg
│   │   ├── tuscan-cooking.jpg
│   │   ├── tuscan-vineyards.jpg
│   │   ├── norway-fjords.jpg
│   │   ├── alpine-extension.jpg
│   │   └── thumbnail.png
│   └── icons/                           # Handcrafted, accessible SVGs
│       ├── search.svg, calendar.svg, user.svg, map-pin.svg, train.svg,
│       ├── check.svg, close.svg, menu.svg, phone.svg, mail.svg,
│       └── chevron-down.svg, chevron-right.svg, star.svg, heart.svg...
├── css/
│   ├── style.css                        # Design tokens, reset, typography, header & footer
│   ├── components.css                   # Buttons, cards, accordions, modals, forms & badges
│   └── responsive.css                   # Breakpoints (1440px, 1024px, 768px, 390px, 320px)
├── js/
│   ├── main.js                          # Currency engine, toast alerts, wishlist LocalStorage
│   ├── navigation.js                    # Sticky header, mobile drawer menu, active nav state
│   └── interactions.js                  # Filter pills, live search, lightbox, wizard & validation
└── README.md
```

---

## 3. Design System & Tokens

### Color Palette
- **Deep Navy (`#142C40`)**: Actions, primary buttons, hero branding, active states.
- **Warm Limestone (`#F4F0E8`)**: Surface background, primary page canvas.
- **Muted Stone (`#D8CFC0`)**: Restrained card borders, divider lines, inputs.
- **Warm Brass (`#A88A54`)**: Decorative metallic accents, eyebrow text, gold badges.
- **Dark Ink (`#202A33`)**: High-contrast body copy and readable typography.
- **Focus Blue (`#174EA6`)**: Accessible 3px offset focus ring for keyboard navigation.
- **Pine Green (`#1E6B37`)**: Confirmation badges and success states.

### Typography Hierarchy
- **Editorial Headings**: *Playfair Display* (weights 400, 500, 600, 700 with italic variants).
- **Interface & Body UI**: *Inter* (weights 300, 400, 500, 600, 700).

### 8-Point Spacing Scale
- `var(--space-8)` (8px)
- `var(--space-12)` (12px)
- `var(--space-16)` (16px)
- `var(--space-20)` (20px)
- `var(--space-24)` (24px)
- `var(--space-32)` (32px)
- `var(--space-40)` (40px)
- `var(--space-48)` (48px)
- `var(--space-64)` (64px)
- `var(--space-80)` (80px)
- `var(--space-96)` (96px)

---

## 4. Interactive Features

1. **Currency Converter**: Switch between GBP, USD, EUR, CHF, AUD, and CAD at any time from the top navigation. All price tags across the site update dynamically via `data-price-gbp`.
2. **Interactive Travel Planner**: A 4-step wizard that captures travel interests, regions, dates, and pacing preferences, culminating in a custom itinerary summary and specialist consultation request.
3. **Live Filter & Instant Search**: Filter destinations, experiences, stays, and journal stories instantly without reloading the page.
4. **Accessible Accordions**: Keyboard-operable FAQ and day-by-day itineraries with smooth transitions and ARIA attributes (`aria-expanded`, `aria-controls`).
5. **Interactive Itinerary Calculator**: Toggle optional add-ons (Tuscan cooking masterclass +£330, VIP airport meet & greet +£90) with real-time recalculation of the journey total.
6. **Encrypted Form Validation**: Client-side validation across checkout, contact, newsletter, and change-request forms with accessible inline error summaries.
7. **Lightbox Photo Gallery**: Modal for high-resolution destination previews with keyboard escape and photo credit attribution.
8. **Client Booking Persistence**: Successful checkout saves confirmed itinerary (`VEL-270210`) into `localStorage` and updates My Bookings and Account views.

---

## 5. How to Run Locally

Because this project is built entirely with vanilla standards, no build step, compiler, or package manager is required:

1. Double-click `index.html` to open directly in any modern browser (Chrome, Safari, Edge, Firefox).
2. Or serve via any local HTTP server:
   ```bash
   # Using Python built-in server:
   python -m http.server 8000

   # Or using Node.js:
   npx serve .
   ```
3. Navigate to `http://localhost:8000`.
