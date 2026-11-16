# Verification pass — corrections applied to research.md

Method: mechanical citation check (`recon_kit.py citations`, clean), then a fresh-context semantic auditor on 9 load-bearing citations, then lead re-verification of every disputed item at the primary source.

## Correction 1 — OpusClip pricing direction: claim OVERTURNED

The D2 digest claimed OpusClip "repriced down ~21%": Pro annual $174/yr (June 2025) → $138/yr (Nov 2026).

**False.** The live page shows US (TIER1) Pro at **$29/mo or $14.50/mo annual, $174/yr, 3,600 credits per 12 months**. The $11.50 / $138 pair exists only in the page's embedded geo-tier config (`TIER1: 14.5, TIER2: 11.5, TIER3: 9.5`), applied to non-US/UK/DE/AU/CA/FR/ES/SEPA IPs. The digest mixed TIER1 monthly with TIER2 annual.

The archived June 2025 page shows the same $29 / $14.50 / $174 / 3,600 credits per year. **No price change, no metering change.** Descript was already reported unchanged since May 2025.

Consequence: the "price per seat flat-to-down, metering up" conclusion is replaced by "prices and meters both stable for 18 months". A new entrant cannot win on price, and need not fear a race to the bottom.

## Correction 2 — OpusClip DOES define a credit

The digest asserted the page does not define credit→minutes, and treated the $/hr figure as an unverified assumption.

**False.** The Pro credits line carries the tooltip `1 credit = 1 minute of video processing`. Cost per raw hour is therefore computed, not assumed: $174 ÷ 3,600 min = **$2.90/hr** on annual Pro; $15 × 12 ÷ (150 × 12 min) = **$6.00/hr** on Starter.

## Correction 3 — App Store quotes: genuine, but the auditor could not see them

The semantic auditor reported that credits-on-failure, watermark-at-export and forced-reframing had no support in the OpusClip App Store page. It had read the 10 reviews the HTML renders.

Re-checked against Apple's public review RSS feed (`itunes.apple.com/us/rss/customerreviews/id=<id>/sortBy=mostRecent/json`), the quotes are **verbatim and date-matching** — e.g. VEED "Soon as I applied for the 7 day free trail I was charged $32.00" (2026-07-14), "I spent 30 min on a video ONLY TO FIND OUT AT THE END I HAVE TO PAY FOR NO WATERMARK" (2026-09-02), OpusClip "even edited text won't show up on video / Customers service is low grade AI" (2026-10-20).

Verdict: no fabrication. One paraphrase error fixed (VEED reviewer said "very important, high-profile Instagram account", not "very high-profile"). Quotes older than the feed's first page (OpusClip pre-2026-09, VEED pre-2026-04) are excluded rather than repeated unverified.

**New evidence found in this pass:** CapCut reviewers name the 10-minute per-video cap as blocking real work ("that is way too low for youtube"), which ties the pricing dimension's duration-cap observation to a documented user complaint.

## Lesson worth carrying

A rendered App Store page is not the review corpus. The RSS feed is. Any future pass on user-voice should start at the feed.
