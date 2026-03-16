# Kalpé Storefront — GitHub Pages Template

A premium Shopify-style static storefront powered by the Kalpé public feed API.

## 🚀 Deploy to GitHub Pages

1. **Fork or copy** this `storefront/` folder to a new GitHub repository
2. **Enable GitHub Pages** in Settings → Pages → Source: `main` branch, `/` (root)
3. **Update the feed URL** in `index.html`:

```js
const CONFIG = {
  feedUrl: 'https://app-YOURAPPID.base44.app/functions/getStorefrontFeed',
  storeSlug: 'kalpe-store',   // ← your store_slug from StorefrontSettings
  fallbackBrand: 'Kalpé',
  fallbackPrimary: '#0096D6',
};
```

That's it — your storefront is live and synced with Kalpé.

## 🔧 Customize for another merchant

To reuse this template for a new store, change only:
- `CONFIG.storeSlug` → the merchant's `store_slug` in StorefrontSettings
- `CONFIG.fallbackBrand` → fallback brand name (shown during loading)
- `CONFIG.fallbackPrimary` → fallback accent color (overridden by feed data)

All branding, products, pricing, stock, WhatsApp numbers, and social links
are pulled live from the Kalpé feed — no manual updates needed.

## 📡 Feed endpoint

```
POST https://[your-app].base44.app/functions/getStorefrontFeed
Body: { "store_slug": "kalpe-store" }
```

Returns:
- `store` — business name, logo, tagline, about, WhatsApp, phone, socials, colors
- `products` — name, price, images, description, category, stock, WhatsApp link
- `meta` — total counts, generation timestamp

## ✨ Features

- Premium Shopify-style design
- Hero section with dynamic background from cover image
- Featured products "Coups de cœur" section
- Full product catalog grid with filters & sort
- Product detail modal with gallery support
- Category filter pills
- WhatsApp-first CTA throughout
- Mobile-optimized (critical for African market)
- Skeleton loading states
- Offline error handling
- Floating WhatsApp button
- Animated marquee band
- Scroll fade-in animations
- Zero dependencies — pure HTML/CSS/JS