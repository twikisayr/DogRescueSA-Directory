# Dog Rescue SA Audit and Rescue-Network Plan

**Audit date:** 2026-07-16  
**Site:** https://dogrescuesa.co.za  
**Repository:** `twikisayr/DogRescueSA-Directory`

## Strategic decision

Dog Rescue SA should remain the network's **breed-agnostic, rehome-first discovery and routing layer**.

It is not:

- a rescue, shelter, or kennel;
- a dog-listings or classifieds platform;
- an application or surrender-form owner;
- a substitute for partner rescue policies, capacity, or decisions;
- a deep-content site competing with specialist network properties.

Its job is to catch broad South African intent, explain the safest next step briefly, and route the visitor to the specialist property that owns the real guidance or action.

## Network fit

| User intent | Dog Rescue SA role | Destination owner |
|---|---|---|
| Rehome a Yorkie | Broad signpost | SAYR guidance, then Yorkie Rescue action/forms |
| Adopt a Yorkie | Broad signpost | Yorkie Rescue listings/application pathway |
| Rehome or adopt a small dog | Broad signpost | Little Doggy Rescue |
| Small-breed education and rescue comparison | Do not duplicate | SmallDogRescue.co.za guidance/referral hub |
| Rehome or adopt a French Bulldog | Broad signpost | French Bulldog Rescue SA |
| Rehome or adopt a Maltese | Broad signpost | Maltese Rescue SA |
| Lost or found dog | Immediate signpost | LostDogs.co.za |
| Yorkie care and prevention | Do not duplicate | YorkieSA.com |

### Cannibalisation boundary

- **DogRescueSA.co.za:** broad terms such as finding the right rescue pathway, rehoming a dog safely, private rehoming risk, and rescue partners by breed.
- **SmallDogRescue.co.za:** small-dog-specific education, partner profiles, verification methodology, province guidance, and rescue-finder depth.
- **Specialist rescue sites:** breed-specific guidance, current dogs, forms, policies, and operational action.

Dog Rescue SA should use short, useful summaries and contextual links. It should not publish deep breed guides already owned by specialist sites.

## Audit evidence

### Technical and crawl

- HTTPS pages return `200` with no `X-Robots-Tag: noindex`.
- `robots.txt` allows crawling and declares the sitemap.
- Homepage is submitted and indexed in GSC.
- Four subpages were discovered but not indexed at audit time.
- `/rehome-a-dog/` was unknown to Google at audit time.
- GSC latest 28-day window: 2 impressions, 0 clicks; the site is effectively pre-visibility.
- Live mobile Lighthouse before repair: performance 97, accessibility 92, best practices 100, SEO 100.
- Main accessibility defects were low copyright contrast and missing `<main>` landmarks.

### Architecture and content

- Rehome intent correctly leads the navigation and homepage.
- No forms, accounts, public listings, or owner-to-adopter contact features exist.
- `/breeds/` was a soft route defect: it served a duplicate homepage despite being in primary navigation.
- Existing partner copy overstated current dog availability, partner fees, privacy handling, and common process steps.
- The About page incorrectly said Dog Rescue SA was not affiliated with linked sites despite the shared network relationship.
- Current network coverage is limited to Yorkies, small dogs, French Bulldogs, Maltese dogs, and lost/found routing. The site must not imply complete national breed coverage yet.

### Authority and network wiring

A live sampled crawl of network homepages and direct sitemap URLs found no contextual links back to Dog Rescue SA from the sampled pages. The directory sends useful traffic outward, but currently receives little visible network support back. This is a discovery and authority weakness, not a reason to build a mechanical footer link wheel.

## Sprint 1 repair completed locally

- Replaced the soft `/breeds/` route with a distinct current-coverage page.
- Added `/breeds/` to the sitemap and refreshed genuine modification dates.
- Added one `<main>` landmark to every page.
- Corrected low-contrast copyright text and mobile menu labels.
- Softened or removed guarantees around partner capacity, fees, privacy, screening, availability, and outcomes.
- Clarified that Dog Rescue SA does not collect enquiries or pass user details to partners.
- Clarified that partner rescues control their own processes and decisions.
- Kept province pages unpublished.
- Kept existing canonicals, redirects, schema, forms, and destination URLs unchanged.

## Prioritised plan

### P0 — Publish and verify the repair

1. Deploy the tested seven-page static site.
2. Confirm every live sitemap URL returns `200` and `/breeds/` is no longer a homepage duplicate.
3. Confirm live sitemap contains seven URLs.
4. Re-run live Lighthouse and mobile rendering.
5. Check GSC after Google downloads the updated sitemap.

### P1 — Build discovery and trust without a link wheel

Add a small number of contextual inbound links where they genuinely help:

1. A broad “not sure which rescue handles your dog?” link from a relevant SmallDogRescue.co.za directory/guidance page.
2. A contextual Dog Rescue SA link from Little Doggy Rescue's broad safe-rehoming guidance where the visitor's dog may fall outside LDR's scope.
3. A contextual breed-directory link from one suitable French Bulldog or Maltese resource page—not every page or footer.
4. A Dog Rescue SA route from a LostDogs.co.za “found a dog and cannot keep it” guidance context, if operationally accurate.

Use varied, natural anchors. Do not add identical global partner matrices.

### P1 — Improve current-page usefulness

- Add a concise “how to choose the right pathway” block to `/rehome-a-dog/` after partner coverage is verified.
- Add visible “last reviewed” dates only after a repeatable partner-review process exists.
- Add a corrections/contact route only when its destination and handling process are approved.
- Verify all partner descriptions against each organisation's actual scope before expanding them.

### P2 — Research before expansion

Do not publish additional breed or province pages until readiness is GREEN.

Required evidence for a new breed route:

- active, traceable rescue organisation;
- verified website/contact destination;
- stated breed and geographic scope;
- current rehoming/adoption pathway;
- no unsupported promise of intake capacity or placement.

Required evidence for each province page:

- genuinely distinct partner coverage notes;
- four to six relevant towns/areas;
- province-specific routing or logistics context;
- at least 200 words of unique, useful local content;
- no template page where only the province name changes.

Only three province pages should be considered in the first province release, and only once each independently earns publication.

### P3 — Monitoring

- Weekly for the first month: GSC indexed pages, impressions, queries, and page coverage.
- Monthly: partner-link status and scope verification.
- Quarterly: cannibalisation review against SmallDogRescue.co.za and specialist sites.
- Expansion trigger: real query impressions or repeated user-routing gaps—not page-count targets.

## Success measures

The first useful milestones are:

- all seven core URLs discovered and crawled;
- at least five core URLs indexed;
- non-brand impressions for rehoming and rescue-pathway queries;
- measurable outbound referrals to the correct specialist sites;
- no applications, surrender enquiries, or dog listings mistakenly submitted to Dog Rescue SA;
- no thin province pages or duplicated specialist content.
