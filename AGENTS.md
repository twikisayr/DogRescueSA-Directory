# Codex project brief — Dog Rescue SA brand refresh

## Scope
Implement only the controlled visual redesign described by the user in the current task. Work on branch `design/professional-brand-refresh` in `/home/gareth/DogRescue-Directory-Build/site`.

## Invariants
- Dog Rescue SA remains a rehome-first, breed-agnostic guidance and routing directory, not a rescue, shelter, kennel, listings site, form owner, application processor, or adoption marketplace.
- Preserve all existing URLs, approved page copy and intent, titles, meta descriptions, canonicals, robots.txt, sitemap.xml, schema intent, partner destination URLs, and routing behaviour.
- Do not add province pages, new breed pages, listings, accounts, forms, donation paths, tracking, remote dependencies, or new claims about partner capacity, screening, privacy, fees, timelines, placement, or outcomes.
- Do not deploy, push, merge, reset, delete, purge cache, alter DNS, alter redirects, or change canonical/schema/robots/sitemap policy.
- Do not change the content meaning during this design sprint. If a copy change is visually necessary, keep it strictly shortening/formatting and report it.

## Allowed implementation
- Add `/assets/css/site.css`, local SVG brand assets, locally stored image assets, local minimal JS only if needed, and metadata asset references requested by the design brief.
- Refactor the seven existing HTML pages (the six named sprint pages plus the already-published `/breeds/` page) to use the shared visual system. Do not change page URLs.
- Add `DESIGN_BASELINE.md` and update/create `BUILD_SPEC.md` as requested.
- Add `ASSET_SOURCES.md` documenting image provenance/licence. If a suitable licensed hero cannot be verified, use a self-authored SVG illustration rather than a questionable image.

## Required verification
- Inspect source before editing.
- Keep one H1 per page, semantic headings, accessible mobile navigation, visible focus states, touch-sized controls, descriptive hero alt text, explicit image dimensions, and no 320px overflow.
- Verify local links, partner links, metadata/canonical/schema preservation, no remote requests, asset existence, and HTML validity where tooling exists.
- Leave a complete changed-file report. Do not commit or deploy; Hermes reviews and controls the next phase.
