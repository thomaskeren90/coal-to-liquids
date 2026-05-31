# Indonesia Energy Ventures — Complete Playbook

## By Thomas / Bimo

---

# SECTION 1: SYNFUEL FROM COAL (CTL)

## What is Coal-to-Liquids?
Coal → Gasifier → Syngas (CO+H₂) → Cleanup → Fischer-Tropsch → Synthetic crude → Refined fuels

**Proven at scale:** Sasol (South Africa, since 1955), Shenhua (China).
**Why Indonesia:** 38 billion tonnes coal (4th globally), government downstream mandate, import substitution.

## The Scale Problem
| Scale | Output | Cost |
|-------|--------|------|
| Lab | 50ml/day fuel | Rp 20-40 juta |
| Pilot | 1 barrel/day | Rp 500 juta-1M |
| Small plant | 100 barrels/day | $5-10M |
| Industrial | 10,000+ barrels/day | $500M+ |

---

# SECTION 2: FISCHER-TROPSCH LAB BUILD

## The Reactor

**Vessel:** 316 stainless steel tube, 50mm OD × 500mm, Schedule 80 (30+ bar rating)
**Heater:** Ceramic band heater 500-1000W, 220V, ceramic fiber insulation
**Controller:** Arduino Nano + MAX31855 + K-type thermocouple + MOSFET → your PCB
**Gas:** CO cylinder + H2 cylinder + mass flow controllers + check valves
**Condenser:** Copper coil in chilled water bath
**Catalyst:** Iron-based (Fe/Cu/K on silica support)

## The Process
1. Fill vessel with 20-50g catalyst
2. Purge with N2, heat to 400°C under H2 (reduce catalyst, 4hrs)
3. Cool to 220-250°C, switch to syngas (H2:CO = 2:1)
4. Pressurize to 10-20 bar, hold temp ±1°C
5. Collect liquid fuel from condenser daily
6. Expected: 20-50ml diesel-range liquid/day

## Scaling Path
Small tube → bigger tube → more catalyst → more output.
1kg catalyst → 10L/day fuel.

---

# SECTION 3: PYROLYSIS — THE CASHELOW BUSINESS

## What Pyrolysis Makes (from coal or biomass)
| Output | Use | Selling Price |
|--------|-----|--------------|
| Charcoal (coke) | BBQ, water filtration, metallurgy | Rp 5-15K/kg |
| Tar/oil | Industrial fuel | Rp 3-8K/kg |
| Syngas | Fuel for the reactor itself | Free |
| Activated carbon | Water filters, gold mining | Rp 15-50K/kg |

## Simple Drum Retort (Rp 5-10 juta)
**Build:** 200L drum (outer) + 100L drum (inner) + chimney + burner
**How it works:** Fire the outer drum → inner drum heats coal WITHOUT oxygen → gases burn back → self-sustaining after 200°C
**Per batch:** 15-25kg charcoal, 10-15L oil, free fuel for next batch
**Time:** 4-6 hours per batch

## Activated Carbon (90% margin)
Charcoal → grind to 4-8 mesh → steam treat at 800-900°C for 2hrs → activated carbon
Cost: ~Rp 1,000/kg production → selling price: Rp 15,000-50,000/kg

## Palm Kernel Shell Path
Buy waste PKS from mills → pyrolyze → activate → sell as activated carbon
PKS cost: Rp 200-500/kg (sometimes free, mills pay to dispose)
Activated carbon: Rp 15,000-50,000/kg

---

# SECTION 4: CHINA'S "TEAPOT REFINERIES"

## What They Are
Small, family-owned crude distillation units in Shandong province, China.
Husband-and-wife operations running 500-2,000 barrels/day.
At peak they processed 20%+ of China's oil.

## The Tech — Simple Distillation
```
Crude oil → Heater → Distillation column → Fractions by boiling point
  Light:  gasoline (30-200°C)
  Mid:    diesel (200-350°C)
  Heavy:  fuel oil / asphalt (>350°C)
```

Same principle as distilling alcohol. Temperature-based, no chemistry.
Just thermocouples + valves + a tower. Your PCB can control it.

## Cost
Build: $500K-$3M (vs $500M+ for Pertamina-scale)  
Land: 1-2 hectares  
Staff: 2-5 people (or zero with automation)

## Relevance to You
Your pyrolysis oil → teapot column → diesel + gasoline.
You don't need FT to make fuel. Pyrolysis + simple distillation = done.

---

# SECTION 5: AMMONIA & FERTILIZER

## Why Indonesia
- Imports 4M+ tonnes urea/year
- Fertilizer subsidy is government priority
- Any domestic production wins on logistics

## The Challenge
Haber-Bosch needs 150-250 bar. Smallest viable plant = $500M.

## Near-term Entry
Don't make ammonia. Buy bulk urea → rebrand → distribute to farmers.
Build the distribution network today. Fund R&D for production later.

---

# SECTION 6: SOLAR + THESE PROCESSES

| Process | Power Need | Solar Feasibility |
|---------|-----------|-------------------|
| FT lab | 500W-2kW | ✅ 2-4 panels |
| Pyrolysis pilot | 5-10kW | ✅ 10-20 panels |
| Pyrolysis 1tpd | 10-30kW | ✅ 20-60 panels |
| Teapot refinery | 30-100kW | ⚠️ Needs grid hybrid |

Strategy: Build in Indonesia's sun belt (East Java, NTT). Solar by day, grid by night.

---

# SECTION 7: MASTER PLAN

## Phase 1 (Now — Rp 15-30 juta)
- Build drum retort → coal pyrolysis → prove charcoal output
- Start FT lab reactor (your PCB) → learn the process
- Document everything → sell as content

## Phase 2 (3-6 months)
- Scale pyrolysis to 100kg/day → sell activated carbon → real cashflow
- Connect pyrolysis oil → simple distillation column → diesel
- Use cashflow to fund FT scale-up

## Phase 3 (6-18 months)
- Choose winner: pyrolysis products OR FT fuel
- Build teapot-scale refinery if oil volume justifies it
- Sell business plans/feasibility studies to Indonesian investors

## The Loop
```
Coal → Pyrolysis → Charcoal (sell) + Oil (distill) → Diesel (sell)
                                              ↓
                              FT reactor → Synfuel (scale later)
```

---

# QUICK REFERENCE

**Your PCB** = Arduino + MAX31855 + thermocouple + MOSFET + OLED
→ Controls temperature for: FT reactor, pyrolysis retort, distillation column

**Teapot rule:** Temperature control is 80% of the skill. You already have it.

**Best first dollar:** Pyrolysis → activated carbon. 90% margin. Feedstock is waste.

**Best long play:** FT from coal. Indonesia has the coal. China/India will buy the tech.

