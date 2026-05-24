# Insights for App Store Connect Landing Page

Static MVP landing page for the Insights for App Store Connect macOS app.

## Preview

Open `index.html` in a browser. There is no framework, package manager, build step, or tracking script.

## Publish Notes

- Primary CTA: `https://apps.apple.com/app/id6745999897`
- App Store listing copy: `app-store-listing.md`
- App icon asset: `assets/app-icon.png`
- Hero mockup asset: `assets/hero-mockup.png`
- Feature screenshot: `assets/feature-response-workflow.png`
- Metrics feature screenshot: `assets/feature-workspace-metrics.png`
- Request removal feature screenshot: `assets/feature-workspace-request-removal.png`
- Acquisition funnel screenshot: `assets/feature-acquisition-funnel.png`
- Acquisition breakdown screenshot: `assets/feature-acquisition-breakdowns.png`
- Social proof uses the same `https://insightsserver-s89wk.ondigitalocean.app/v1/social-proof` endpoint as the app auth screen. The page includes an embedded snapshot fallback because the live endpoint currently needs CORS headers or a same-origin proxy before browser fetches can read it from a separate static host.
- The feature sections use sticky screenshot areas with animated CSS spotlight crops as each text step scrolls into focus. Steps can swap screenshots via `data-image`, and each `.feature-tour` sets its own `data-default-image`. Adjust `data-spot-x`, `data-spot-y`, `data-spot-w`, and `data-spot-h` on each `.feature-step` in `index.html` if a highlight needs to move.
