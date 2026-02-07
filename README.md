# Real Estate Investment Opportunity Assessment

An agentic prompt system for comprehensive real estate market analysis.

## Table of Contents

- [System Architecture](#system-architecture)
- [Folder Structure](#folder-structure)
- [How to Use](#how-to-use)
- [Tips](#tips)
- [Investment Range](#investment-range)
- [Data Sources](#data-sources)

---

## System Architecture

```
┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ PROMPT       │  │ PROMPT       │  │ PROMPT       │  │ PROMPT       │
│ INPUT 1      │  │ INPUT 2      │  │ INPUT 3      │  │ INPUT 4      │
│ Property     │  │ Location &   │  │ Market       │  │ Financial &  │
│ Data         │  │ Macro-Econ   │  │ Dynamics     │  │ Deal         │
└──────┬───────┘  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘
       │                 │                 │                 │
       └────────────┬────┴────────┬────────┴────────┬────────┘
                    │             │                 │
                    ▼             ▼                 ▼
            ┌─────────────────────────────────────────────────────┐
            │              MASTER ASSESSMENT PROMPT               │
            │         Investment Opportunity Scoring Engine       │
            └─────────────────────────┬───────────────────────────┘
                                      │
                                      ▼
                          ┌───────────────────────┐
                          │   SCORED & RANKED     │
                          │   INVESTMENT REPORT   │
                          └───────────────────────┘
```

---

## Folder Structure

```
real-estate/
├── README.md                          # This file
├── prompts/
│   ├── 01-property-data.md            # Property-Level Data Sheet
│   ├── 02-location-macro.md           # Location & Macro-Economic Research
│   ├── 03-market-dynamics.md          # Real Estate Market Dynamics
│   ├── 04-financial-deal.md           # Financial & Deal Structure
│   └── master-assessment.md           # Master Investment Assessment Engine
```

---

## How to Use

### Phase 1: Identify Candidates
1. Browse listing portals (see [Data Sources](#data-sources) below)
2. Filter for your budget range (€100k-€300k)
3. Shortlist 3-8 properties for deep analysis

### Phase 2: Collect Data
4. For each property, fill out **[01-property-data.md](prompts/01-property-data.md)**
5. For each unique city/town, run **[02-location-macro.md](prompts/02-location-macro.md)** (reusable)
6. Run **[03-market-dynamics.md](prompts/03-market-dynamics.md)** for pricing/rental data

### Phase 3: Financial Model
7. Complete **[04-financial-deal.md](prompts/04-financial-deal.md)** for each property
   - Use data from steps 4-6 to fill calculated fields
   - Get renovation quotes if significant work needed

### Phase 4: Assess
8. Feed all 4 inputs into **[master-assessment.md](prompts/master-assessment.md)**
9. Get: Score /100 + Risk Rating + BUY/PASS verdict

### Phase 5: Decide
10. Eliminate PASS / STRONG PASS properties
11. Negotiate on BUY / STRONG BUY properties
12. Re-run after property visits or new data

---

## Tips

| Tip | Why |
|-----|-----|
| Fill as many fields as possible | More data = better scores |
| Use "unknown" rather than guessing | System accounts for gaps |
| Cross-reference agent claims | Verify with independent data |
| Visit before final decision | Photos lie |
| Get independent renovation quotes | Sellers underestimate |

---

## Investment Range

**Target Budget:** €100,000 – €300,000

---

## Data Sources

> ⚠️ **Important:**
> - These sources are **Bulgaria-specific**. If you're investing in another country, replace them with equivalent local sources.
> - **Online research is not enough.** You must physically visit properties to collect accurate data for [01-property-data.md](prompts/01-property-data.md) — condition ratings, environment assessment, and many fields cannot be reliably assessed from listings alone.

### Property Listings & Pricing

| Source | URL | Notes |
|--------|-----|-------|
| imot.bg | imot.bg | Largest Bulgarian property portal |
| imoti.net | imoti.net | Major listing aggregator |
| alo.bg | alo.bg | Classifieds with RE section |
| homes.bg | homes.bg | English-friendly portal |
| bulgarianproperties.com | bulgarianproperties.com | Targeted at foreign buyers |
| OLX.bg | olx.bg | Classifieds marketplace |
| RE/MAX Bulgaria | remax.bg | International franchise |
| Yavlena | yavlena.com | Major local agency |

### Rental Market Data

| Source | URL | Notes |
|--------|-----|-------|
| Airbnb | airbnb.com | Short-term rental rates, occupancy |
| Booking.com | booking.com | Short-term, hotel benchmarks |
| AirDNA | airdna.co | Short-term rental analytics (paid) |
| imot.bg (rent) | imot.bg | Long-term rental listings |
| Numbeo | numbeo.com | Cost of living & rent indices |

### Official / Government Data

| Source | URL | Data Available |
|--------|-----|----------------|
| NSI | nsi.bg | National Statistical Institute — population, economy, construction |
| BNB | bnb.bg | Bulgarian National Bank — interest rates, mortgage data |
| Cadastre Agency | cadastre.bg | Property registry, titles |
| Municipality websites | varies | Local tax rates, zoning, development plans |

### Economic & Market Research

| Source | URL | Notes |
|--------|-----|-------|
| Eurostat | ec.europa.eu/eurostat | EU-level comparative data |
| World Bank Data | data.worldbank.org | Global economic indicators |
| Colliers / CBRE / JLL | varies | Commercial market reports |
| Bulgarian Properties | bulgarianproperties.com | Quarterly market reports |

### Quality of Life & Location

| Source | URL | Data Available |
|--------|-----|----------------|
| Numbeo | numbeo.com | Cost of living, crime, QoL indices |
| IQAir | iqair.com | Air quality data |
| Google Maps | maps.google.com | Distance, walkability |
| TripAdvisor | tripadvisor.com | Tourism demand indicators |

### Climate & Environmental Risk

| Source | URL | Data Available |
|--------|-----|----------------|
| Bulgarian Met Service | meteo.bg | Weather data |
| EU Flood Risk Maps | efas.eu | EFAS flood mapping |
| Copernicus | copernicus.eu | Satellite/environmental monitoring |
