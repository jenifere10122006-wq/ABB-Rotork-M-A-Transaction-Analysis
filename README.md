# ABB / Rotork: M&A Transaction Analysis

## Overview

This project analyses ABB Ltd's recommended all-cash acquisition of Rotork plc and models the transaction from an investment-banking perspective.

I built a transaction model covering:

- offer mechanics and acquisition premium;
- equity purchase price and enterprise value;
- transaction multiples;
- sources and uses of funds;
- acquisition financing;
- implied EBITDA synergies;
- EPS accretion / dilution; and
- sensitivity to synergy realisation and borrowing costs.

The objective was to understand how a public M&A transaction moves from announced deal terms to purchase price, financing requirements and pro forma earnings impact.

---

## Transaction Overview

ABB announced a recommended all-cash offer for Rotork on 16 July 2026.

| Metric | Value |
|---|---:|
| Cash consideration | 503p/share |
| Permitted dividend | Up to 3p/share |
| Total potential shareholder value | 506p/share |
| Unaffected Rotork share price | 290.8p |
| Premium to unaffected price | 73.0% |
| 3-month VWAP | 309.2p |
| Premium to 3-month VWAP | 62.7% |
| Fully diluted Rotork shares | 822.3m |
| Implied equity purchase price | $5.57bn |
| Disclosed implied enterprise value | $5.50bn |
| EV / 2025A Sales | 5.25x |
| EV / 2025A Adjusted EBITDA | 19.5x |
| Expected completion | H1 2027 |

As of the model date, shareholder and Court meetings had approved the transaction, while Court sanction and remaining closing conditions were still outstanding.

---

## 1. Purchase Price & Enterprise Value

I first translated the announced offer terms into an implied equity purchase price.

The model uses:

$$
\text{Equity Purchase Price}
=
\text{Offer Price per Share}
\times
\text{Fully Diluted Shares}
$$

Using 503p per share and approximately 822.3 million diluted shares gives an equity purchase price of approximately **£4.14bn**, or **$5.57bn** at the transaction-date GBP/USD exchange rate.

I then bridge equity value to enterprise value by adjusting for Rotork's cash, debt, lease liabilities and pension deficit.

The resulting model enterprise value is consistent with the approximately **$5.50bn disclosed transaction EV**.

---

## 2. Transaction Multiples

Rotork's 2025 adjusted financials imply acquisition multiples of approximately:

- **5.25x EV / Sales**
- **19.5x EV / Adjusted EBITDA**

These multiples highlight the relatively high entry valuation paid by ABB and provide the starting point for analysing the economic importance of potential synergies.

---

## 3. Financing & Sources and Uses

I constructed a sources-and-uses schedule to determine how ABB could fund the acquisition.

### Uses

| Use | $m |
|---|---:|
| Cash consideration | 5,573 |
| Transaction fees | 25 |
| Target debt refinancing | 60 |
| **Total Uses** | **5,659** |

### Sources

| Source | $m |
|---|---:|
| ABB Robotics disposal proceeds | 4,800 |
| ABB existing cash | 500 |
| Incremental debt / facilities | 359 |
| **Total Sources** | **5,659** |

The model therefore requires approximately **$359m of incremental borrowing** after applying the expected Robotics disposal proceeds and $500m of ABB cash.

The financing schedule also models:

- a **4.5% base borrowing rate** on incremental debt;
- a **3.5% foregone yield** on ABB cash used; and
- approximately **$24.9m of annual after-tax financing drag**.

Sources and uses reconcile to zero.

The simplified financing drag is:

$$
\text{After-Tax Financing Drag}
=
\left(
\text{Incremental Debt}
\times
\text{Borrowing Rate}
+
\text{Cash Used}
\times
\text{Foregone Yield}
\right)
\times
(1-\text{Tax Rate})
$$

---

## 4. Implied Synergy Analysis

ABB described the transaction using a post-synergy EV / EBITDA multiple in the "mid-teens" but did not provide a specific EBITDA synergy target in the transaction announcement used for this model.

I therefore reverse-engineered the level of EBITDA synergies implied by different interpretations of a mid-teens post-synergy multiple.

The post-synergy EBITDA implied by a given transaction multiple is:

$$
\text{Post-Synergy EBITDA}
=
\frac{\text{Transaction EV}}
{\text{Post-Synergy EV / EBITDA}}
$$

Implied EBITDA synergies are then calculated as:

$$
\text{Implied EBITDA Synergy}
=
\text{Post-Synergy EBITDA}
-
\text{Standalone Rotork EBITDA}
$$

This produces:

| Post-Synergy EV / EBITDA | Implied EBITDA Synergy |
|---:|---:|
| 14.0x | $110m |
| **15.0x** | **$84m** |
| 16.0x | $61m |

I use approximately **$84m** as the base implied EBITDA synergy case.

These values are an analyst interpretation of ABB's transaction language rather than company synergy guidance.

---

## 5. EPS Accretion / Dilution

I built a pro forma EPS bridge combining ABB's standalone earnings, Rotork's earnings contribution, financing drag and potential synergies.

The simplified earnings bridge is:

$$
\text{Pro Forma Net Income}
=
\text{ABB Standalone Net Income}
+
\text{Rotork Net Income}
+
\text{After-Tax Synergies}
-
\text{After-Tax Financing Drag}
$$

Pro forma EPS is then:

$$
\text{Pro Forma EPS}
=
\frac{\text{Pro Forma Net Income}}
{\text{ABB Diluted Shares}}
$$

EPS accretion is calculated as:

$$
\text{EPS Accretion}
=
\frac{\text{Pro Forma EPS}}
{\text{ABB Standalone EPS}}
-1
$$

### FY27E Pro Forma / Run-Rate

FY27E is shown on a **full-year pro forma / run-rate basis**, because the transaction is expected to complete during H1 2027 rather than being owned by ABB for the entire reported year.

- ABB standalone EPS: **$2.95**
- Pro forma EPS: **$3.02**
- EPS accretion: **2.4%**

The base model assumes no EBITDA synergies are realised during FY27E.

### FY28E

FY28E represents the first full post-close year.

- ABB standalone EPS: **$3.10**
- Pro forma EPS before synergies: **$3.17**
- Pro forma EPS after synergies: **$3.21**
- EPS accretion before synergies: **2.4%**
- EPS accretion after synergies: **3.6%**

Importantly, the transaction is already **accretive before synergies** under the model assumptions, so no positive breakeven EBITDA synergy is required.

---

## 6. Sensitivity Analysis

I tested FY28E EPS accretion across different:

- EBITDA synergy outcomes; and
- incremental borrowing rates.

The analysis considers synergy cases ranging from **$0m to $130m** and borrowing costs from **3.5% to 6.5%**.

Across the tested range, modeled FY28E EPS accretion remains positive, ranging from approximately **2.3% to 4.2%**.

The base case of approximately **$84m of synergies and a 4.5% borrowing rate** produces approximately **3.6% FY28E EPS accretion**.

---

## Strategic Rationale

The transaction has several potential strategic benefits for ABB:

- expands ABB's Process Automation portfolio into flow control and electric actuation;
- adds Rotork's installed base and aftermarket exposure across process industries;
- creates potential cross-selling opportunities through ABB's global automation and electrification channels; and
- adds Rotork as a separate division within ABB's Process Automation business.

---

## Key Risks

### Valuation

ABB is paying a substantial acquisition premium, including approximately **73% to Rotork's unaffected share price** and approximately **19.5x 2025A adjusted EBITDA**.

The transaction therefore depends on ABB generating sufficient strategic and financial benefits to justify the entry valuation.

### Synergy Execution

The model's **$61m–$110m synergy range is inferred**, not explicit company guidance.

Actual realised synergies may differ materially from the modeled range.

### Financing

Higher borrowing costs would reduce EPS accretion, although the modeled transaction remains accretive across the borrowing-rate sensitivity tested.

### Closing & Integration

Court, regulatory and other closing conditions remain relevant until completion. Post-close integration and execution may also affect the economic outcome.

---

## Model Structure

The Excel model contains six schedules:

1. **Transaction Summary** — deal terms, valuation, rationale and risks
2. **ABB Financials** — acquirer standalone financials and forecasts
3. **Rotork Financials** — target standalone financials and forecasts
4. **Transaction & Financing** — purchase price, EV bridge, transaction multiples, synergies and sources & uses
5. **Accretion-Dilution** — pro forma EPS analysis
6. **Sensitivity & Sources** — EPS sensitivity and source documentation

---

## Key Takeaways

The transaction implies approximately **$5.50bn of enterprise value** and values Rotork at approximately **19.5x 2025A adjusted EBITDA**, reflecting a significant acquisition premium.

Despite the high entry valuation, the modeled transaction is accretive to ABB EPS before synergies because Rotork's earnings contribution exceeds the after-tax financing drag.

A 15.0x post-synergy EV / EBITDA interpretation implies approximately **$84m of EBITDA synergies**, increasing modeled FY28E EPS accretion from approximately **2.4% pre-synergy to 3.6% post-synergy**.

The analysis therefore highlights the interaction between **purchase price, financing structure, target earnings and synergy realisation** in determining acquisition economics.

---

## Limitations

This model is intended as a transaction-analysis exercise rather than a full purchase-accounting model.

It does not include:

- purchase-price allocation or incremental amortisation;
- integration and restructuring costs;
- dividend effects;
- changes in diluted share count; or
- detailed post-close accounting adjustments.

FY27E and FY28E standalone forecasts use analyst growth assumptions and are not company guidance.

---

## Sources

The workbook contains a full source log covering:

- ABB's acquisition announcement;
- the Rotork Scheme Document;
- transaction meeting results;
- Rotork H1 2026 and FY2025 results;
- ABB Q2 2026 and FY2025 financial reporting;
- Robotics disposal proceeds; and
- transaction-date GBP/USD FX.

Analyst assumptions are explicitly identified separately from company-disclosed information.

---

## Disclaimer

This project is independent analysis prepared for educational and portfolio purposes using publicly available information. It does not constitute investment advice.
