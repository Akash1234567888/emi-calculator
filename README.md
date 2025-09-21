
# EMI Calculator

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  
![Status](https://img.shields.io/badge/status-ready-blue)

A simple, fast EMI (Equated Monthly Installment) Calculator that computes monthly installments, total interest, and total payment for a loan. Enter loan amount, annual interest rate, and tenure — the calculator returns precise results and a repayment schedule to help financial planning.

---

## 🔧 Features

- Calculate monthly EMI, total interest payable, and total repayment.
- Shows an amortization schedule (month-by-month principal & interest).
- Lightweight — runs fully in the browser (no server required).
- Accessible UI and quick results — ideal for embedding into websites or using as a learning project.

---

## 📐 Formula

Monthly interest rate \( r \) = (annualInterestRate / 100) / 12  
Number of months \( n \) = tenureYears × 12

\[
\text{EMI} = P \times \frac{r \times (1+r)^n}{(1+r)^n - 1}
\]

Where:
- \(P\) = loan principal
- \(r\) = monthly interest rate
- \(n\) = total number of monthly payments

---

## 🚀 Demo

> Add a GIF or link to a live demo here (e.g., GitHub Pages).  
> `https://your-username.github.io/emi-calculator/` (replace when published)

---

## 💻 Quick Start (static HTML + JS)

Copy these files into a folder and open `index.html` in your browser.

### `index.html`
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>EMI Calculator</title>
  <style>
    body { font-family: Arial, sans-serif; max-width:700px; margin:2rem auto; padding:1rem; }
    label, input { display:block; margin:0.4rem 0; }
    .result { margin-top:1rem; padding:1rem; border:1px solid #ddd; border-radius:6px; background:#fafafa; }
  </style>
</head>
<body>
  <h1>EMI Calculator</h1>

  <label>Loan Amount (₹)
    <input id="principal" type="number" value="500000" />
  </label>

  <label>Annual Interest Rate (%)
    <input id="annualRate" type="number" step="0.01" value="8.5" />
  </label>

  <label>Tenure (years)
    <input id="tenure" type="number" value="5" />
  </label>

  <button id="calcBtn">Calculate EMI</button>

  <div id="output" class="result" aria-live="polite"></div>

  <script src="emi.js"></script>
</body>
</html>
