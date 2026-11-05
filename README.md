# Eja Menu — Grilled Fish & Sides

> A lightning-fast, mobile-first web ordering menu for barbecue grilled fish and sides with instant WhatsApp order generation.

[![Deployed on Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?logo=vercel&logoColor=white)](https://eja-menu.vercel.app/)

---

## 🌟 Overview

**Eja Menu** is an ultra-lightweight, zero-dependency digital menu designed for fast-casual food businesses and barbecue pop-ups. Customers can seamlessly browse menu items, adjust quantities, toggle between pickup and delivery, and send pre-formatted order details straight to WhatsApp with one tap.

Live Site: **[eja-menu.vercel.app](https://eja-menu.vercel.app/)**

---

## ✨ Features

- **⚡ Lightweight:** One HTML file with built-in CSS and JavaScript, no frameworks or libraries, so it loads quickly even on slow mobile connections.
- **📱 Mobile-First & Responsive:** Large touch targets, smooth transitions, and safe-area support for modern smartphones.
- **🐟 Interactive Cart & Live Summary:**
  - Dynamic item counters (`+` / `−`) with instant price recalculations.
  - Nigerian Naira (`₦`) currency formatting with custom SVG symbols.
  - Real-time collapsible order review with a one-tap clear option.
- **🛵 Delivery & Pickup Switch:**
  - Interactive switch toggle.
  - Delivery address field (hides when pickup is chosen) with a reminder if it is left blank.
  - Pickup note shown when pickup is chosen.
  - Clear customer guidance on delivery fee policies; the order message says the fee is to be confirmed.
- **📝 Customer Details:** Optional name and a note for the grill (for example, "less pepper") are added to the WhatsApp message.
- **🚫 Sold-Out Flag:** Mark any menu item as sold out with one setting (see [Updating the Menu](#-updating-the-menu)).
- **💬 Direct WhatsApp Ordering:**
  - Auto-compiles an organized, easy-to-read order receipt directly into a pre-filled WhatsApp message URL.
  - One-tap handoff to merchant line (`0902 751 0364`).
- **🎨 Dark & Light Mode Support:** Automatic color adaptation using CSS system media queries (`prefers-color-scheme`).
- **🔗 Rich Social Sharing:** Fully configured Open Graph (OG) and Twitter card tags with dedicated `1200x630` preview artwork.

---

## 📋 Menu Items

### Grilled Fish
- **Catfish** — Smoky, with pepper sauce (`₦5,500`)
- **Tilapia** — Spiced and charcoal grilled (`₦6,000`)
- **Croaker** — Whole fish, house marinade (`₦8,000`)

### Sides
- **Sweet Potato** (`₦1,000`)
- **Roasted Plantain** (`₦1,000`)
- **Fried Plantain** (`₦1,500`)
- **French Fries** (`₦1,500`)
- **Yam Chips** (`₦2,000`)
- **Extra Pepper Sauce** (`₦500`)

---

## ✏️ Updating the Menu

Menu items and prices are listed in the `menuItems` list near the top of the script in `index.html`. To change a price, edit the number. To mark an item sold out, add `soldOut: true`:

```js
{ id: 'croaker', name: 'Croaker', description: 'Whole fish, house marinade', price: 8000, category: 'fish', soldOut: true },
```

Commit the change and the site redeploys. Remove `soldOut: true` when the item is back. If you change a price here, update the Menu Items list above too.

---

## 🛠️ Tech Stack

- **HTML5:** Semantic markup, accessibility labels (`aria-*`), and Open Graph metadata.
- **CSS3:** Custom properties (CSS variables), Flexbox, CSS Grid, media queries, and touch optimization.
- **Vanilla JavaScript (ES6+):** Lightweight reactive state management without build steps or bundlers.

---

## 🚀 Performance & Optimization

- **Zero External Dependencies:** No jQuery, React, or web fonts to download before the page shows.
- **Optimized Assets:** High-performance SVG and PNG favicons, async-decoded brand logo.
- **Edge Deployment Ready:** Drop-in deployable to any CDN or static hosting platform (Netlify, Vercel, GitHub Pages, Cloudflare Pages).

---

## 📁 Project Structure

```text
eja-menu/
├── index.html              # Main single-page application & menu
├── logo.png                # Brand logo artwork
├── favicon.ico             # Legacy browser tab icon (32x32)
├── favicon.svg             # Modern scalable vector tab icon
├── favicon-32x32.png       # Standard PNG favicon
├── apple-touch-icon.png    # iOS bookmark / home-screen touch icon (180x180)
├── eja-social-preview.png  # Social media link preview banner (1200x630)
└── README.md               # Project documentation
```

---

## 💻 Local Development

No package manager or build tool required.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/DayoSanya/eja-menu.git
   cd eja-menu
   ```

2. **Open the project:**
   - Simply double-click `index.html` to open in your browser, or
   - Use a local dev server (e.g. VS Code Live Server, or Python):
     ```bash
     python -m http.server 3000
     ```
   - Visit `http://localhost:3000` in your browser.

---

## 🚢 Deployment

The live site runs on **Vercel**. Use one host as the main site. If you also deploy elsewhere, keep the `canonical` and `og:` addresses in `index.html` pointing at the main site (currently `https://eja-menu.vercel.app/`).

### Deploy to Netlify
1. Connect your GitHub repository to [Netlify](https://www.netlify.com/).
2. Set **Publish directory** to `/` (root).
3. Leave build command empty. Deploy!

### Deploy to Vercel
1. Import your GitHub repository into [Vercel](https://vercel.com/).
2. Select **Other** as the framework preset.
3. Leave output directory empty and click **Deploy**.
