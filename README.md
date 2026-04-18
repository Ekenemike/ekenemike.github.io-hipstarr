# Hipstarr Music Research
## Global Asset Retention & Identity Density Index
### Afrobeats vs Latin Pop — A Streaming Decay Comparative Audit (2019–2024)

---

> **Status:** Preliminary Findings · Data Collection In Progress  
> **Author:** Ekene Ahuche · Lagos, Nigeria  
> **Contact:** [@ekenemike_](https://x.com/ekenemike_) · [Substack](https://ekenemike.substack.com)

---

## What This Is

This repository contains the research dashboard, cleaned dataset, and Python analysis scripts for an ongoing comparative streaming decay analysis of 26 tracks — 13 Afrobeats and 13 Latin Pop — released between 2019 and 2024.

The central question: **Does Afrobeats' global streaming growth reflect genuine mainstream market penetration, or diaspora-concentrated consumption being misread as global crossover?**

The Latin Pop sample serves as a structural comparator — a genre that achieved genuine multi-market commercial scale during the same period.

---

## Headline Finding

**Afrobeats average 6-month retention: 32.4%**  
**Latin Pop average 6-month retention: 30.6%**

The original hypothesis — that Latin Pop builds more durable catalogue assets — was wrong. Afrobeats retains better on average. The reason *why* is more important than the number itself.

---

## Methodology

### Inclusion Criteria
Tracks must have charted in a minimum of 2 markets outside their home country on Spotify's published weekly Top 200 charts. This threshold excluded a significant number of culturally prominent tracks — including Asake's entire catalogue, Kizz Daniel's Buga, and Tems' Free Mind — which is itself a finding about Afrobeats' multi-market chart penetration rate.

### Primary Metric — 6-Month Retention Formula
```
Retention % = (Streams in peak market at 6 months) ÷ (Peak weekly streams in same market) × 100
```

### Data-Lifecycle Mismatch Framework
Standard analytics fail to capture the true value of Afrobeats assets because they don't account for:

1. **Active Market Rule** — if the primary market flatlines before the 6-month mark, the calculation pivots to the next most significant active market for both numerator and denominator
2. **Primary Active Market Anchor** — for slow-burn tracks, the 6-month timer anchors to the local market peak rather than the global viral peak
3. **Cross-Platform Validation** — where Spotify data is silent, Chartmetric and TurnTable Charts are used to validate continued asset value below Top 200 threshold
4. **Remix Attribution Rule** — tracks with remix releases during lifecycle are analyzed separately; stream cannibalization is flagged where original decay is artificially distorted

### Data Sources
| Source | Usage |
|--------|-------|
| [Kworb.net](https://kworb.net) | Spotify chart history — weekly streams by market |
| [Chartmetric Professional](https://chartmetric.com) | Audience demographics, city data, editorial playlists, TikTok |
| [Spotify Charts](https://charts.spotify.com) | Supplementary weekly data for tracks without Kworb pages |

---

## Repository Structure

```
hipstarr-music-research/
│
├── index.html                          # Interactive dashboard (open in browser)
├── README.md                           # This file
│
├── data/
│   ├── master_tracker.csv              # All 26 tracks — full dataset
│   ├── hipstarr_cleaned_looker.csv     # Looker Studio-ready cleaned CSV
│   └── kworb_weekly/                   # Individual weekly stream CSVs per track
│       ├── essence_weekly.csv
│       ├── love_nwantiti_weekly.csv
│       └── ...
│
├── scripts/
│   ├── 01_decay_halflife.py            # Stream half-life calculation
│   ├── 02_decay_curves.py              # Decay rate coefficients + visualisation
│   ├── 03_identity_density_index.py    # IDI composite score calculator
│   └── requirements.txt               # Python dependencies
│
└── outputs/
    ├── decay_curves.png                # Decay curve chart — all 26 tracks
    ├── halflife_results.csv            # Half-life table
    └── idi_scores.csv                  # Identity Density Index scores
```

---

## The Afrobeats Sample — 13 Tracks

| Track | Artist | Peak Market | 6M Retention | Classification |
|-------|---------|------------|--------------|----------------|
| Calm Down Remix | Rema ft. Selena Gomez | US | 59.5% | Longevity — Remix-Stabilized |
| Soso | Omah Lay | NG | 58.8% | Longevity — Organic |
| Peru Remix | Fireboy DML ft. Ed Sheeran | GB | 55.2% | Hybrid — Remix-Stabilized |
| Last Last | Burna Boy | GB | 36.58% | High-Yield Stability |
| Essence | Wizkid ft. Tems | GB | RECURRING | Hybrid — Revival Cycle |
| Love Nwantiti | CKay | US | 32.7% | Hybrid — Delayed Virality |
| Ku Lo Sa | Oxlade | FR | 29.73% | High-Retention Virality |
| Rush | Ayra Starr | FR | 29.6% | Moderate Retention — Regional |
| It's Plenty | Burna Boy | NG | 27.92% | Moderate Retention |
| Attention | Omah Lay ft. Justin Bieber | US | 0.3% | Virality — Co-sign Collapse |
| Unavailable | Davido ft. Musa Keys | NG | 12.21% | Viral Spike |
| Soundgasm | Rema | NL | 6.7% | Virality |
| Peru Original | Fireboy DML | GB | 0% | Variant Substitution |

## The Latin Pop Sample — 13 Tracks

| Track | Artist | Peak Market | 6M Retention | Classification |
|-------|---------|------------|--------------|----------------|
| Me Porto Bonito | Bad Bunny ft. Chencho | MX | 55.6% | Longevity |
| Tití Me Preguntó | Bad Bunny | MX | 53.23% | Longevity |
| Neverita | Bad Bunny | MX | 51.75% | Unicorn |
| Provenza | Karol G | MX | 43.09% | Commercial Corridor |
| Yonaguni | Bad Bunny | MX | 37.14% | High-Yield Stability |
| Bzrp Vol 52 | Quevedo ft. Bizarrap | MX | 31.55% | Commercial Corridor |
| Moscow Mule | Bad Bunny | MX | 24.54% | Commercial Corridor |
| Bichota | Karol G | MX | 22.96% | Commercial Corridor |
| Telepatía | Kali Uchis | US | 22.89% | Commercial Corridor |
| Todo De Ti | Rauw Alejandro | MX | 22.8% | Commercial Corridor |
| TQG | Karol G ft. Shakira | MX | 20.47% | Commercial Corridor |
| Bzrp Vol 53 | Shakira ft. Bizarrap | MX | 11.19% | Viral Spike |
| El Apagón | Bad Bunny | MX | 0% | Event Asset |

---

## Key Findings

**Finding 1 — The Diaspora Ceiling**
Lagos is the #1 streaming city on 100% of Afrobeats tracks in the sample. Nigerian cities account for 47–65% of total audience per track — even on tracks peaking in GB, US, and FR. Afrobeats streams travel globally but follow a single community.

**Finding 2 — Co-sign Quality > Co-sign Scale**
Ed Sheeran (Peru Remix) → 55.2% retention. Selena Gomez (Calm Down Remix) → 59.5%. Justin Bieber (Attention) → 0.3%. The foundation beneath the co-sign matters more than the co-signing artist's size.

**Finding 3 — The Organic Premium**
Soso (58.8% retention, 8 editorial playlists) outperforms multiple tracks with 10x the institutional support. Organic slow-build tracks consistently produce more durable assets than viral-first drops.

**Finding 4 — Federation vs Empire**
Latin Pop distributes audience across 20+ Spanish-speaking economies (Federation Model). Afrobeats concentrates in one community dispersed across Western markets (Imperial Hub Model). Same diaspora mechanism — different addressable scale.

**Finding 5 — The Qualification Gap**
Only 13 of 25 carefully selected Afrobeats tracks met the multi-market chart threshold. The majority of culturally significant Afrobeats hits — Asake's catalogue, Buga, Free Mind, Bloody Samaritan — stream in the hundreds of millions without breaking Spotify's multi-market chart system. This is a structural finding about the genre's global chart penetration rate, not a data limitation.

**Finding 6 — Data-Lifecycle Mismatch**
Standard streaming analytics systematically misvalue both genres. Peak market breadth without city-level geographic analysis is a misleading catalogue valuation metric. A track charting in 16 countries may represent less genuine market development than a track charting in 6 — if the 16-country presence reflects diaspora dispersion rather than local audience development.

---

## Upcoming Analysis

- [ ] Python decay curves — stream half-life per track
- [ ] Identity Density Index scores — composite metric (city concentration + editorial + retention)
- [ ] Full 5–7 page briefing note
- [ ] Presentation at Music Marketing Conference Africa — April 30, 2026

---

## License & Attribution

This research is the original work of Ekene Ahuche / Hipstarr Music Research. Data sourced from Kworb.net, Chartmetric Professional, and Spotify Charts. Preliminary findings — not for reproduction without attribution.

© 2026 Hipstarr Music Research · Lagos, Nigeria
