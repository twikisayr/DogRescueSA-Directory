# Dog Rescue SA Build Specification

## Architecture

Dog Rescue SA is a static HTML guidance directory deployed from `public/` to the direct-upload Cloudflare Pages project `dogrescuesa`. The site is rehome-first, directory-second, and routes visitors to independent rescue organisations.

### Source control and deployment ownership

- GitHub repository `twikisayr/DogRescueSA-Directory` is the source-control and review system.
- Cloudflare Pages project `dogrescuesa` is the current Direct Upload production project; it is not treated as a GitHub-integrated Pages project.
- Production deployments remain controlled and manual. A Git push alone does not publish production.
- After review, a non-production Wrangler branch deployment may be used for preview testing when suitable Cloudflare Pages write authentication is available. Preview deployment must not change `dogrescuesa.co.za`.
- Do not create or migrate to a new Git-integrated Cloudflare Pages project without separate approval.

## Styling policy

- A local shared stylesheet at `/assets/css/site.css` is permitted and preferred for site-wide consistency.
- Third-party CSS, remotely hosted CSS, CSS frameworks, Bootstrap, Tailwind CDN, and UI libraries are not permitted.
- JavaScript must remain minimal and local. Ordinary navigation uses real anchor links.
- Brand and image assets are stored locally under `/assets/`.

## Content and SEO invariants

- Preserve existing URLs, titles, meta descriptions, canonicals, robots, sitemap, schema intent, partner destinations, and user journeys unless separately approved.
- Do not add province pages, breed pages, dog listings, accounts, forms, adoption processing, donation functionality, or public submissions.
- Dog Rescue SA routes; partner organisations manage their own processes, capacity, privacy, screening, fees, and decisions.
- Avoid promises of guaranteed safety, intake, placement, approval, timelines, confidentiality, or partner services.

## Required checks

- All existing pages return HTTP 200 locally and on the approved preview.
- Existing sitemap and robots contents remain unchanged in this sprint.
- No remote font, CSS, image, tracker, or icon-library requests.
- Mobile menu is keyboard accessible with visible focus, `aria-expanded`, and no horizontal overflow at 320px.
- Metadata, canonical tags, schema intent, links, image dimensions, and asset references are checked after changes.
- Production deployment requires explicit approval after preview review; this branch must not be merged or deployed during implementation.
