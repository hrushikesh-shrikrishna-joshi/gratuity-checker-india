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

Gratuity calculation in India is often misunderstood. Employees don't know if they qualify, HR teams manually calculate payouts, and edge cases (like 4 years 240 days, contract employees, or death/disability) create confusion and payroll errors.

This GPT gives anyone — employee, HR, or payroll manager — a fast, conversational way to:
- Check if an employee qualifies for gratuity
- Estimate the exact payout amount
- Understand edge cases specific to Indian labour law
- Get plain-English explanations of complex clauses

---

## Key Features

| Feature | Details |
|---|---|
| Eligibility Check | Determines qualification based on years of service, employment type, and exit reason |
| Payout Calculation | Computes gratuity using last drawn salary and years of service |
| Edge Case Handling | Covers 4 yrs 240 days rule, death/disability, resignation vs. termination |
| Act Reference | Cites relevant sections of the Payment of Gratuity Act, 1972 |
| Plain Language | Explains results in simple, jargon-free language |
| India-Specific | Focused exclusively on Indian labour law — no generic global advice |

---

## Example Prompts

Here are real questions you can ask this GPT:

```
I have worked for 4 years and 242 days. Am I eligible for gratuity?
```

```
My last drawn basic salary is ₹45,000 and I have completed 7 years and 8 months of service.
Calculate my gratuity.
```

```
If an employee dies after 2 years of service, is the nominee entitled to gratuity?
```

```
What is the maximum gratuity amount payable under the current law?
```

```
Does gratuity apply to contract employees or only permanent staff?
```

```
My employer is refusing to pay gratuity. What are my legal options?
```

---

## How Gratuity Is Calculated

The GPT uses the standard formula defined in the Act:

**For employees covered under the Act:**
```
Gratuity = (Last Drawn Salary × 15 × Years of Service) / 26
```

**For employees NOT covered under the Act:**
```
Gratuity = (Last Drawn Salary × 15 × Years of Service) / 30
```

> **Salary** here means Basic + Dearness Allowance (DA) only — not CTC or gross salary.
> **Maximum** gratuity payable is ₹20,00,000 (₹20 Lakhs) as of the latest notification.

---

## Key Rules Covered

- Minimum 5 years of continuous service required (with the 4 yrs 240 days exception)
- Applies to establishments with 10 or more employees
- Covers resignation, retirement, retrenchment, death, and disability
- Employer must pay within 30 days of it becoming payable
- Gratuity can be forfeited for misconduct causing damage/loss
- Nominees / legal heirs receive gratuity in case of employee's death

---

## Who Is This For?

- **Employees** — checking eligibility before or after leaving a job
- **HR Professionals** — quick reference for common gratuity queries
- **Payroll Teams** — verifying calculation methodology
- **Finance Students** — learning Indian labour law in a practical way
- **Startup Founders** — understanding obligations when building a team

---

## Assumptions & Limitations

- Calculations are based on the **Payment of Gratuity Act, 1972** and its amendments
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
1. The question you asked
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

> *This project is a demonstration of domain-specific Custom GPT design, prompt engineering, and product documentation. It is not a substitute for professional HR, legal, or payroll advice.*
