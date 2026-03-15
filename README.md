# Retirement Calculator: See your money compound over time

A single-file, interactive retirement planning tool. Model your nest egg, withdrawal income, and sensitivity across different retirement ages — no backend, no dependencies, no install required.

## What it does

- **Wealth accumulation** — projects your portfolio from today to retirement, broken down by initial investments, contributions, and interest earned
- **Retirement income (4% rule)** — fixed annual withdrawal at 4% of starting balance; portfolio keeps growing and leaves an estate
- **Retirement income (fixed drawdown)** — withdraws exactly enough each year to reach $0 at your life expectancy; withdrawals increase over time as the balance compounds
- **Retirement age sensitivity** — clickable age cards (±10 years from your planned retirement) with full income breakdowns and side-by-side charts for each age
- **Sensitivity table** — full ±10 year table showing nest egg, vs-plan diff, 4% income, and drawdown income for every age
- **Share my scenario** — encodes all inputs into a URL, copies to clipboard so anyone can open your exact scenario
- **Fully interactive** — all inputs update charts and metrics instantly

## Inputs

| Field | Description |
|---|---|
| Current age | Your age today |
| Planned retirement age | The age you plan to stop working |
| Life expectancy | Used to calculate drawdown to $0 |
| Current investments | Your total invested balance today |
| Annual contribution | How much you add per year until retirement |
| Growth rate (accumulation) | Expected annual return while working (e.g. 7%) |
| Growth rate (retirement) | More conservative return after retiring (e.g. 4%) |

## How to run

This is a single HTML file — no server, no build step, no dependencies.

**Option 1: Open on GitHub Pages**

<https://acepeda2019.github.io/retirement_calculator/>

**Option 2: Open directly in a browser**

Download or clone the repo, then double-click `index.html` — or from the terminal:
```bash
open index.html
```

## Project structure

```
retirement-calculator/
├── index.html    # the entire app — HTML, CSS, and JS in one file
├── preview.png   # og:image for link previews
└── README.md     # this file
```

All charting is handled by [Chart.js](https://www.chartjs.org/) loaded via CDN. Fonts are loaded from Google Fonts. No other external dependencies.

## Assumptions & disclaimers

- Returns are modeled as a fixed annual percentage — real markets are not this smooth
- Contributions are assumed to be made at the start of each year
- The 4% rule is based on historical research for 30-year retirements; your mileage may vary
- This tool is for **educational and planning purposes only** — not financial advice
- Always consult a qualified financial advisor before making retirement decisions
