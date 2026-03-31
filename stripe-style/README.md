# Document360 landing page theme (Stripe-inspired)

A **Knowledge Base landing page** layout for [Document360](https://document360.com/). Document360 lets you configure site-wide branding and **Customize site** to edit the home page, header, footer, and custom CSS/JS. This package is **one optional visual style** for that landing experience—clean, documentation-style layouts similar in spirit to Stripe’s docs—not an official Stripe product.

**Official guide:** [Customize site](https://docs.document360.com/docs/customize-site) (Document360 documentation)—covers **Site customization**, the **Customize site** builder, **Main pages** (including Home), and **Custom CSS / JavaScript**.

---

## What’s included

| Folder | Purpose |
|--------|---------|
| `Header-Section/` | Top navigation bar (HTML + CSS) |
| `Hero-Section/` | Hero area with background and utility card (split across custom blocks where noted in the HTML comments) |
| `Body-1st-fold/` | First content fold (e.g. product pillars / links) |
| `Product-Section/` | Product highlights |
| `Try-out-Section/` | Try-it / CTA style block |
| `Footer-Section/` | Footer |
| `Article-page/` | Article and overview layouts (for article-style pages, if you use them) |
| `Assets/` | Images such as logos |
| `script.js` | Optional JavaScript (subsection below) |

Each section ships as **paired `.html` and `.css`** files. Paste the CSS in **Customize site** → **Custom CSS / JavaScript** (CSS tab). Add the HTML via **Main pages** → **Home** (stacked blocks), or place header/footer fragments in **Site header & footer** if that fits your layout—Document360 supports both patterns ([Customize site](https://docs.document360.com/docs/customize-site)).

---

## How to use this in Document360

These steps follow Document360’s **Knowledge base site** settings ([Customize site](https://docs.document360.com/docs/customize-site)). Your project should use **KB site 2.0** where advanced customization applies.

### Branding and base styles (optional but recommended)

1. Go to **Settings** → **Knowledge base site** → **Site customization**.
2. Set **Site theme** (light/dark), **Branding** (logo, favicon, logo URL), **Colors**, **Fonts**, **Styling** (buttons), and **Site layout** (full width vs center) to match your brand.
3. Click **Save**.

### Custom CSS and JavaScript

1. From **Site customization**, click **Customize site**.
2. In the builder, open the section dropdown and select **Custom CSS / JavaScript** (listed under **Site header & footer** in the left panel, per Document360).
3. Paste this theme’s **CSS** (merge section `.css` files in a sensible order: global layout first, then each section). Add **JavaScript** from `script.js` only if you need that behavior, in the **JavaScript** panel.

### Home / landing page content

1. Inside **Customize site**, use the page dropdown and open **Main pages** → **Home** (or the equivalent home page builder for your project).
2. Add the HTML for each section (header → hero → body → … → footer) in the blocks or regions your builder provides. If the UI splits content across multiple blocks, follow hints in the HTML (e.g. “Use two separate custom code blocks”, “Block 1” / “Block 2”).

### Publish

- **Save** stores work in the builder; **Publish** pushes changes to the live knowledge base site. After edits, **Publish** so readers see the updated landing page.

### Assets

Replace placeholder `#` links, hero images, and logo paths with your own URLs or Document360 Drive URLs. Some samples reference external CDN URLs; use your own assets for production if you want full control.

### JavaScript (`script.js`)

Optional. The **`articleDetailsLoaded`** block compares `articleId` to **`YOUR-ARTICLE-ID-1`** and **`YOUR-ARTICLE-ID-2`** — replace those strings with your real article UUIDs from Document360 (or remove the branches you do not need). Until you do, those branches never run. The script also expects `.left-container` for the country/language row and uses **jQuery** (`$`) in places; see the comments in `script.js`.

---


## Article page files

`Article-page/` contains layouts that may include Document360 **custom block** markup (e.g. `editor360-custom-block`). Use these on **article templates** or rich-content areas where that markup is supported; for a **landing page only**, you might not need every file.

---

## Customization checklist

- [ ] Replace links (`href="#"`, support, changelog, social).
- [ ] Swap images and alt text for your brand.
- [ ] In `script.js`, replace `YOUR-ARTICLE-ID-1` and `YOUR-ARTICLE-ID-2` with your Document360 article UUIDs (or remove unused branches).
- [ ] Confirm jQuery availability if you keep `$` usage.
- [ ] Test responsive behavior in Document360 preview on mobile widths.

---

## Disclaimer

This theme is **inspired by** a modern documentation / Stripe-like aesthetic. **Stripe** and related marks are trademarks of Stripe, Inc. This project is **not** affiliated with, endorsed by, or sponsored by Stripe. Use at your own discretion and ensure your content and branding comply with applicable trademark and style guidelines.


