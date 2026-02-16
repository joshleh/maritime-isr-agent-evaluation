# Maritime ISR Agent Evaluation

Benchmarking LLM agent strategies for maritime ISR allocation against classical optimization baselines using real AIS vessel data.

---

## Overview

This project builds a simulation and evaluation framework for maritime Intelligence, Surveillance, and Reconnaissance (ISR) tasking under uncertainty.

Using real AIS vessel trajectory data from MarineCadastre, the system models vessel movement patterns and evaluates different planning strategies for allocating limited ISR assets.

The core objective is to measure the effectiveness of LLM-based agent strategies relative to classical optimization methods in a controlled wargaming-style environment.

---

## Problem Statement

Given:
- A maritime operating region
- Historical AIS-derived vessel movement priors
- A limited fleet of ISR assets
- Operational constraints (range, endurance, coverage)

Determine:
An allocation strategy that maximizes detection probability and coverage efficiency under uncertainty.

---

## System Architecture

The framework consists of four components:

1. **Simulation Environment**
   - AIS-derived vessel movement modeling
   - Scenario generation
   - Monte Carlo sampling

2. **Classical Optimization Baselines**
   - Greedy allocation
   - Linear / mixed-integer optimization
   - Constraint-based tasking

3. **LLM Agent Graph**
   - Strategy generation agent
   - Geospatial analysis tools
   - Optimization tool-calling
   - Plan revision loop

4. **Evaluation Harness**
   - Scenario benchmarking
   - Performance metrics:
     - Coverage %
     - Detection probability
     - Resource efficiency
     - Robustness under adversarial variation
   - Statistical comparison (LLM vs baselines)

---

## Data

- Source: MarineCadastre AIS dataset (NOAA/BOEM)
- Region: [To be defined]
- Subset: Filtered temporal window for tractable experimentation
- Derived Features:
  - Vessel density heatmaps
  - Movement velocity distributions
  - Chokepoint likelihood modeling

---

## Research Questions

1. Can LLM-based agents generate competitive ISR allocation strategies relative to classical optimizers?
2. Does tool-augmented prompting improve planning performance?
3. Under what scenario complexity does LLM performance degrade?
4. How sensitive are strategies to uncertainty in vessel movement priors?

---

## Current Status

- [ ] AIS preprocessing pipeline
- [ ] Simulation environment
- [ ] Optimization baselines
- [ ] Agent graph prototype
- [ ] Evaluation tooling
- [ ] Benchmark results

---

## Repository Structure

```text
maritime-isr-agent-evaluation/
│
├── simulation/        # Scenario generation and vessel movement modeling
├── optimizer/         # Classical optimization baselines (greedy, LP/MIP)
├── agent_graph/       # LLM agent architecture and tool-calling logic
├── evaluation/        # Metrics, benchmarking, statistical comparison
├── data_processing/   # AIS preprocessing and feature extraction
├── experiments/       # Reproducible experiment configs and results
└── README.md
```

---

## Disclaimer

This project is a research prototype exploring evaluation methodologies for AI-enabled planning systems. It does not represent real operational systems.
