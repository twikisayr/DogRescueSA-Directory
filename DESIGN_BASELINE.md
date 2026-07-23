# Dog Rescue SA — Professional Brand Refresh Baseline

**Captured:** 2026-07-23
**Repository:** `twikisayr/DogRescueSA-Directory`
**Production commit:** `8b7a1484d11796ab29affadc51e3a68abd45d739` (`seo: strengthen DogRescueSA semantic signals`)
**Baseline branch:** `main`
**Redesign branch:** `design/professional-brand-refresh`
**Deployment:** Direct Cloudflare Pages upload of `public/` to project `dogrescuesa`; Git push is source history only.

## Repository state

- Working tree was clean before branching.
- Existing static source: seven HTML pages under `public/` (the six requested redesign pages plus the existing `/breeds/` page), `robots.txt`, and `sitemap.xml`.
- No existing shared stylesheet, local brand assets, hero image, favicon, OG image, package/build script, or repository health-check script was present.
- The redesign will use one local shared stylesheet and preserve the static architecture.

## Live HTTP baseline

Checked against the custom domain before edits:

| URL | Status | Notes |
|---|---:|---|
| `/` | 200 | live homepage |
| `/about/` | 200 | live page |
| `/rehome-a-dog/` | 200 | live page |
| `/private-rehoming-risks/` | 200 | live page |
| `/find-a-rescue/` | 200 | live page |
| `/lost/` | 200 | live page |
| `/breeds/` | 200 | existing page retained in navigation |
| `/robots.txt` | 200 | `text/plain` |
| `/sitemap.xml` | 403 | live anomaly; not changed in this design sprint |
| `http://dogrescuesa.co.za/` | 200 final HTTPS URL | redirect behaviour needs separate production approval/fix; not changed here |
| `https://www.dogrescuesa.co.za/` | 200 | www policy needs separate production approval/fix; not changed here |

## Current metadata and schema

| Page | Title | Canonical | Meta description | JSON-LD |
|---|---|---|---|---:|
| `/` | Dog Rescue SA — Rehome a Dog Safely or Find a Rescue in South Africa | `https://dogrescuesa.co.za/` | present | 1 Organization/WebSite graph |
| `/about/` | About Dog Rescue SA — South Africa's Rescue Dog Directory | `https://dogrescuesa.co.za/about/` | present | 0 |
| `/rehome-a-dog/` | Rehome a Dog Safely in South Africa — Private, Respectful Guidance | `https://dogrescuesa.co.za/rehome-a-dog/` | present | 1 FAQPage |
| `/private-rehoming-risks/` | The Risks of Rehoming a Dog Privately in South Africa | `https://dogrescuesa.co.za/private-rehoming-risks/` | present | 0 |
| `/find-a-rescue/` | Find Trusted Dog Rescues in South Africa — Dog Rescue SA | `https://dogrescuesa.co.za/find-a-rescue/` | present | 0 |
| `/lost/` | Lost Your Dog? — Dog Rescue SA | `https://dogrescuesa.co.za/lost/` | present | 0 |
| `/breeds/` | Dog Rescue Partners by Breed in South Africa — Dog Rescue SA | **missing in source** | present | 0 |

No page had OG/Twitter metadata or favicon references at baseline.

## Partner destinations

Baseline `HEAD` checks returned HTTP 200 for:

- SA Yorkie Rescue: `https://www.yorkierescue.co.za/`
- Little Doggy Rescue: `https://littledoggyrescue.co.za/`
- French Bulldog Rescue SA: `https://frenchbulldogrescue.co.za/`
- Maltese Rescue SA: `https://www.malteserescue.co.za/`
- Lost Dogs SA: `https://lostdogs.co.za/`

The redesign preserves existing destination URLs and does not add partner claims, forms, listings, province routes, or new SEO URLs.

## Baseline scope decision

The requested six pages receive the full visual redesign. The already-published `/breeds/` page receives the same shared header, footer, typography, controls, and visual system so the existing navigation does not lead to an inconsistent legacy page. Its content, URL, metadata, canonical state, and partner destinations remain otherwise unchanged.
