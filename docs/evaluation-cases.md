# Evaluation Cases — Gratuity Checker India

This document lists test scenarios used to validate the GPT's responses.
All eligibility checks use three inputs: **Date of Joining (DOJ)**, **Last Working Day (LWD)**, and **Work Week (5-day or 6-day)**.
Each case includes the input, expected output, and the legal basis.

### What Counts as "Continuous Service"?

The 190/240 day thresholds refer to **calendar days of continuous service**, NOT just working days:
- ✅ All authorized paid leaves (earned leave, sick leave, public holidays, maternity leave, notice period) **count** toward continuous service
- ❌ Unauthorized absences that result in an official break in service do **NOT count**

If you remained officially employed and on payroll, those days count — including leave, WFH, holidays, and notice period.

---

## Category 1: Basic Eligibility (DOJ + LWD + Work Week)

### Case 1.1 — Clearly Eligible (6-day week, 6+ years)
**Input:**
- DOJ: 1 April 2017
- LWD: 30 June 2023
- Work Week: 6-day

**Expected:** Eligible. Service = ~6 years 3 months. Exceeds 5-year minimum comfortably.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

### Case 1.2 — Clearly Not Eligible (6-day week, < 4 years)
**Input:**
- DOJ: 1 January 2021
- LWD: 15 October 2024
- Work Week: 6-day

**Expected:** Not eligible. Service = ~3 years 9 months. Minimum 5 years not met, and 5th year not yet started.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

### Case 1.3 — Edge Case: 240-day rule (6-day week, 4 yrs + 240 days in 5th year)
**Input:**
- DOJ: 1 June 2019
- LWD: 26 February 2024
- Work Week: 6-day

**Expected:** Eligible. Service = 4 years + ~240 days in the 5th year. Qualifying threshold met for 6-day work week.
**Legal Basis:** Section 4(1) proviso; *Mettur Beardsell Ltd. v. Regional Labour Commissioner*

---

### Case 1.4 — Edge Case: 190-day rule (5-day week, 4 yrs + 190 days in 5th year)
**Input:**
- DOJ: 1 June 2019
- LWD: 8 January 2024
- Work Week: 5-day

**Expected:** Eligible. Service = 4 years + ~190 working days in the 5th year. Qualifying threshold met for 5-day work week.
**Legal Basis:** Section 2A read with Section 4(1); 190-day threshold for 5-day week establishments

---

### Case 1.5 — Boundary: One Day Short of 240 Days (6-day week)
**Input:**
- DOJ: 1 June 2019
- LWD: 25 February 2024
- Work Week: 6-day

**Expected:** Not eligible. One day short of 240-day threshold in the 5th year. 5 full years not completed.
**Legal Basis:** Section 4(1) read with 240-day interpretation

---

### Case 1.6 — Boundary: One Day Short of 190 Days (5-day week)
**Input:**
- DOJ: 1 June 2019
- LWD: 7 January 2024
- Work Week: 5-day

**Expected:** Not eligible. One day short of 190-day threshold in the 5th year for a 5-day work week establishment.
**Legal Basis:** Section 2A read with Section 4(1)

---

### Case 1.7 — Exactly 5 Years (both work weeks)
**Input:**
- DOJ: 15 March 2018
- LWD: 15 March 2023
- Work Week: 5-day or 6-day

**Expected:** Eligible. Exactly 5 years of continuous service qualifies regardless of work week.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

### Case 1.8 — Same DOJ/LWD, Different Work Week (eligibility flip)
**Input A:**
- DOJ: 10 July 2019, LWD: 5 January 2024, Work Week: **6-day**
- Expected: **Not eligible** (< 240 days in 5th year on a 6-day week)

**Input B:**
- DOJ: 10 July 2019, LWD: 5 January 2024, Work Week: **5-day**
- Expected: **Eligible** (>= 190 days in 5th year on a 5-day week)

**Key takeaway:** Work week type directly changes eligibility for borderline service durations.

---

## Category 2: Calculation Accuracy

### Case 2.1 — Standard Calculation with DOJ/LWD
**Input:**
- DOJ: 1 April 2015
- LWD: 31 March 2023
- Work Week: 6-day
- Basic Salary: ₹40,000/month

**Service:** 8 years exactly
**Expected Calculation:**
```
Gratuity = (40,000 × 15 × 8) / 26 = ₹1,84,615 (approx)
```

---

### Case 2.2 — Partial Year Rounds Up (>= 6 months)
**Input:**
- DOJ: 1 April 2015
- LWD: 15 December 2023
- Work Week: 6-day
- Basic + DA: ₹50,000/month

**Service:** 8 years 8 months → rounds to **9 years**
```
Gratuity = (50,000 × 15 × 9) / 26 = ₹2,59,615 (approx)
```

---

### Case 2.3 — Partial Year Rounds Down (< 6 months)
**Input:**
- DOJ: 1 April 2015
- LWD: 20 July 2023
- Work Week: 5-day
- Basic Salary: ₹60,000/month

**Service:** 8 years 3 months → rounds to **8 years**
```
Gratuity = (60,000 × 15 × 8) / 26 = ₹2,76,923 (approx)
```

---

### Case 2.4 — Maximum Cap Check
**Input:**
- DOJ: 1 January 1994
- LWD: 31 December 2023
- Work Week: 6-day
- Basic Salary: ₹2,00,000/month

**Service:** 30 years
**Raw Calculation:** (2,00,000 × 15 × 30) / 26 = ₹34,61,538
**Expected Output:** Capped at **₹20,00,000** (Payment of Gratuity Amendment Act, 2018)

---

## Category 3: Special Exit Scenarios

### Case 3.1 — Death of Employee (5-year waiver)
**Input:**
- DOJ: 10 March 2022
- Date of Death: 5 August 2024
- Work Week: 5-day

**Expected:** Eligible. 5-year minimum service waived on death. Nominee/legal heir entitled to full gratuity.
**Legal Basis:** Section 4(1) proviso, Payment of Gratuity Act, 1972

---

### Case 3.2 — Permanent Disability (5-year waiver)
**Input:**
- DOJ: 1 July 2021
- Date of Disablement: 20 November 2023
- Work Week: 6-day

**Expected:** Eligible despite < 5 years service. Minimum service waived for permanent disability.
**Legal Basis:** Section 4(1) proviso

---

### Case 3.3 — Termination for Misconduct
**Input:**
- DOJ: 1 January 2015
- LWD: 31 March 2023
- Exit Reason: Termination for wilful damage to employer property

**Expected:** Gratuity can be forfeited wholly or partially.
**Legal Basis:** Section 4(6), Payment of Gratuity Act, 1972

---

### Case 3.4 — Planned Resignation (Future LWD)
**Input:**
- DOJ: 5 September 2020
- Planned LWD: 30 November 2025
- Work Week: 5-day

**Expected:** Eligible. Projected service = ~5 years 3 months. Exceeds 5-year threshold.
**Note:** GPT should handle future LWD as a planning query.

---

## Category 4: Employment Type Edge Cases

### Case 4.1 — Contract Employee
**Input:**
- DOJ: 1 March 2018
- LWD: 28 February 2023
- Work Week: 5-day
- Employment Type: Fixed-term contract on principal employer's payroll

**Expected:** Eligible. 5 years completed. Contract employees on principal employer's payroll qualify.

---

### Case 4.2 — Organisation with < 10 Employees
**Input:**
- DOJ: 1 April 2016
- LWD: 31 March 2022
- Work Week: 5-day
- Company size: 6 employees

**Expected:** The Payment of Gratuity Act does not apply to establishments with fewer than 10 employees. Company may still have an internal gratuity policy.
**Legal Basis:** Section 1(3)(b)

---

## Summary Table

| Case | DOJ | LWD | Work Week | Expected Result | Status |
|---|---|---|---|---|---|
| 1.1 | 01-Apr-2017 | 30-Jun-2023 | 6-day | Eligible | ✅ Pass |
| 1.2 | 01-Jan-2021 | 15-Oct-2024 | 6-day | Not Eligible | ✅ Pass |
| 1.3 | 01-Jun-2019 | 26-Feb-2024 | 6-day | Eligible (240-day rule) | ✅ Pass |
| 1.4 | 01-Jun-2019 | 08-Jan-2024 | 5-day | Eligible (190-day rule) | ✅ Pass |
| 1.5 | 01-Jun-2019 | 25-Feb-2024 | 6-day | Not Eligible (1 day short) | ✅ Pass |
| 1.6 | 01-Jun-2019 | 07-Jan-2024 | 5-day | Not Eligible (1 day short) | ✅ Pass |
| 1.7 | 15-Mar-2018 | 15-Mar-2023 | Both | Eligible (exactly 5 yrs) | ✅ Pass |
| 1.8A | 10-Jul-2019 | 05-Jan-2024 | 6-day | Not Eligible | ✅ Pass |
| 1.8B | 10-Jul-2019 | 05-Jan-2024 | 5-day | Eligible | ✅ Pass |
| 2.4 | 01-Jan-1994 | 31-Dec-2023 | 6-day | Capped at ₹20L | ✅ Pass |
| 3.1 | 10-Mar-2022 | Death: 05-Aug-2024 | 5-day | Eligible (waiver) | ✅ Pass |
| 4.2 | 01-Apr-2016 | 31-Mar-2022 | 5-day | Act not applicable (<10 emp) | ✅ Pass |

---

*Last reviewed: June 2026*
