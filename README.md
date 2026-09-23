# Rpay — Frontend Mobile Wallet

**A fully responsive digital banking / mobile wallet UI, built from scratch with plain HTML5 and CSS3 — no frameworks, no JS libraries.**

Rpay is a front-end concept for an international bank and mobile wallet product. It was built as a way to learn static web development in depth: page structure, component-driven CSS, layout systems (Flexbox + Grid), theming with CSS custom properties, and responsive design — all without relying on Bootstrap, Tailwind, or any JS framework.

🔗 Repo: [github.com/kabouwa/Rpay-Frontend-Mobile-Wallet](https://github.com/kabouwa/Rpay-Frontend-Mobile-Wallet)

🌐 Website : [kabouwa.github.io/Rpay-Frontend-Mobile-Wallet](https://kabouwa.github.io/Rpay-Frontend-Mobile-Wallet)

---

## ✨ Highlights

- **100% hand-written HTML5 & CSS3** — every layout, animation and component built from first principles.
- **6 fully designed screens**, sharing one consistent design system.
- **Responsive by design** — flexible grids and media queries across every stylesheet, adapting from desktop down to mobile.
- **Custom design system** via CSS variables (`root.css`): a full color palette (primary, success, warning, danger, muted, with light/dark variants), consistent radii, shadows and gradients reused across every page.
- **Micro-interactions**: an animated logo/loading-bar entry sequence on page load, hover states, and active-nav highlighting.
- **Custom typeface** (`Rpay Sans Big`) for on-brand headings.

## 📱 Pages & Features

| Page | What it does |
|---|---|
| **Landing (`index.html`)** | Marketing homepage: hero pitch ("All your money, one smart wallet"), live-style balance preview, multi-currency support, transparent-fee explainer, and a features grid (fast transfers, linked cards, modern dashboard, 24/7 help). |
| **Auth (`Auth.html`)** | Combined sign-in / create-account screen with social login options (Google, Facebook, LinkedIn) and a full-height brand visual panel. |
| **Dashboard (`Dashboard.html`)** | Account overview: total balance, linked cards carousel, recent activity feed, quick-transfer shortcut to recent recipients, and a revenue/spending statistics panel. |
| **Wallet (`Wallet.html`)** | Multi-currency wallet management (USD / EUR / MAD), per-currency balances, linked cards with masked numbers, account ID, daily/monthly limits, and security settings. |
| **Transfer (`Transfer.html`)** | Send-money flow: recipient picker (with recent recipients), transfer details form, and contextual transfer tips. |
| **Transactions (`Transactions.html`)** | Full transaction history with filtering controls. |
| **Support (`Support.html`)** | Help center with a support ticket / conversation view. |

## 🛠️ Tech Stack

- **HTML5** — semantic markup across 7 pages
- **CSS3** — Flexbox, CSS Grid, custom properties (design tokens), keyframe animations, `backdrop-filter` glass effects, media queries
- **Font Awesome** for iconography
- A custom bundled webfont for headings
- No build tools, no JS runtime dependencies — pure static front-end

## 📂 Project Structure

```
Rpay-Frontend-Mobile-Wallet/
├── index.html              # Public landing page
├── customer/
│   ├── Auth.html            # Sign in / Sign up
│   ├── Dashboard.html        # Account overview
│   ├── Wallet.html           # Multi-currency wallet
│   ├── Transfer.html         # Send money
│   ├── Transactions.html     # Transaction history
│   └── Support.html          # Help center
└── assets/
    ├── styles/               # One stylesheet per page + shared root.css design system
    ├── fonts/                # Custom typeface
    ├── icon/                 # App/browser icons
    └── img/                  # Illustrations & imagery
```

## 🎯 What this project demonstrates

- Structuring a multi-page static site with a shared, reusable design system instead of one-off styles per page
- Building fintech-style UI patterns from scratch: masked card numbers, currency wallets, transfer flows, activity feeds
- Writing maintainable CSS at scale using variables/tokens rather than hardcoded values
- Responsive layout techniques without a CSS framework

## 🚀 Running it locally

No build step required — clone and open in a browser:

```bash
git clone https://github.com/kabouwa/Rpay-Frontend-Mobile-Wallet.git
cd Rpay-Frontend-Mobile-Wallet
open index.html   # or just double-click it / use a Live Server extension
```
