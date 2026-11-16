# D2 — Pricing & packaging (round 1)

Assistant: pricing researcher. Sources opened: ~8. All numbers read live 2026-11-11 unless a Wayback date is given.

## Price table

| Product | Free tier | Entry paid | Mid | Top | Meter | Verified from |
|---|---|---|---|---|---|---|
| OpusClip | 60 credits/mo, 1080p, watermark, no editor, clips expire 3 days | Starter $15/mo (comparison table shows $12) — 150 credits/mo | Pro $29/mo, or $11.5/mo annual ($138/yr) — 3,600 credits/12mo, 2 seats | Business custom | Credits/mo (credit = upload minute; **not defined on page**) | opus.pro/pricing |
| Descript | 60 media min/mo + 100 one-time AI credits | Hobbyist $16/mo annual-billed ($24 monthly) — 10 media hrs + 400 AI credits/mo | Creator $24 ($35 monthly) — 30 hrs + 800 credits, 4K | Business $50 ($65) — 40 hrs + 1,500 credits; Enterprise custom | Media hours + AI credits (dual meter) | descript.com/pricing |
| Submagic | none (no-card trial) | Starter $12/member/mo annual ($19 monthly) — 45 credits, 2-min max video | Pro $23 ($29?) — 120 credits, 5-min max | Business $41 — 300 credits, 30-min max, 4K/60fps | Credits (= videos / "Magic Clips"); API $0.10–0.23/min | submagic.co/pricing |
| VEED | free plan exists, not priced on page | Creator $10/user/mo yearly — 6,000 credits | Pro $21/user/mo yearly — 18,000 credits, brand kits, 144 hr/yr AI voice | Enterprise custom | Per-user + AI credits | veed.io/pricing |
| Kapwing | 10 credits, watermark, 4-min export cap | Pro $16/mo — 1,000 credits, 4K, 120-min export | Business $50/mo — 4,000 credits | Enterprise/custom | Credits/mo + export-length caps | kapwing.com/pricing |
| Klap | — | Basic $14.50/mo ($174/yr) — 100 clips/mo | Pro $39.50 ($474/yr) — 300 clips | Pro+ $94.50 ($1,134/yr) — 1,000 clips | Clips/mo (outlier — no minutes) | klap.app/pricing |
| Vizard | 60 credits/mo, 720p, 3-day storage, 1 social account | Creator $29/mo list, $174/yr (~$14.50/mo) — 7,200 credits/yr | Business $39/mo, $234/yr | higher credit tiers | 1 credit = 1 minute uploaded (stated) | vizard.ai/pricing |
| CapCut Pro | free w/ watermark | locale-gated, not rendered | — | — | AI credits ("500 monthly AI credits" seen) | capcut.com/pricing |

## Packaging pattern

Credits dominate: 6 of 7 priced products (Opus, Submagic, VEED, Kapwing, Vizard, CapCut). Pure seat pricing is nearly gone — VEED is the only per-user price and still bolts credits on top. Descript is the sole dual meter (media hours + AI credits), Klap the sole output-metered product (clips). Nobody sells flat "unlimited" at entry.

What gets gated, consistently in this order: **watermark → resolution (720p → 1080p → 4K) → per-video duration cap → export-length cap → brand kit/template count → seats → API minutes**. Duration caps are the sharpest wall and under-marketed: Submagic caps 2 / 5 / 30 minutes by tier, Kapwing 4 vs 120 minutes. API is priced as a separate minute bundle (Submagic $0.23/min down to $0.10/min at volume). Credits are the universal rationing device; dollar-denominated usage pricing is not yet accepted.

## Cost of 1 hour of raw footage

- **Vizard** (only product with a stated conversion): 1 credit = 1 min upload → 60 credits. Creator $174 ÷ 7,200 = $0.024/min → **$1.45/hr**. Business $234 ÷ 12,000 = **$1.17/hr**.
- **Descript**: 1 hr = 1 media hour. Hobbyist $16 ÷ 10 = **$1.60/hr**; Creator $24 ÷ 30 = **$0.80/hr**. AI credits for clip generation are additive and unquantified → real cost higher.
- **OpusClip** (assuming 1 credit ≈ 1 upload minute, *not verified*): Starter 150 credits = 2.5 hr/mo at $15 → **$6.00/hr**; Pro 300/mo at $23 annual → **$4.60/hr**.
- **Klap**: output-metered, ~10–20 clips per podcast hour → $1.45–$2.90 of the $14.50 Basic allowance.
- **Submagic**: a 60-minute file **exceeds every tier's per-video cap** (30 min max at $41) — one hour is a Custom-plan conversation, not a $23 plan. Biggest gotcha in the category: the meter looks affordable, the duration cap blocks the actual job.
- **Clustering**: allowance-cost per raw hour is **$0.80–$6**, ~1–7% of an editor hour. Margin is not in the meter — it is in unused capacity.

## Direction (Wayback)

- **OpusClip**: snapshot 2025-06-03 (web.archive.org/web/20250603012036/https://www.opus.pro/pricing) — Starter $15 monthly; Pro $29/mo or **$14.50/mo annual, $174/yr**. Today: Starter $15; Pro $29/mo or **$11.5/mo, $138/yr, 3,600 credits/yr, unused credits roll over 2 months**. → **Headline annual price fell ~21% while credits became a fixed annual pool.** Repriced down, metered tighter.
- **Descript**: snapshot 2025-05-29 (…/20250529120751/…descript.com/pricing) — $16 / $24 / $35 / $50 / $65. Today: **identical**. → No change in 18 months.

Direction overall: **price per seat flat-to-down, metering up.** Cheaper entry, harder caps, annual credit pools instead of monthly allowances.

## Claims

| Claim | Source | Pub | Confidence | Class |
|---|---|---|---|---|
| Opus Pro $29/mo, $11.5/mo annual, $138/yr, 3,600 credits/12mo | opus.pro/pricing | live | high | pricing |
| Opus Pro was $29/mo / $14.50 annual, $174/yr in Jun 2025 | web.archive.org/web/20250603012036/… | 2025-06-03 | high | pricing |
| Opus free = 60 credits, watermark, 3-day export expiry | opus.pro/pricing | live | high | packaging |
| Descript $16/$24/$50 annual-billed + 10/30/40 media hrs + 400/800/1,500 AI credits | descript.com/pricing | live | high (annual↔monthly mapping medium) | pricing |
| Descript prices unchanged since May 2025 | web.archive.org/web/20250529120751/… | 2025-05-29 | high | pricing |
| Submagic $12/$23/$41 per member annual; 2/5/30-min per-video caps | submagic.co/pricing | live | high | packaging |
| Submagic API resold $0.10–0.23/min | submagic.co/pricing | live | high | pricing |
| Vizard "1 credit = 1 minute of video", Creator $174/yr | vizard.ai/pricing | live | high | pricing |
| Kapwing Pro $16 / 1,000 credits; 4-min vs 120-min export caps | kapwing.com/pricing | live | high | packaging |
| Klap meters clips, not minutes ($14.50/100 clips) | klap.app/pricing | live | high | packaging |
| VEED Creator $10/user, 6,000 credits; Pro $21, 18,000 credits | veed.io/pricing | live | medium (no monthly price captured) | pricing |
| Buyers punish credit burn: failed renders consumed credits, no restoration; repeat charges after cancellation | trustpilot.com/review/opus.pro?stars=1 | live | medium (self-selected 1-star) | sentiment |

## Could not verify

- CapCut Pro price (locale-gated).
- Munch, 2short.ai (2short.ai/pricing redirected to Trustpilot).
- Opus credit→minute definition (not on the page).
- VEED monthly prices and free-tier limits (toggle not exercised).
- Submagic monthly prices ($19 seen once; $29/$41 unconfirmed); credits→footage mapping unpublished.
- Descript AI-credit burn rate for clip generation.
- Wayback for Submagic / VEED / Kapwing — direction rests on two products only.

## Implication for a new entrant

Buyers are anchored at **$12–$29/mo**, allowance-cost of a raw hour at ~$1–$3, and **duration caps matter more than price**. A $19–$24 entry seat with a *measured upload-minute* allowance (not opaque credits) and no per-video duration cap is a defensible wedge; per-finished-minute pricing would be a novelty buyers are not trained on; the loudest 1-star complaints are credits vanishing on failed renders, so credit refunds on failure is a cheap trust lever.
