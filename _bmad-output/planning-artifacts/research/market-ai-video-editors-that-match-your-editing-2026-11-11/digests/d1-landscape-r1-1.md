# D1 — Landscape & feature match (round 1)

Assistant: breadth-first researcher, D1 ownership. Sources opened: ~8. Accessed 2026-11-11.

## Feature match

Only products whose own pages were opened. ✅ yes · ◐ partial · ✗ no · ? unknown

| Product | a. Retakes/pauses | b. Learns style from refs | c. Word captions | d. Visuals on spoken words | e. Long→shorts | f. URL→video | g. Profile→style | h. Local/OSS/agent |
|---|---|---|---|---|---|---|---|---|
| OpusClip | ✅ filler+pause, also via API/MCP | ✗ brand templates only | ✅ animated | ◐ stock/AI b-roll, no real captures | ✅ core job | ✗ | ✗ | ◐ cloud + MCP server |
| Descript | ✅ Remove Retakes, filler, word gaps | ✗ Brand Studio/layout packs = brand, not edit style | ✅ | ◐ layouts/graphics | ✅ Create Clips | ✗ | ✗ | ✗ |
| Submagic | ✅ removeBadTakes, removeSilencePace | ✗ 35+ themes, presets, Brand Kit | ✅ | ◐ magicBrolls | ? short-form only | ✗ | ✗ | ◐ REST API |
| Klap | ? | ✗ | ✅ 99+ langs | ◐ b-roll in editor | ✅ | ✗ | ✗ | ◐ API + official MCP |
| Pictory | ? | ✗ | ✅ | ◐ stock | ◐ | ✅ URL/blog→video | ✗ | ✗ |
| Cutprint | ✅ retakes, fillers, pauses | ✅ measured style profile, rules w/ evidence | ✅ | ◐ "products you mention stay in" | ✅ platform versions | ✗ | ◐ paste channel link | ✗ cloud, invite-only |
| Ponder | ◐ strongest-moments first cut | ✅ "add past videos or your channel" | ✅ | ◐ graphics/VFX | ? | ✗ | ◐ channel link | ✗ "offline not yet" |
| Lua | ✅ retakes+silences, shows each word cut | ✅ "show Lua the reels you love" | ✅ EN/Tamil/Tanglish | ✅ records product's own site, per line | ◐ IG reels only | ✗ | ✗ | ✗ Mac app, waitlist |
| cutai (MIT) | ✅ silence/low-value trim | ✅ style-extract / style-learn → EDITSTYLE.md | ✅ subtitles | ✗ | ✅ highlights | ✗ | ✗ | ✅ local-first, MCP, agent mode |

## Q2 finding

**Yes — the feature the brief assumed might not exist is already shipping**, from at least six named products plus one MIT CLI. Cutprint derives style from your published videos *and* creators you admire, and publishes the actual measurements (cuts/min, shot lengths, hook length, words per caption, loudness) as plain-language rules with evidence per rule, learning most from raw+finished pairs. Ponder ("add past videos or your channel"), Lua ("show Lua the reels you love… drop reels or paste links"), Cutwords, Clypmint and PandaStudio all claim reference-video style cloning; `cutai` does `style-extract` / `style-learn` from multiple refs into a portable `EDITSTYLE.md` for free.

So "learns a style from 3–6 references" is **not a moat in Nov 2026 — it is a pre-launch land grab**: Cutprint is invite-only, Lua opens 50 creators per batch, and Cutwords/Clypmint/PandaStudio show no pricing, company or independent coverage. The feature is commoditised; *fidelity of the learned style* is unproven everywhere.

## Claims

- Learns pace/hooks/captions/B-roll/audio from own videos + admired creators; style profile as reviewable rules | https://cutprint.app/features/style-learning | Cutprint | undated | high | feature
- Invite-only, 4 paid tiers, Free includes "style learning from your references" | https://cutprint.app/ | Cutprint | ©2026 | high | traction
- Reference videos → saved reusable "style"; docs on matching pacing/captions/titles | https://ponder.ai/docs/using-ponder/reference-videos-and-briefs ; https://ponder.ai/ | Ponder | undated | high | feature
- "Learns the pace, the caption look and the b-roll" from reels/links; b-roll recorded from product's own site, "never stock" | https://www.trylua.com/ ; https://www.trylua.com/product/b-roll | Lua | undated | high | feature
- Waitlist, 50 creators/batch, $30–199/mo, Mac Apple silicon, Instagram-first | https://www.trylua.com/ | Lua | undated | high | traction
- Style cloning from a pasted link: cuts, pacing, captions, fonts, zooms, transitions, sound | https://clypmint.com/clone-video-editing-style | Clypmint | undated | low (no pricing/company/coverage found) | feature
- Upload a reference; "learns how it's edited" → readable style card | https://cutwords.com/edit-styles | Cutwords | undated | low (same) | feature
- `style-extract`, `style-learn` (multiple refs), EDITSTYLE.md, MCP server, agent mode, MIT | https://pypi.org/project/cutai/ | PyPI/CutAI | released 2026-04-02 | high (alpha, 1 maintainer) | feature
- Submagic consistency = Brand Kit + saved presets snapshotting caption theme/hook/music/effects | https://docs.submagic.co/llms-full.txt ; https://care.submagic.co/en/article/how-to-use-brand-kit-in-submagic-16031pe/ | Submagic | 2026-10-28 | high | feature
- Descript consistency = Brand Studio + layout packs, incl. AI pack from brand-guideline PDF | https://help.descript.com/branding/brand-studio ; https://help.descript.com/templates-and-presets/layouts-generate | Descript | undated | high | feature
- Descript ships Remove Retakes / filler / Edit for Clarity | https://help.descript.com/descript-terms-and-concepts | Descript | undated | high | feature
- OpusClip removes filler+pauses incl. enableRemoveFillerWords; MCP can "apply a brand template" but cannot compose a timeline | https://www.opus.pro/tools/video-editing-api ; https://www.opus.pro/blog/claude-video-editing-tutorial | Opus | undated | high | feature
- OpusClip b-roll = "royalty-free stock footage or AI-generated" | https://www.opus.pro/blog/three-hacks-to-create-engaging-shorts-faster-with-opus-clip | Opus | undated | high | feature
- URL→video: keeps "real screenshots and logo" | https://www.revid.ai/tools/website-to-video | Revid | undated | med | feature
- URL→video from blog/product page + brand kit | https://pictory.ai/url-to-video | Pictory | undated | high | feature
- Klap has official MCP server, API | https://klap.app/alternatives | Klap | undated | med (self-published) | feature

## Leads worth chasing

1. **Ponder and Cutprint** are the only two style-learners with a downloadable/paid product — test both on the same 3 reference videos and score fidelity. That is the real competitive benchmark.
2. **The bundle gap**: URL→video vendors (Pictory, Revid, Clevera, PromoHyper) don't learn style; style-learners (Cutprint, Ponder, Lua) don't do URL→product video; nobody does profile→style *plus* real-capture visuals except Lua, and Lua is Mac/Instagram-only.
3. **cutai** — MIT, local, MCP, style transfer. Watch its GitHub: if it matures it caps pricing for the whole category.

## Looked for and could not find

- **No vendor specifies "3–6" references** — Cutprint takes "your videos and creators you admire", cutai "multiple reference videos"; the 3–6 framing appears in no source.
- **No independent review, funding, user count or launch date** for Cutwords, Clypmint, PandaStudio, Cutprint — only their own pages. Several read as AI-generated SEO landers; treat as positioning, not capability.
- **No mainstream editor does reference-video style learning**: Descript, OpusClip and Submagic all resolve consistency to brand kits, layout packs, themes and saved presets.
- **No stock-b-roll product captures live pages/logos per spoken word** — Lua is the sole confirmed case; Cutroom, StoryCut, captionrich, Pireel, Sapari are stock/AI or your-own-assets.
- **Unverified this run (budget):** CapCut, VEED, Firecut, Gling, TimeBolt, Recut, Munch, 2short.ai, Riverside, Vizard.
