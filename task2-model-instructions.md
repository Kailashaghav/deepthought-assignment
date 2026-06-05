# Task 2: Google Sheets Model

## How to Build It

Create a new Google Sheet. Column A/B = Inputs. Column D/E = Outputs.

---

## INPUTS (Column A = Label, Column B = Value)

| Cell | Label | Enter This Value |
|---|---|---|
| B2 | Selling Price (SP) | 800 |
| B3 | COGS | 280 |
| B4 | Amazon Referral Fee % | 0.12 |
| B5 | Monthly Ad Spend | 300000 |
| B6 | Units Sold via Ads | 1500 |
| B7 | Organic Units Sold | 2000 |
| B8 | Fixed Costs (monthly) | 150000 |

---

## OUTPUTS (Column D = Label, Column E = Formula)

| Cell | Label | Formula |
|---|---|---|
| E2 | Gross Margin per Unit | =B2-B3 |
| E3 | Amazon Fee per Unit | =B2*B4 |
| E4 | Ad Cost per Unit | =B5/B6 |
| E5 | Net Margin (Ad Units) | =E2-E3-E4 |
| E6 | Net Margin (Organic Units) | =E2-E3 |
| E7 | Total Monthly Revenue | =B2*(B6+B7) |
| E8 | Total Monthly Profit | =(E5*B6)+(E6*B7)-B8 |
| E9 | ACOS (%) | =B5/(B2*B6)*100 |
| E10 | TACOS (%) | =B5/E7*100 |
| E11 | Break-Even Ad Spend | =(E6*B7)+(E2-E3)*B6-B8 |

---

## Conditional Formatting

1. Select E8 → Format > Conditional formatting
   → Less than 0 → Red background

2. Select E10 → Format > Conditional formatting
   → Greater than 15 → Yellow background
   → Greater than 20 → Red background

---

## Scenario Results

| Scenario | Change | New Profit | TACOS |
|---|---|---|---|
| Base case | Default values | ₹10,34,000 | 10.7% |
| SP → ₹950 | B2 = 950 | ~₹14,80,000 | ~9.1% |
| COGS +20% | B3 = 336 | ~₹8,20,000 | 10.7% |
| Organic → 3,500 | B7 = 3500 | ~₹13,20,000 | ~8.1% |
| SP → ₹700 (price war) | B2 = 700 | ~₹6,40,000 | ~12.5% |
