---
layout: page
title: Documentation
permalink: /docs/
lede: "Everything Nocturne can do, and how to set it up. Version 1.0.0."
description: "Merchant documentation for the Nocturne Shopify theme — setup, presets, the size rail, product page, sections and FAQ."
---


> **Before you edit theme code:** duplicate your theme first
> (**Online Store → Themes → … → Duplicate**) and make changes to the copy. Custom code
> changes are not covered by theme support, and they can be overwritten by a theme update.
> If you need code work done, consider hiring a
> [Shopify Partner](https://www.shopify.com/partners/directory).

---

## 1. Getting started

### Install and pick a preset

Nocturne ships three presets. All three are fully dark; they differ in color, type, corner
treatment and glow intensity.

| Preset | Character | Best for |
|---|---|---|
| **Nocturne** | Violet neon, tight uppercase type, small radii | Performance running, technical footwear |
| **Halide** | Cyan and green neon, soft rounded corners, wide page | Trail, outdoor, lifestyle |
| **Filament** | Magenta and amber, condensed caps, square corners | Limited drops, streetwear, collaborations |

Switch presets under **Theme settings → Theme styles**. Changing preset replaces your
color, type and layout settings — it does not change your content.

### First five things to set

1. **Theme settings → Brand** — upload your favicon (32 × 32px) and social sharing image
   (1200 × 630px).
2. **Header → Logo** — 400 × 100px recommended. Without one, your shop name is used as a
   wordmark.
3. **Theme settings → Product cards → Size option names** — make this match the option name
   your products actually use, or the size rail will not appear. See section 3.
4. **Shopify admin → Search and Discovery** — add filters. The collection page renders
   whatever you configure there.
5. **Navigation** — build your main menu. Nocturne supports three levels of nesting.

---

## 2. The command bar header

Nocturne's header is one bar that swaps between three states rather than opening separate
drawers.

- **Navigation.** On desktop, top-level items with children open a panel beneath the bar.
  Items with grandchildren open a wide multi-column panel automatically — you do not
  configure this, it follows your menu structure.
- **Search.** The magnifier opens a full-width search panel with live results.
- **Cart.** Opens the cart drawer, or goes to the cart page, depending on
  **Theme settings → Cart → Cart type**.

**Settings:** color scheme, layout (logo left with the menu beside it, or logo centered
with the menu below), logo, logo width, menu, and whether the header stays visible on
scroll.

The account icon is Shopify's own `<shopify-account>` component. It shows sign-in state
and is always visible on desktop and mobile.

### Top bar

Holds rotating announcements plus your country and language selectors. Add up to six
announcement blocks. Rotation pauses on hover and on keyboard focus, and is skipped
entirely for visitors who have asked their device for reduced motion.

---

## 3. The size rail

This is Nocturne's signature feature. On every product grid, each card shows the product's
sizes as a row of chips. In-stock sizes are clickable and add that exact variant to the
cart. Sold-out sizes stay visible but struck through, so customers can see the full run.

**To make it work:**

1. Your product must have an option whose name matches one of the entries in
   **Theme settings → Product cards → Size option names** (default:
   `Size, Shoe size, US size, EU size`). Add your own name to that list if you use
   something different.
2. That size option must be the **only** option that varies. If a product has both Color
   and Size with more than one value each, a size alone does not identify a variant, so
   the rail is hidden and the card links through to the product page instead. This is
   deliberate — it prevents adding the wrong colorway.

Turn the rail off for the whole store under **Theme settings → Product cards → Show size
rail**.

On desktop the rail appears on hover or keyboard focus. On touch devices, where hover does
not exist, it is always visible.

### Color swatches

Cards also show color swatches when the product has a color option matching
**Color option names**, and you have configured swatches in
**Shopify admin → Settings → Metafields / Product options**. Each swatch links to that
colorway.

---

## 4. The product page

The product page is two columns: a media stage and a buy panel, both sticky on desktop.
On mobile, the media becomes a swipeable carousel and the add to cart button docks to the
bottom of the screen once the real button scrolls out of view.

### Blocks

Everything in the buy panel is a block you can reorder, remove or add to:

| Block | Notes |
|---|---|
| Product title | Renders as the page's main heading |
| Price | Includes sale price, unit price and a tax note |
| Vendor | Optionally links to the vendor's collection |
| Description | Your product description from the admin |
| Variant picker | Colors as swatches, sizes as a chip rail, everything else as chips |
| Inventory status | In stock, low stock or out of stock |
| Quantity selector | |
| Buy buttons | Add to cart, accelerated checkout, Shop Pay Installments |
| Gift card recipient | Only appears on gift card products |
| Pickup availability | Only appears when you have local pickup enabled |
| Share | |
| Collapsible row | Shipping, materials, fit notes — add as many as you need |
| Icon with text | Short reassurance points |
| Heading, Text, Image, Button, Spacer, Group | General-purpose layout blocks |
| Custom Liquid | For app snippets or your own code |

App blocks can be placed anywhere in the panel.

### Media

The stage supports images, Shopify-hosted video, YouTube and Vimeo embeds, and 3D models.
The thumbnail rail on the left tracks whichever item is in view. Selecting a variant that
has its own image scrolls the stage to it.

### Size guide

Add a size guide two ways:

- **Variant picker → Size guide page** adds a link beside the size options.
- The **Size guide** section builds a conversion table (US, UK, EU, foot length) from row
  blocks, for use on a dedicated page.

---

## 5. Collection and search

### Filtering

Filters come from **Shopify admin → Search and Discovery**. Nocturne renders them as a
horizontal chip rail rather than a sidebar, with active filters shown as removable chips
beneath. Filtering updates the grid in place without a page reload, and the browser's Back
button returns to the previous filter set.

Filtering also works with JavaScript disabled — the filter form submits normally.

### Density toggle

Customers can switch between a comfortable grid and a compact one. The choice is
remembered in their browser. Turn it off under the collection section's settings.

### Search

Predictive search shows products, collections, pages, articles and query suggestions as
customers type. Configure what appears under **Theme settings → Search**. The search
results page groups results by type.

---

## 6. Cart

Choose **Drawer** or **Page** under **Theme settings → Cart**. Both share the same line
items, totals and checkout buttons.

Included: quantity changes that refresh the whole cart, order notes, subscription selling
plans, automatic discounts shown per line and on the order, accelerated checkout buttons,
and an empty state.

Nocturne does not include a discount code field in the cart. Discount codes belong at
checkout, and Theme Store rules do not permit cart-level discount code entry in a theme.

---

## 7. Color and type

### Color schemes

Every preset has five color schemes. Sections and blocks each pick one, which is how a
single page can move between deep black, raised surfaces and a full-bleed neon panel.

Each scheme defines twelve colors, including a background, a foreground for it, and a glow
color used by the edge-light system. Every scheme in every preset has been checked against
WCAG AA contrast.

If you change scheme colors, keep body text at 4.5:1 against its background.

### Edge light

**Theme settings → Edge light** controls Nocturne's neon:

- **Glow strength** — how intense the neon is across the whole theme. Set it to 0 for a
  flat dark theme with no glow.
- **Glow spread** — how far the glow extends.
- **Add glow on hover** — whether interactive elements light up on hover.
- **Show film grain** — a subtle texture that stops large dark areas from banding.

### Typography

Two fonts: one for headings, one for body text. Bold, italic and bold-italic variants load
automatically. Adjust size scale, letter spacing and capitalization separately for
headings.

---

## 8. Sections reference

| Section | Use |
|---|---|
| Slideshow | Full-bleed hero with up to six slides |
| Featured collection | Product grid from one collection, with size rails |
| Featured collections | Grid of collection cards |
| Featured product | One product with the full buy panel |
| Image with text | Two-column editorial row |
| Image gallery | Editorial grid with optional captions and links |
| Rich text | Centered block of copy |
| Multicolumn | Icon, heading and text columns |
| Logo list | Press mentions or stockists |
| Testimonials | Customer quotes with optional ratings |
| Blog posts | Recent articles from one blog |
| Newsletter | Email signup with optional background image |
| Map | Store location, address and hours, with a directions link |
| Collapsible content | Frequently asked questions |
| Video | Shopify-hosted video, or a YouTube or Vimeo embed that loads on click |
| Scrolling text | Neon ticker of short phrases |
| Size guide | Footwear size conversion table |
| Custom Liquid | Your own code |
| Apps | Container for app blocks |

---

## 9. Accessibility and performance

Nocturne is built to the Theme Store's accessibility bar:

- Every interactive element is keyboard operable, including multi-level menus
- Visible focus rings everywhere, with keyboard focus order matching the page order
- Touch targets are at least 24 × 24 CSS pixels
- Every image has alt text; every form input has a label
- Animation is skipped for visitors who prefer reduced motion

For performance, use images no larger than you need. Nocturne generates responsive sizes
automatically, but an 8MB source photo still costs you. 2400px on the long edge is plenty
for a full-bleed hero.

---

## 10. FAQ

**The size rail is not showing on my product cards.**
Check three things: the option name matches **Theme settings → Product cards → Size option
names**; the size option is the only one that varies on that product; and the product is
in stock. See section 3.

**My filters are not appearing.**
Filters come from Shopify's Search and Discovery app settings, not from the theme. Add
them there and they will appear.

**Can I use a light color scheme?**
Yes. Scheme 5 in every preset is a light scheme. Apply it to any section. Nocturne is
designed dark, so a fully light store will not look like the demo.

**How do I change the announcement bar text?**
Theme editor → Header group → Top bar. Each announcement is a block.

**Why is there no discount code field in the cart?**
Theme Store rules do not permit it. Discount codes are entered at checkout.

**How do I add a size guide?**
Either link a page from the variant picker block, or add the Size guide section to a page.
See section 4.

**Where do I change the colors?**
Theme settings → Colors. Each of the five schemes is edited independently.

---

## 11. Support

- **What is covered:** bugs in the theme, questions about settings and sections, and help
  understanding how a feature works. We reply within two business days.
- **What is not covered:** custom code, app integrations, and design work. We are happy to
  quote for these separately.
- **Before contacting us:** duplicate your theme if you have edited its code, and tell us
  your store URL and which preset you are using.

Contact us through the [support form]({{ "/support/" | relative_url }}).
