# Insights for Apps Landing Page

Static MVP landing page for the Insights for Apps iOS, iPadOS, and macOS app.

## Preview

Open `index.html` in a browser. There is no framework, package manager, build step, or tracking script.

## Publish Notes

- Primary CTA: `https://apps.apple.com/app/id6745999897`
- App Store listing copy: `app-store-listing.md`
- App icon asset: `assets/app-icon.png`
- Social preview image: `assets/social-preview-2026-07-09.png`
- Hero acquisition analytics screenshot: `assets/hero-acquisition-analytics.png`
- Sales analytics feature screenshot: `assets/feature-sales-analytics.png`
- Subscription analytics feature screenshot: `assets/feature-subscription-analytics.png`
- Reviews feature screenshot: `assets/feature-reviews.png`
- Social proof uses the same `https://insightsserver-s89wk.ondigitalocean.app/v1/social-proof` endpoint as the app auth screen. The page includes an embedded snapshot fallback because the live endpoint currently needs CORS headers or a same-origin proxy before browser fetches can read it from a separate static host.
- The landing page is organized around the app sidebar taxonomy: Growth & Marketing, Monetization, and Trust & Safety. Each taxonomy section uses a static real product screenshot and can be expanded in the page lightbox.
