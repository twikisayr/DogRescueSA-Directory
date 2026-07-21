# Dog Rescue SA Daily Growth Backlog

**Site:** https://dogrescuesa.co.za  
**Repository:** `twikisayr/DogRescueSA-Directory`  
**Last production content change:** 2026-07-16  
**Backlog owner:** Daily Dog Rescue SA audit and next action

## Operating policy

The daily job must use this file as its work queue. It may reprioritise an item only when new evidence is recorded here.

### Action limits

- Maximum per run: **one scoped issue, one commit, one production deployment**.
- A healthy no-change day is a successful outcome. Never manufacture work to force a deployment.
- Do not change the same page again within **72 hours** of a meaningful content, title, navigation, or internal-link change unless fixing breakage, an inaccurate claim, an accessibility defect, or an indexing blocker.
- Assess early discovery and crawl effects after at least **7 days**; use a **28-day** window for meaningful search-performance decisions.
- If evidence or tools are degraded, research or monitor only. Do not deploy from assumptions.
- A cross-network opportunity is a proposal by default. Do not edit several repositories in one run or create a mechanical footer/link wheel.
- Province and breed expansion remains blocked until the readiness requirements in `AUDIT_AND_NETWORK_PLAN_2026-07-16.md` are independently GREEN.

### Readiness meanings

- **GREEN:** evidence supports safe execution now.
- **YELLOW:** useful candidate, but evidence, cooldown, ownership, or operational confirmation is incomplete.
- **RED:** do not execute without explicit approval or until mandatory readiness conditions are met.
- **MONITOR:** measurement item; no production edit is implied.
- **DONE:** completed and verified.

### Selection rule

1. Handle a verified P0 failure first.
2. Otherwise select the highest-ranked GREEN item.
3. If no GREEN item exists, advance the highest-ranked YELLOW item through research only.
4. If only MONITOR items are due, measure and report.
5. If nothing is due, send a short healthy heartbeat and make no change.

## Current ranked backlog

| Rank | ID | State | Candidate | Evidence / dependency | Impact | Confidence | Effort | Risk | Earliest action |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | DRSA-007 | RED | Add the missing self-referencing canonical to `/breeds/` | Weekly crawl on 2026-07-20 verified that all seven sitemap URLs return `200` without `noindex`, but `/breeds/` alone has no canonical tag; the other six canonicals match their live URLs. The source file also lacks the tag. This is an index-signal inconsistency on a new page, but canonical changes require explicit approval. | High | High | Low | Medium | After explicit approval, add only `<link rel="canonical" href="https://dogrescuesa.co.za/breeds/">`, deploy through the confirmed direct Pages project and verify live |
| 2 | DRSA-002 | MONITOR | Confirm Google processes the seven-URL sitemap and inspect core URL coverage | Maton fallback on 2026-07-20: sitemap downloaded 2026-07-16 with 7 submitted, 0 indexed, 0 errors and 0 warnings. GSC page data showed 1 homepage impression and 0 clicks for 2026-07-12–18 versus 2 impressions and 0 clicks for 2026-07-05–11. This is only four days after resubmission and remains below the seven-day evaluation window. | High | High | Low | Low | Evaluate crawl/index trend from 2026-07-23 and meaningful performance on 2026-08-13 |
| 3 | DRSA-003 | YELLOW | Add a concise “choose the right pathway” block to `/rehome-a-dog/` | Current page is useful but can route ambiguous breeds more clearly. Partner scope must first be reverified; do not imply comprehensive national coverage or partner intake capacity. | Medium | Medium | Low | Low | After partner verification and 72-hour page cooldown |
| 4 | DRSA-004 | YELLOW | Establish a repeatable partner-scope review record | Needed before visible “last reviewed” dates, broader breed routes, or claims of current coverage. Review website/contact destination, breed scope, geography, surrender path, adoption path and disclaimers. | Medium | High | Medium | Low | Research one partner per run when no higher GREEN item exists |
| 5 | DRSA-005 | RED | Add a corrections/contact route | Destination, ownership, response expectations, privacy handling and operating process are not approved. | Medium | High | Medium | High | Explicit operational approval required |
| 6 | DRSA-006 | RED | Publish province pages | No province currently has all required distinct partner coverage, towns, logistics context and unique useful content recorded. Only three initial province pages may be considered when each independently reaches GREEN. | Medium | Low | High | High | Blocked pending full readiness evidence and approval for structural expansion |

## Completed items

| ID | Completed | Result | Verification |
|---|---|---|---|
| DRSA-000 | 2026-07-16 | Repaired `/breeds/`, corrected claims and accessibility, deployed seven-page site, updated sitemap and documented direct Cloudflare Pages workflow | All seven sitemap URLs returned 200; live homepage and breeds page scored 100 performance, 100 accessibility, 100 best practices and 100 SEO in Lighthouse; both custom domains active; GSC sitemap resubmitted with zero errors |
| DRSA-001 | 2026-07-21 | Added one contextual, tracked route from SmallDogRescue.co.za's rescue directory for visitors whose dogs are not small breeds | Commit `7907da8` is on `origin/main`; the live source page returns `200`, contains the intended non-promissory Dog Rescue SA link, has no `X-Robots-Tag: noindex`, and the tracked destination returns `200` |

## Daily action log

Append only concise durable entries when an item changes state, evidence materially changes, or production is deployed. Do not append routine healthy checks.

| Date | Item | Action | Evidence / outcome | Next measurement |
|---|---|---|---|---|
| 2026-07-16 | DRSA-000 | Completed Sprint 1 repair and deployment | Production and GSC submission verified | Check sitemap processing and URL coverage from 2026-07-23 |
| 2026-07-16 | DRSA-001 | Researched one exact contextual inbound-link opportunity; no production change | Live `/find-a-small-dog-rescue/` is an indexable small-dog directory with no Dog Rescue SA link. Exact source placement and non-promissory copy recorded; target repository is dirty with unrelated audit output. | Recheck target worktree before a future single-repository execution run |
| 2026-07-20 | DRSA-007 / DRSA-002 | Completed Monday crawl, partner-link sample, GSC fallback comparison and Lighthouse baseline; no production change | Seven sitemap URLs and eight unique partner destinations returned `200`; robots and sitemap are healthy; homepage Lighthouse scored 100 in all four categories on desktop and mobile. `/breeds/` alone lacks a canonical. GSC sitemap reports 7 submitted, 0 indexed, 0 errors and 0 warnings. | Seek approval for the single canonical fix; remeasure GSC from 2026-07-23 |
| 2026-07-21 | DRSA-001 | Verified the previously committed contextual inbound link live and marked the item complete; no Dog Rescue SA production change | SmallDogRescue.co.za commit `7907da8` is on `origin/main`; the live page and tracked Dog Rescue SA destination both return `200`, and the source page has no `X-Robots-Tag: noindex` | Measure GSC crawl/index trend from 2026-07-23 |
