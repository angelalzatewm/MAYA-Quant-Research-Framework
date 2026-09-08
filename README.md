# MAYA - Quantitative Research Infrastructure
## Architecture, Research Methodology & HANNA Live Lifecycle

**Version 2.0 | Research methodology blueprint**

## 1. Executive philosophy

MAYA is not a single trading robot and does not guarantee profitability. It is a controlled research laboratory designed to move market observations through increasingly strict evidence gates:

```text
Does a pattern exist?
↓
Is it statistically defensible?
↓
Does it survive temporal separation?
↓
Is it economically exploitable?
↓
Can it become an executable rule?
↓
Does it survive true OOS?
↓
Can it operate live under controlled risk and adaptation?
```

## 2. Complete lifecycle

```text
MARKET
  ↓
MAYA COLLECTOR
  ↓
EDA-LITE - DISCOVERY / CALIBRATION
  ↓
STRONG_CANDIDATE
  ↓
MAYA CORE - STRICT VALIDATION / CERTIFICATION
  ↓
OOS_ELIGIBLE
  ↓
MAYA HUNTER - TRUE OOS
  ↓
OOS APPROVED INDIVIDUAL
  ↓
HANNA - LIVE MANAGEMENT / EXECUTION / MONITORING
  ↓
REAL CAPITAL + NEW INFORMATION
  ↓
CONTROLLED RESEARCH TRIGGER
  ↺ MAYA RESEARCH CYCLE
```

| Layer | Main question | Output |
|---|---|---|
| Collector | What happened in the market? | Structured event data |
| EDA-Lite | Where might an edge exist? | Candidate / Strong Candidate |
| Core | Can the candidate survive strict validation? | Certified / OOS Eligible |
| Hunter | What happens on unseen data? | OOS evidence |
| HANNA | How does an approved individual operate and evolve safely? | Live individual state |

## 3. MAYA Collector

Collector is the evidence factory. It captures event timing, fixing/range context, decision-time features, volatility and structural variables, MFE/MAE first-touch behavior and data quality. It does not certify a strategy.

**Mental model:** Collector is the scientist collecting samples.

## 4. EDA-Lite

EDA-Lite is the prospecting layer. It is lighter than Core in model/search complexity, not lighter in causal or temporal discipline.

```text
CSV → Data Quality → Fast Screen → Event Labeling → EDA
    → WFO-Lite → RF-Lite → Monte Carlo → Robustness
    → Barrier-Theoretical Economics → Surrogate → Registry
```

Its purpose is to reduce the research universe and identify candidates that deserve deeper validation. A `STRONG_CANDIDATE` is **not** a production approval.

## 5. MAYA Core

Core receives a frozen candidate artifact, not merely a performance score. It revalidates the candidate under a stricter protocol and decides whether the candidate is defensible under MAYA's certification rules.

**Certification means:** the candidate satisfied the declared research protocol. It does not mean guaranteed future profitability.

## 6. MAYA Hunter

Hunter receives an OOS-eligible candidate and evaluates it on genuinely unseen data. The frozen rule/model becomes evidence, not a tuning set. Hunter should execute, measure and report; it should not silently optimize the candidate.

## 7. HANNA - the live individual layer

After a candidate passes Core and Hunter, it becomes an approved operational individual. HANNA manages a population of such individuals.

Example:

```text
HANNA_001
Asset: XAUUSD
Profile: PRE_ASIA
Candidate: XU_PRE_ASIA_BARRIER15_0042
Model: MODEL_v001
Core certificate: CORE_CERT_0042
Hunter OOS: PASSED
Status: LIVE
```

HANNA is not simply a bot. It is the live lifecycle manager for approved quantitative individuals.

## 8. HANNA philosophy: adaptive, but governed

The key rule is:

> **HANNA may learn from new information, but HANNA may not certify itself.**

Live information can trigger research, but a structural model/rule change must return to the MAYA research cycle:

```text
HANNA observes
   ↓
Detects drift / degradation / new evidence
   ↓
Research trigger
   ↓
EDA-Lite → Core → Hunter
   ↓
New approved version
   ↓
HANNA deploys the new version
```

A live loss must not automatically rewrite the strategy.

## 9. OOS versioning

OOS belongs to a specific model version. For example:

```text
MODEL_v001
Train: 2016–2022
Internal validation: 2023
True OOS: 2024–2026

MODEL_v002
May use 2024–2026 as research data
Therefore it requires a new validation boundary and future OOS period
```

Using live OOS data to research a new model means those observations are no longer unseen for that new version.

## 10. Signal vs meta-labeling vs sizing

The primary predictive model and capital allocation should be separate layers:

```text
Primary model
   ↓
Side / trade decision
   ↓
Optional meta-label model
   ↓
Probability / confidence
   ↓
Bet sizing
   ↓
Risk limits
   ↓
Execution
```

Meta-labeling is a future research extension for estimating whether to take a primary signal and/or how aggressively to size it. Kelly or fractional Kelly belongs to the sizing layer, not to the proof of alpha. D'Alembert-type progression rules are money-management experiments, not evidence of edge.

## 11. Performance is multidimensional

MAYA/HANNA should not be reduced to maximizing a single backtest metric. Separate:

- **Statistical:** MCC, PR-AUC, calibration.
- **Economic:** expectancy, profit factor, cost-adjusted return.
- **Risk:** drawdown, Sharpe, Sortino, CVaR.
- **Robustness:** fold/year/regime stability.
- **Selection control:** Monte Carlo, multiple-testing record, DSR context.
- **Operations:** spread, slippage, latency, fill quality.

Deflated Sharpe Ratio is a supporting selection-aware metric, not a replacement for WFO, Monte Carlo, economic validation or true OOS.

## 12. The research feedback loop

```text
RESEARCH FACTORY
Collector → EDA-Lite → Core → Hunter
                         ↓
                 Approved Individual
                         ↓
                       HANNA
                         ↓
                  Live Capital
                         ↓
               New Evidence / Monitoring
                         ↓
                  Research Trigger
                         ↓
                      Collector ↺
```

This is a controlled feedback loop, not uncontrolled self-modification.

## 13. The four levels of edge

1. **Statistical edge** - predictive relationship under the stated protocol.
2. **Economic edge** - positive economic value after declared costs.
3. **Executable edge** - deterministic, auditable implementation.
4. **Live edge** - acceptable behavior under live conditions.

A candidate may pass one level and fail another. A live failure can be valuable evidence that persistence did not hold.

## 14. Final philosophy

> **MAYA discovers, challenges, validates and tests. HANNA deploys, manages, monitors and controls the live lifecycle. Neither layer is allowed to bypass the governance that protects research integrity.**

## 15. Next architectural contract

The next formal interface to define is the **OOS Approved Individual Contract** between Hunter and HANNA. It should specify: identity, candidate/model version, feature contract, rule hash, Core certificate, Hunter evidence, risk constraints, execution constraints and permitted live adaptations.
