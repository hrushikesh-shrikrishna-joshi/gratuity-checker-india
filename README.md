# Gratuity Checker India 🇮🇳

> A Custom GPT that helps employees, HR professionals, and payroll teams quickly check **gratuity eligibility** and **calculate gratuity payouts** under the **Payment of Gratuity Act, 1972**.

[![Custom GPT](https://img.shields.io/badge/ChatGPT-Custom%20GPT-10a37f?style=for-the-badge&logo=openai&logoColor=white)](https://chatgpt.com/g/g-69d20abb914881918eecf9e73964feb0-gratuity-checker-india)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)]

---

## Try It Live

**[>> Open Gratuity Checker India on ChatGPT](https://chatgpt.com/g/g-69d20abb914881918eecf9e73964feb0-gratuity-checker-india)**

> Requires a free or paid ChatGPT account to use.

---

## What Problem Does This Solve?

Gratuity calculation in India is often misunderstood. Employees don't know if they qualify, HR teams manually calculate payouts, and edge cases (like the 4 years 240 days rule, contract employees, or death/disability) create confusion and payroll errors.

This GPT gives anyone — employee, HR, or payroll manager — a fast, conversational way to:
- Check if an employee qualifies for gratuity using real dates
- Estimate the exact payout amount
- Understand edge cases specific to Indian labour law
- Get plain-English explanations of complex clauses

---

## What Is Gratuity?

- **Gratuity** is a lump-sum payment made by an employer to an employee as a **reward for long-term service**.
- It is governed by the **Payment of Gratuity Act, 1972**.
- **It is NOT a deduction from your salary.** The employer pays it from their own funds.
- Most IT and private companies with **10 or more employees** are covered by this law.

---

## Key Features

| Feature | Details |
|---|---|
| Eligibility Check | Determines qualification based on **Date of Joining (DOJ)**, **Last Working Day (LWD)**, and **work week (5-day or 6-day)** |
| Payout Calculation | Computes gratuity using last drawn salary and service duration derived from DOJ → LWD |
| Edge Case Handling | Covers 4 yrs 240/190 days rule (based on work week), death/disability, resignation vs. termination |
| What Counts as Service | Includes paid leaves, earned leave, sick leave, public holidays, maternity leave, and notice period |
| Act Reference | Cites relevant sections of the Payment of Gratuity Act, 1972 |
| Plain Language | Explains results in simple, jargon-free language |
| India-Specific | Focused exclusively on Indian labour law — no generic global advice |

---

## How Eligibility Is Determined

The GPT calculates actual service duration from your **Date of Joining (DOJ)** to your **Last Working Day (LWD)** and checks the qualifying threshold based on your **work week**:

| Work Week | Qualifying Days in 5th Year | Equivalent |
|---|---|---|
| 6-day work week | 240 days | ~8 months |
| 5-day work week | 190 days | ~7.5 months |

**Standard rule:** Minimum 5 years of continuous service.

**Edge case rule:** If you haven't completed 5 full years, but have completed **240 days (6-day week)** or **190 days (5-day week)** in the 5th year — you are still eligible.

> These are **calendar days of continuous service**, not just working days. All authorized paid leaves, earned leave, sick leave, public holidays, maternity leave, and notice period count toward continuous service. Unauthorized absences that result in a break do NOT count.

**Inputs needed for eligibility check:**
1. **Date of Joining (DOJ)** — e.g., `15 March 2018`
2. **Last Working Day (LWD)** — e.g., `10 June 2023` (actual or planned)
3. **Work Week** — 5-day or 6-day

---

## Example Prompts

Here are real questions you can ask this GPT:

```
My Date of Joining is 10 April 2019 and my Last Working Day is 20 June 2024.
I work a 5-day week. Am I eligible for gratuity?
```

```
DOJ: 1 July 2020, LWD: 15 March 2025, 6-day work week.
Calculate my gratuity. Basic salary is ₹52,000/month.
```

```
I joined on 5 January 2021. I am planning to resign on 30 September 2025.
My company has a 5-day work week. Will I qualify for gratuity?
```

```
I have worked for 4 years and 8 months at a company with a 6-day work week.
My DOJ was 1 June 2020. When is the earliest I can resign and still get gratuity?
```

```
If an employee dies after 2 years of service, is the nominee entitled to gratuity?
```

```
My employer is refusing to pay gratuity. What are my legal options?
```

---

## How Gratuity Is Calculated

Once eligibility is confirmed (from DOJ, LWD, and work week), the payout is computed using the standard formula:

**For employees covered under the Act:**
```
Gratuity = (Last Drawn Salary × 15 × Years of Service) / 26
```

**For employees NOT covered under the Act:**
```
Gratuity = (Last Drawn Salary × 15 × Years of Service) / 30
```

### Understanding the Formula

- **15** = 15 days of salary
- **26** = Represents a 26-working-day month (30 days - 4 Sundays)
- **30** = For establishments operating all 7 days (no weekly offs)

### What Counts as "Salary" or "Wages"?

- **Traditionally:** Basic Salary + Dearness Allowance (DA) only — **not CTC or gross salary**.
- **In most IT companies:** DA is often zero, so Basic Salary alone is used.
- **Important exception:** If your Basic + DA is less than 50% of your total pay, part of your allowances may be included to bring "wages" closer to 50% for statutory calculations.

> **Years of Service** is computed from DOJ to LWD. Fractions ≥ 6 months round up.
> **Maximum** gratuity payable is ₹20,00,000 (₹20 Lakhs) as of the latest notification.

---

## What Counts as Continuous Service?

✅ **Counts:**
- All authorized paid leaves (earned leave, sick leave)
- Public holidays
- Maternity leave
- Notice period (you're on payroll until LWD)
- Work from home days
- Official training/probation period (if you were paid as an employee)

❌ **Does NOT count:**
- Unauthorized absences that result in an official break in service
- Unpaid internships (unless you were treated as a paid employee)

> **Key takeaway:** If you remained officially employed and on payroll, those days count — including leave, WFH, holidays, and notice period.

---

## Key Rules Covered

- Minimum **5 years of continuous service** required (DOJ to LWD)
- **5-day work week:** 190+ days in the 5th year qualifies (even if < 5 full years)
- **6-day work week:** 240+ days in the 5th year qualifies (even if < 5 full years)
- Applies to establishments with 10 or more employees
- Covers resignation, retirement, retrenchment, death, and disability
- Employer must pay within 30 days of it becoming payable (delays attract interest)
- Gratuity can be forfeited for misconduct causing damage/loss
- Nominees / legal heirs receive gratuity in case of employee's death

---

## Common Myths Busted

| Myth | Reality |
|---|---|
| You must complete exactly 5 full years to get gratuity. | No — 4 years, 190 days for 5-day workweek OR 4 years, 240 days for 6-day workweek! |
| Only days present in office are counted. | All approved leaves and holidays count as per law. |
| Notice period doesn't count. | It ABSOLUTELY counts — you're on payroll until your LWD. |
| Gratuity is paid from your own salary/CTC. | False — it's your employer's liability, not a salary deduction. |
| Company policy overrides the law if they started gratuity later. | Doesn't matter when the company started it — your whole tenure from DOJ gets calculated. |
| If company changes HR rules, your old period is excluded. | Your service period as per contract and law must be included. |

---

## Who Is This For?

- **Employees** — checking eligibility before or after leaving a job
- **HR Professionals** — quick reference for common gratuity queries
- **Payroll Teams** — verifying calculation methodology
- **Finance Students** — learning Indian labour law in a practical way
- **Startup Founders** — understanding obligations when building a team

---

## Assumptions & Limitations

- Eligibility is computed from actual **DOJ** and **LWD** dates provided by the user
- Work week (5-day or 6-day) determines which day-count threshold applies in the 5th year
- Calculations are based on the **Payment of Gratuity Act, 1972** and its amendments
- **Does not fully cover changes introduced under the 2025 Labour Codes** or later amendments
- Does not account for company-specific gratuity policies that may be *more* generous than the Act
- Does not replace formal legal, HR, or payroll advice
- Tax implications of gratuity (income tax exemption under Section 10(10)) are explained conceptually but tax-specific advice should be verified with a CA
- Data used in calculations is not stored or retained between sessions

See [`docs/disclaimer.md`](docs/disclaimer.md) for full disclaimer.

---

## Documentation

| File | Description |
|---|---|
| [`docs/evaluation-cases.md`](docs/evaluation-cases.md) | Test scenarios and edge cases used to validate GPT responses |
| [`docs/disclaimer.md`](docs/disclaimer.md) | Legal and usage disclaimer |
| [`docs/roadmap.md`](docs/roadmap.md) | Planned improvements and future features |

---

## Built With

- [OpenAI Custom GPTs](https://openai.com/blog/introducing-gpts) — GPT Builder platform
- Payment of Gratuity Act, 1972 (India)
- Ministry of Labour & Employment, Government of India guidelines

---

## Contributing

Found an edge case this GPT handles incorrectly? Open an issue with:
1. The DOJ, LWD, work week, and salary you used
2. The response you received
3. What the correct answer should be (with a source/reference)

Pull requests for documentation improvements are welcome.

---

## License

This repository is licensed under the [MIT License](LICENSE). The GPT itself is hosted on OpenAI's platform.

---

## Author

**Hrushikesh Joshi**
Senior Software Engineer | Pune, India

[![GitHub](https://img.shields.io/badge/GitHub-hrushikesh--shrikrishna--joshi-181717?style=flat&logo=github)](https://github.com/hrushikesh-shrikrishna-joshi)

---

## Legal References

- [Payment of Gratuity Act, 1972 - Official Website](https://clc.gov.in/clc/acts-rules/payment-gratuity-act)
- Section 4, Payment of Gratuity Act, 1972 — Gratuity payable after 5 years of continuous service
- Section 2A — Defines continuous service (190 days for 5-day week, 240 days for 6-day week)
- Section 7(3) — Gratuity must be paid within 30 days of separation; delays attract interest
- Landmark Judgment: *Mettur Beardsell Ltd. vs. RLC, 1996* (Madras HC) — Interpreted < 5 years with 240 days as eligible

---

> *This project is a demonstration of domain-specific Custom GPT design, prompt engineering, and product documentation. It is not a substitute for professional HR, legal, or payroll advice.*
