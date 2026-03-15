# Compound — Retirement Calculator

A single-file, interactive retirement planning tool. Model your nest egg, withdrawal income, and sensitivity across different retirement ages — no backend, no dependencies, no install required.

## What it does

- **Wealth accumulation** — projects your portfolio from today to retirement, broken down by initial savings, contributions, and interest earned
- **Retirement income (4% rule)** — fixed annual withdrawal at 4% of starting balance; portfolio keeps growing and leaves an estate
- **Retirement income (fixed drawdown)** — withdraws exactly enough each year to reach $0 at your life expectancy; withdrawals increase over time as the balance compounds
- **Fully interactive** — all inputs update charts and metrics instantly

## Inputs

| Field | Description |
|---|---|
| Current age | Your age today |
| Retirement age | The age you plan to stop working |
| Life expectancy | Used to calculate drawdown to $0 |
| Current savings | Your total invested balance today |
| Annual contribution | How much you add per year until retirement |
| Growth rate (accumulation) | Expected annual return while working (e.g. 7%) |
| Growth rate (retirement) | More conservative return after retiring (e.g. 5%) |

## How to run

This is a single HTML file — no server, no build step, no dependencies.

**Option 1: Open on GitHub Pages**

<https://acepeda2019.github.io/retirement-calculator>

**Option 2: Open directly in a browser**

Download or clone the repo, then double-click `index.html` — or from the terminal:
```bash
open index.html
```

## Project structure

```
retirement-calculator/
├── index.html   # the entire app — HTML, CSS, and JS in one file
└── README.md    # this file
```

All charting is handled by [Chart.js](https://www.chartjs.org/) loaded via CDN. Fonts are loaded from Google Fonts. No other external dependencies.

## Assumptions & disclaimers

- Returns are modeled as a fixed annual percentage — real markets are not this smooth
- Contributions are assumed to be made at the start of each year
- The 4% rule is based on historical research for 30-year retirements; your mileage may vary
- This tool is for **educational and planning purposes only** — not financial advice
- Always consult a qualified financial advisor before making retirement decisions

## Customizing defaults

The default values (age 36, $500k balance, $32k/yr contribution, 7% return) are set in the HTML inputs. To change them for your audience, open `index.html` and update the `value` attributes on each `<input>` element.
