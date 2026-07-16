# Dog Rescue SA — rescue dog directory for South Africa

**Live:** https://dogrescuesa.co.za  
**Pages:** dogrescuesa.pages.dev  
**Redirect:** dogrescuenetwork.co.za → dogrescuesa.co.za  

A static, rehome-first signpost connecting South Africans with current rescue-network pathways. It does not host dogs, collect enquiries, process applications, or promise partner capacity.

## What this is

A **signpost directory** — not a rescue, not a classifieds site, not a marketplace. Every page routes visitors to the right partner rescue organisation.

## Partner Rescues

- [SA Yorkie Rescue](https://www.yorkierescue.co.za) — Yorkie adoption & rehoming
- [Little Doggy Rescue](https://littledoggyrescue.co.za) — Small dog rescue SA
- [French Bulldog Rescue SA](https://frenchbulldogrescue.co.za) — Frenchie rehoming
- [Maltese Rescue SA](https://www.malteserescue.co.za) — Maltese rehoming
- [Lost Dogs SA](https://lostdogs.co.za) — Lost & found dogs
- [SAYR](https://sayr.co.za) — Yorkie rehoming guidance
- [YorkieSA](https://yorkiesa.com) — Yorkie care & owner guides

## Structure

```
public/                    ← Cloudflare Pages deploy root
├── index.html             ← rehome-first homepage
├── rehome-a-dog/          ← rehoming pathways
├── find-a-rescue/         ← adoption signposts
├── breeds/                ← current breed coverage
├── private-rehoming-risks/
├── about/
├── lost/                  ← Lost Dogs SA signpost
├── robots.txt
└── sitemap.xml
```

## Build workflow

1. Write spec → review → approve (Hermes)
2. Build and verify locally on a feature branch
3. Merge or commit the approved files to `main`
4. Push `main` to GitHub for source history
5. Deploy `public/` directly to the confirmed `dogrescuesa` Cloudflare Pages project in the `Info@sayr.co.za` account
6. Verify the live custom domain; this project is not Git-connected

See `BUILD_SPEC.md` for full specification.
See `CODEX_GUARDRAILS.md` for Codex usage rules.
