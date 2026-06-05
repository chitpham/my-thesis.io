# CfDs and PPAs: How contracts shape spot market outcomes
**Master's Thesis — Aalto University — 2026 // Chi Pham**

## Overview
This repository contains the theoretical model, calibration code, and interactive results dashboard for my master's thesis studying how forward contracts (PPA and CfD) affect strategic bidding behaviour and equilibrium spot prices in electricity markets.

🔗 [View interactive dashboard](https://chitpham.github.io/thesis-dashboard)

## Research Question
How does allocation of forward contract affect spot price through firms’ bidding strategy? And whether CfDs or PPAs outperform another in the sense of reducing spot price?

## Repository Structure
- `docs/` — interactive dashboard (Chart.js, HTML)
- `code/` — calibration and simulation scripts (Python/R)
- `data/` — cleaned dataset used for calibration

## Data
Raw market data sourced from [Elexon / your source].
Not included due to licensing — available upon request.
Cleaned and simulation result data are provided in `data/`.

## Key Findings
1. Bidding is decreasing in contract coverage f — but only up to a threshold f* that varies with renewable output r
2. No-arbitrage PPA leaves market outcomes unchanged; CfD retains a price effect upon coverage level
3. Contract price-suppressing effects are least visible in winter due to nature of high demand and renewable source scarcity. 

## Methods
- Theoretical model: uniform single-step auction with privately known and stochastic renewable availability.
- Calibration: UK electricity day-ahead market data, 2024
- Simulation: Hourly spot prices are simulated by drawing renewable output r from a calibrated seasonal distribution, computing the equilibrium bid function for each hour given observed (and calibrated) market demand, marginal cost, thermal capacity. This is repeated across different values of contract coverage f to generate prices under each scenario.
