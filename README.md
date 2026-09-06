# MAYA — Quantitative Research Infrastructure

> **Research in Progress · Public Blueprint · Not a production trading system**

MAYA is a modular quantitative research infrastructure designed to transform structured market observations into systematically evaluated trading hypotheses.

The project is organized as a research pipeline rather than as a single trading strategy:

```text
Market Data
    │
    ▼
┌─────────────────────┐
│ MAYA COLLECTOR      │
│ Data + Feature Eng. │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ EDA-LITE            │
│ Discovery / Triage  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ MAYA CORE           │
│ Rigorous Validation │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ MAYA HUNTER         │
│ True OOS / Execution│
└─────────────────────┘
```

## Why MAYA?

The central research question is not:

> "Can I make a backtest look profitable?"

It is:

> **"Can an apparent trading edge survive increasingly strict tests for causality, temporal separation, statistical significance, economic viability and out-of-sample execution?"**

MAYA is being built to answer that question in stages.

## Current status

| Component | Status |
|---|---|
| MAYA Collector | Research implementation |
| EDA-Lite | **Calibration / methodological refinement** |
| MAYA Core | Validation architecture in development |
| MAYA Hunter | Experimental OOS execution layer |
| Production deployment | **Not production-ready** |

The current EDA-Lite implementation already includes Collector schema grounding, event-based labeling, dynamic WFO purging, pooled WFO Monte Carlo, robustness checks, economic evaluation, surrogate extraction and a candidate registry. The public project will continue to evolve as the methodology is audited and hardened. 

## Repository vision

The repository is intended to document and eventually host the full development lifecycle of MAYA:

```text
maya-quant-research-framework/
│
├── README.md
├── docs/
│   ├── architecture.md
│   ├── maya-explained.md
│   ├── methodology.md
│   ├── roadmap.md
│   ├── status.md
│   ├── data-contracts.md
│   ├── research-governance.md
│   ├── risk-and-limitations.md
│   └── research-plan.md
│
├── collector/
├── eda_lite/
├── maya_core/
├── maya_hunter/
├── examples/
├── tests/
└── configs/
```

## Research principles

- No future information in model inputs.
- Temporal separation between discovery, validation and true OOS.
- Event-based labels and dynamic purge logic.
- Statistical evidence is separated from economic performance.
- Discovery is separated from certification.
- Reproducibility and traceability are first-class concerns.
- A candidate is never treated as a production strategy merely because it performs well in one backtest.

## Important disclaimer

MAYA is a research and engineering project. Nothing in this repository should be interpreted as a guarantee of profitability, investment advice or evidence that any trading strategy will remain profitable in the future.

## Project direction

The long-term objective is to evolve MAYA from a research framework into a reproducible quantitative research infrastructure capable of:

1. collecting structured market events;
2. discovering candidate hypotheses;
3. validating candidates under strict research controls;
4. translating validated candidates into executable rules;
5. evaluating those rules in true out-of-sample conditions;
6. supporting future monitoring and production research workflows.

See:

- [`docs/architecture.md`](docs/architecture.md)
- [`docs/maya-explained.md`](docs/maya-explained.md)
- [`docs/methodology.md`](docs/methodology.md)
- [`docs/roadmap.md`](docs/roadmap.md)
- [`docs/status.md`](docs/status.md)
