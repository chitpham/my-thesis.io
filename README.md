# CfDs and PPAs: How contracts shape spot market outcomes
**Master's Thesis — Aalto University — 2026**

## Overview
This repository contains the results dashboard for my master's thesis studying how forward contracts (PPAs and CfDs) affect bidding behaviour and equilibrium spot prices in electricity wholesale markets. 

🔗 [View dashboard](https://chitpham.github.io/thesis-dashboard)

## Research Question
How does allocation of forward contract affect spot price through firms’ bidding strategy? And whether one contract type outperforms in the sense of reducing spot price?

## Repository Structure
- `docs/` — dashboard
- `code/` — calibration and simulation scripts (Python) (to be updated upon completion)
- `data/` — cleaned dataset used for calibration (to be updated upon completion)

## Data
Raw market data sourced from public data of Elexon and UK NESO.

## Key Findings
1. Bidding is decreasing in contract coverage f for explictly small/large renewble capacity relative to thermal.
2. No-arbitrage PPAs leaves market outcomes unchanged; CfDs retains a price effect upon coverage level. 
3. Contract price-suppressing effects are least visible in winter due to nature of high demand and renewable source scarcity. 

## Methods
- Theoretical model: uniform single-step auction with privately known and stochastic renewable availability.
- Calibration: UK electricity day-ahead market data, 2024
- Simulation: Hourly spot prices are simulated by drawing renewable output r from a calibrated seasonal distribution, computing the equilibrium bid function for each hour given observed (and calibrated) market demand, marginal cost, thermal capacity. This is repeated across different values of contract coverage f to generate prices under each scenario.

## Contact
Author: Chi Pham 
