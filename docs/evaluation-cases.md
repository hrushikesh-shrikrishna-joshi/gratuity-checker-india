# Evaluation Cases — Gratuity Checker India

This document lists test scenarios used to validate the GPT's responses. Each case includes the input, expected output, and the legal basis.

---

## Category 1: Basic Eligibility

### Case 1.1 — Standard Eligibility (5+ years)
**Input:** "I have completed 6 years of service. Am I eligible for gratuity?"
**Expected:** Yes, eligible. Minimum 5 years of continuous service is met.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

### Case 1.2 — Less Than 5 Years (Not Eligible)
**Input:** "I have worked for 3 years and 10 months. Can I get gratuity?"
**Expected:** Not eligible under standard rules. Service is less than 5 years and does not meet the 240-day exception.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

### Case 1.3 — The 4 Years 240 Days Edge Case
**Input:** "I have worked for 4 years and 240 days. Am I eligible?"
**Expected:** Yes, eligible. The 240-day rule in the 5th year counts as completion of 5 years.
**Legal Basis:** Supreme Court ruling in *Mettur Beardsell Ltd. v. Regional Labour Commissioner* — completing 240 days in the 5th year qualifies.

---

### Case 1.4 — 4 Years 239 Days (Boundary Test)
**Input:** "I resigned after 4 years and 239 days of service."
**Expected:** Not eligible. Falls one day short of the 240-day threshold in the 5th year.
**Legal Basis:** Section 4(1) read with the 240-day interpretation

---

### Case 1.5 — Exactly 5 Years
**Input:** "I completed exactly 5 years today and am resigning."
**Expected:** Eligible. Exactly 5 years qualifies.
**Legal Basis:** Section 4(1), Payment of Gratuity Act, 1972

---

## Category 2: Calculation Accuracy

### Case 2.1 — Standard Calculation
**Input:** "Basic salary ₹40,000/month, 8 years of service."
**Expected Calculation:**
```
Gratuity = (40,000 × 15 × 8) / 26
         = 48,00,000 / 26
         = ₹1,84,615 (approx)
```
**Note:** Rounded to nearest rupee.

---

### Case 2.2 — Salary with DA Included
**Input:** "Basic ₹30,000 + DA ₹5,000. Service: 10 years."
**Expected:** Salary for calculation = ₹35,000 (Basic + DA only)
```
Gratuity = (35,000 × 15 × 10) / 26 = ₹2,01,923 (approx)
```

---

### Case 2.3 — Maximum Cap Check
**Input:** "Salary ₹2,00,000/month. Service: 30 years."
**Expected Calculation:**
```
Gratuity = (2,00,000 × 15 × 30) / 26 = ₹34,61,538
```
**But:** Capped at ₹20,00,000 (₹20 Lakhs) as per the Payment of Gratuity (Amendment) Act, 2018.
**Expected Output:** ₹20,00,000

---

### Case 2.4 — Partial Year Rounding
**Input:** "Service: 7 years 8 months. Basic salary ₹50,000."
**Expected:** 7 years 8 months rounds to 8 years (as per the Act, fraction of year ≥ 6 months rounds up).
```
Gratuity = (50,000 × 15 × 8) / 26 = ₹2,30,769 (approx)
```

---

### Case 2.5 — Partial Year Below 6 Months
**Input:** "Service: 9 years 4 months. Basic ₹60,000."
**Expected:** 9 years 4 months treated as 9 years (fraction < 6 months rounded down).
```
Gratuity = (60,000 × 15 × 9) / 26 = ₹3,11,538 (approx)
```

---

## Category 3: Special Exit Scenarios

### Case 3.1 — Death of Employee
**Input:** "An employee died after 2 years of service. Is the nominee entitled to gratuity?"
**Expected:** Yes. In case of death or disablement, the 5-year minimum service requirement is waived. Nominee/legal heir receives full gratuity.
**Legal Basis:** Section 4(1) proviso, Payment of Gratuity Act, 1972

---

### Case 3.2 — Permanent Disability
**Input:** "Employee suffered permanent disability due to an accident at work after 3 years."
**Expected:** Eligible for gratuity despite service < 5 years. Minimum service waived for disability.
**Legal Basis:** Section 4(1) proviso

---

### Case 3.3 — Termination for Misconduct
**Input:** "Employee was terminated for misconduct and damage to property. Can employer withhold gratuity?"
**Expected:** Gratuity can be forfeited wholly or partially if termination is due to wilful omission or negligence causing damage/loss to the employer.
**Legal Basis:** Section 4(6), Payment of Gratuity Act, 1972

---

### Case 3.4 — Voluntary Resignation
**Input:** "I am resigning voluntarily after 6 years. Am I eligible?"
**Expected:** Yes. Resignation does not disqualify an employee from gratuity if minimum service is complete.
**Legal Basis:** Section 4(1)

---

### Case 3.5 — Superannuation / Retirement
**Input:** "Employee is retiring at age 60 with 25 years of service."
**Expected:** Fully eligible. Retirement is one of the qualifying exit reasons.
**Legal Basis:** Section 4(1)

---

## Category 4: Employment Type Edge Cases

### Case 4.1 — Contract Employee
**Input:** "I am on a fixed-term contract for 3 years. Do I qualify for gratuity?"
**Expected:** Contract employees on the payroll of the principal employer are eligible if they complete 5 years of continuous service. If on a contractor's payroll, eligibility depends on whether the contractor employs 10+ people.

---

### Case 4.2 — Seasonal Employment
**Input:** "I work in a factory that operates only 6 months a year. Do I qualify?"
**Expected:** For seasonal establishments, the Act applies. Continuous service for seasonal workers is calculated as 75 days per year (not 240 days).
**Legal Basis:** Section 2A, Payment of Gratuity Act, 1972

---

### Case 4.3 — Organisation with Less Than 10 Employees
**Input:** "My company has only 7 employees. Does the Gratuity Act apply?"
**Expected:** The Act applies to establishments with 10 or more employees. Below 10, the Act does not apply — but a company may still have its own gratuity policy.
**Legal Basis:** Section 1(3)(b)

---

## Category 5: Legal Rights & Process

### Case 5.1 — Employer Refusing to Pay
**Input:** "My employer is refusing to pay my gratuity after I left 2 months ago. What can I do?"
**Expected:** Employee can file a complaint with the Controlling Authority (typically the Labour Commissioner) under Section 7 of the Act. Employer is liable to pay interest for delayed payment beyond 30 days.

---

### Case 5.2 — Tax on Gratuity
**Input:** "Is the gratuity amount taxable?"
**Expected:** For government employees, gratuity is fully exempt. For private sector employees covered under the Act, gratuity is exempt up to ₹20 Lakhs under Section 10(10) of the Income Tax Act. Amount above ₹20 Lakhs is taxable.

---

## Summary Table

| Case | Input Scenario | Expected Result | Status |
|---|---|---|---|
| 1.1 | 6 years service | Eligible | ✅ Pass |
| 1.2 | 3 years 10 months | Not Eligible | ✅ Pass |
| 1.3 | 4 years 240 days | Eligible (edge case) | ✅ Pass |
| 1.4 | 4 years 239 days | Not Eligible | ✅ Pass |
| 1.5 | Exactly 5 years | Eligible | ✅ Pass |
| 2.1 | ₹40K, 8 years | ₹1,84,615 | ✅ Pass |
| 2.3 | ₹2L, 30 years | Capped at ₹20L | ✅ Pass |
| 3.1 | Employee death | Eligible (waiver) | ✅ Pass |
| 3.3 | Misconduct | Partial/Full Forfeiture | ✅ Pass |
| 4.3 | <10 employees | Act not applicable | ✅ Pass |

---

*Last reviewed: June 2026*
