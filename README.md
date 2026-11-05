# Eja Menu — Grilled Fish & Sides

> A lightning-fast, mobile-first web ordering menu for barbecue grilled fish and sides with instant WhatsApp order generation.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Netlify Status](https://img.shields.io/badge/Deploy-Netlify-00C7B7?logo=netlify&logoColor=white)](https://eja-menu.netlify.app/)
[![Speed](https://img.shields.io/badge/PageSpeed-100%2F100-brightgreen.svg)](#performance--optimization)

---

## 🌟 Overview

**Eja Menu** is an ultra-lightweight, zero-dependency digital menu designed for fast-casual food businesses and barbecue pop-ups. Customers can seamlessly browse menu items, adjust quantities, toggle between pickup and delivery, and send pre-formatted order details straight to WhatsApp with one tap.

Live Site: **[eja-menu.netlify.app](https://eja-menu.vercel.app/)**

---

## ✨ Features

- **⚡ Blazing Fast Performance:** Zero heavy frameworks, zero runtime libraries. The total page weight is under ~20 KB for instantaneous loads even on 3G mobile networks.
- **📱 Mobile-First & Responsive:** Clean, accessible touch targets, haptic feel, smooth transitions, and viewport-safe inset support for modern smartphones.
- **🐟 Interactive Cart & Live Summary:**
  - Dynamic item counters (`+` / `−`) with instant price recalculations.
  - Nigerian Naira (`₦`) currency formatting with custom SVG symbols.
  - Real-time collapsible order review with a one-tap clear option.
- **🛵 Delivery & Pickup Switch:**
  - Interactive switch toggle.
  - Dynamic delivery address field (auto-hides when pickup is chosen).
  - Clear customer guidance on delivery fee policies.
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

## 🛠️ Tech Stack

- **HTML5:** Semantic markup, accessibility labels (`aria-*`), and Open Graph metadata.
- **CSS3:** Custom properties (CSS variables), Flexbox, CSS Grid, media queries, and touch optimization.
- **Vanilla JavaScript (ES6+):** Lightweight reactive state management without build steps or bundlers.

---

## 🚀 Performance & Optimization

- **Zero External Dependencies:** No jQuery, React, or heavy fonts blocking the Critical Rendering Path (CRP).
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

### Deploy to Netlify
1. Connect your GitHub repository to [Netlify](https://www.netlify.com/).
2. Set **Publish directory** to `/` (root).
3. Leave build command empty. Deploy!

### Deploy to Vercel
1. Import your GitHub repository into [Vercel](https://vercel.com/).
2. Select **Other** as the framework preset.
3. Leave output directory empty and click **Deploy**.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
