# Roadmap — Gratuity Checker India

This document tracks the current status and planned improvements for the Gratuity Checker India GPT.

---

## Current Version: v1.0

**Status:** Live and Active
**Launch Date:** June 2026
**Platform:** OpenAI Custom GPT (ChatGPT)

### What v1.0 Covers
- [x] Basic gratuity eligibility check (5-year rule)
- [x] 4 years 240 days edge case handling
- [x] Standard payout calculation using the Payment of Gratuity Act formula
- [x] Salary = Basic + DA clarification
- [x] Maximum cap enforcement (₹20 Lakhs)
- [x] Partial year rounding (>= 6 months rounds up)
- [x] Death and disability scenarios (5-year waiver)
- [x] Resignation, retirement, and retrenchment scenarios
- [x] Misconduct and forfeiture explanation
- [x] Tax exemption overview (Section 10(10) of Income Tax Act)
- [x] Employer refusal and legal recourse guidance
- [x] Contract and seasonal employment basic coverage

---

## Planned: v1.1 — Coverage Improvements

**Priority:** High
**Target:** Q3 2026

- [ ] **Sector-Specific Rules** — Journalists (Working Journalists Act), Plantation Workers, Mines Act workers
- [ ] **State-Level Variations** — Where state shops & establishment acts override the central Act
- [ ] **Seasonal Establishment Calculation** — Improve 75-day rule explanation with examples
- [ ] **Piece-Rate Workers** — Gratuity calculation for workers paid on piece-rate basis (average of last 3 months)
- [ ] **Compulsory Retirement vs. Voluntary Retirement Scheme (VRS)** — Different treatment in calculations

---

## Planned: v1.2 — Usability Improvements

**Priority:** Medium
**Target:** Q4 2026

- [ ] **Step-by-Step Calculation Mode** — Ask user for inputs one at a time for better accuracy
- [ ] **Comparison Mode** — Compare two scenarios (e.g., resign now vs. complete one more year)
- [ ] **"Explain Like I'm 5" Mode** — Simpler language mode for non-HR users
- [ ] **Checklist Output** — Generate a checklist of documents needed to claim gratuity
- [ ] **Timeline Generator** — Tell user when the employer must pay by, given exit date

---

## Planned: v2.0 — Expanded Indian Labour Law Suite

**Priority:** Low (Future)
**Target:** 2027

- [ ] **Provident Fund (PF) Checker** — EPF eligibility and withdrawal rules
- [ ] **Leave Encashment Calculator** — Earned leave payout on exit
- [ ] **ESIC Eligibility Checker** — Employee State Insurance Corporation coverage rules
- [ ] **Notice Period & Full & Final Settlement Guide** — What goes into F&F calculations
- [ ] **New Labour Codes Integration** — Reflect changes under the 4 Labour Codes (once operationalised)
  - Code on Wages, 2019
  - Industrial Relations Code, 2020
  - Social Security Code, 2020
  - Occupational Safety Code, 2020

---

## Known Limitations to Address

| Issue | Priority | Status |
|---|---|---|
| No real-time Act amendment tracking | High | Pending |
| State-specific rules not fully covered | High | Planned v1.1 |
| Sector-specific rules incomplete | High | Planned v1.1 |
| No multi-employer / multiple stints calculation | Medium | Planned v1.2 |
| No PDF/export of calculation summary | Low | Future |
| No Hindi or Marathi language support | Low | Future |

---

## Changelog

### v1.0 — June 2026
- Initial launch of Gratuity Checker India on OpenAI Custom GPT platform
- Covers core eligibility, calculation, and edge cases
- GitHub repository created with full documentation

---

## How to Suggest Features

Open a GitHub Issue with the label `enhancement` and describe:
1. The current behaviour or gap
2. The desired behaviour
3. A real-world example or use case
4. Any relevant legal reference (section of the Act, court ruling, etc.)

---

*Last updated: June 2026*
