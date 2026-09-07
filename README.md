# ABB / Rotork: M&A Transaction Analysis

## Overview

Independent transaction analysis of ABB's recommended all-cash acquisition of Rotork plc.

The model covers:

- offer mechanics and acquisition premium
- equity purchase price and enterprise value
- transaction multiples
- sources & uses and acquisition financing
- implied EBITDA synergies
- EPS accretion / dilution
- synergy and borrowing-cost sensitivities

The objective was to model how announced deal terms translate into purchase price, financing requirements and pro forma shareholder impact.

---

## Transaction Overview

| Metric | Value |
|---|---:|
| Cash consideration | 503p/share |
| Permitted dividend | Up to 3p/share |
| Total potential shareholder value | 506p/share |
| Premium to unaffected price | 73.0% |
| Premium to 3-month VWAP | 62.7% |
| Implied equity purchase price | $5.57bn |
| Implied enterprise value | $5.50bn |
| EV / 2025A Sales | 5.25x |
| EV / 2025A Adjusted EBITDA | 19.5x |
| Expected completion | H1 2027 |

---

## Purchase Price & Enterprise Value

I translated the announced 503p/share offer into an implied equity purchase price using Rotork's fully diluted share count.

`Equity purchase price = Offer price × Fully diluted shares`

This gives approximately **£4.14bn**, or **$5.57bn** at the transaction-date GBP/USD exchange rate.

I then bridged equity value to enterprise value using cash, debt, leases and pension adjustments, producing approximately **$5.50bn of enterprise value**, consistent with the disclosed transaction value.

---

## Financing & Sources and Uses

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

The transaction requires approximately **$359m of incremental borrowing** after applying the Robotics disposal proceeds and $500m of ABB cash.

Base financing assumptions include:

- **4.5%** incremental borrowing rate
- **3.5%** foregone yield on cash used
- approximately **$24.9m** annual after-tax financing drag

Sources and uses reconcile to zero.

---

## Implied Synergy Analysis

ABB described the transaction using a post-synergy EV / EBITDA multiple in the **mid-teens**, but did not provide a specific EBITDA synergy target in the transaction materials used for the model.

I therefore reverse-engineered the synergy level implied by different post-synergy multiples.

`Implied synergy = Transaction EV / Post-synergy multiple − Standalone EBITDA`

| Post-Synergy EV / EBITDA | Implied EBITDA Synergy |
|---:|---:|
| 14.0x | $110m |
| **15.0x** | **$84m** |
| 16.0x | $61m |

The base case uses approximately **$84m of implied EBITDA synergies**.

These are analyst estimates inferred from ABB's transaction language rather than company synergy guidance.

---

## EPS Accretion / Dilution

I built a pro forma earnings bridge combining ABB's standalone earnings, Rotork's earnings contribution, financing drag and potential synergies.

`Pro forma net income = ABB net income + Rotork net income + after-tax synergies − financing drag`

`Pro forma EPS = Pro forma net income / ABB diluted shares`

`EPS accretion = Pro forma EPS / ABB standalone EPS − 1`

### FY27E Pro Forma / Run-Rate

FY27E is presented on a **full-year pro forma / run-rate basis** because completion is expected during H1 2027.

| Metric | FY27E |
|---|---:|
| ABB standalone EPS | $2.95 |
| Pro forma EPS | $3.02 |
| **EPS accretion** | **2.4%** |

No EBITDA synergies are assumed in the FY27E base case.

### FY28E

FY28E represents the first full post-close year.

| Metric | FY28E |
|---|---:|
| ABB standalone EPS | $3.10 |
| Pro forma EPS before synergies | $3.17 |
| Pro forma EPS after synergies | $3.21 |
| Accretion before synergies | 2.4% |
| **Accretion after synergies** | **3.6%** |

The modeled transaction is **accretive before synergies**, meaning no positive breakeven EBITDA synergy is required.

---

## Sensitivity Analysis

FY28E EPS accretion is tested across:

- EBITDA synergies of **$0m–$130m**
- borrowing rates of **3.5%–6.5%**

Across the tested range, modeled accretion remains positive at approximately **2.3%–4.2%**.

The base case of **$84m synergies** and a **4.5% borrowing rate** produces approximately **3.6% FY28E EPS accretion**.

---

## Strategic Rationale

The transaction potentially:

- expands ABB's Process Automation portfolio into flow control and electric actuation
- adds Rotork's installed base and aftermarket exposure
- creates cross-selling opportunities through ABB's global platform
- strengthens ABB's exposure to process-industry automation

---

## Key Risks

**Valuation**  
ABB is paying a **73% premium** to Rotork's unaffected share price and approximately **19.5x 2025A adjusted EBITDA**.

**Synergy execution**  
The modeled **$61m–$110m synergy range is inferred**, not explicit company guidance.

**Financing**  
Higher borrowing costs reduce accretion, although the transaction remains accretive across the modeled range.

**Execution**  
Closing conditions, integration and post-close execution may affect the realised economics of the transaction.

---

## Model Structure

The Excel workbook contains:

1. **Transaction Summary** — deal terms, valuation, rationale and risks
2. **ABB Financials** — acquirer standalone financials
3. **Rotork Financials** — target standalone financials
4. **Transaction & Financing** — purchase price, EV bridge, sources & uses and synergies
5. **Accretion-Dilution** — pro forma EPS analysis
6. **Sensitivity & Sources** — sensitivity analysis and source documentation

---

## Key Takeaways

- ABB's offer implies approximately **$5.50bn of enterprise value**
- Rotork is valued at approximately **19.5x 2025A adjusted EBITDA**
- the modeled transaction is **2.4% accretive before synergies**
- a 15.0x post-synergy multiple implies approximately **$84m of EBITDA synergies**
- modeled FY28E accretion rises to approximately **3.6%** in the base synergy case

The analysis highlights how **purchase price, financing structure, target earnings and synergy realisation** interact to determine acquisition economics.

---

## Limitations

The model is a transaction-analysis exercise rather than a full purchase-accounting model.

It excludes:

- purchase-price allocation and incremental amortisation
- integration and restructuring costs
- detailed tax and purchase-accounting adjustments
- dividend effects
- changes in diluted share count

FY27E and FY28E standalone forecasts use analyst assumptions and are not company guidance.

---

## Sources

The workbook includes a full source log covering ABB and Rotork company disclosures, transaction documents, financial results, Robotics disposal proceeds and transaction-date FX.

Company-disclosed information and analyst assumptions are identified separately.
