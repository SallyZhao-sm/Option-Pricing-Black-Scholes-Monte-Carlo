# Option Pricing with Black–Scholes and Monte Carlo Simulation

## Overview

This project implements analytical and simulation-based methods for pricing European and barrier options. It compares the Black–Scholes formula with one-step and multi-step Monte Carlo simulation to evaluate pricing accuracy, computational efficiency, convergence, and path dependence.

## Instruments

- European call and put options
- Up-and-in barrier options with a barrier level of $110

## Methodology

- Calculated European option values using the Black–Scholes closed-form formula
- Simulated terminal asset prices with one-step Monte Carlo
- Simulated complete price paths with multi-step Monte Carlo
- Checked whether simulated paths crossed the barrier before expiration
- Tested price sensitivity to volatility
- Measured Monte Carlo convergence toward Black–Scholes values

## Key Results

- One-step Monte Carlo converged closely to Black–Scholes prices for European options.
- Approximately 30,000 call paths and 700,000 put paths were required to match the analytical values within cents in the tested setup.
- Multi-step simulation was less efficient for vanilla European options but necessary for path-dependent barrier options.
- Barrier option values remained below the corresponding vanilla option values because payoff requires barrier activation.
- Higher volatility increased the probability of crossing the barrier and raised the option values in the tested scenarios.

## Technologies

Python, NumPy, SciPy, Monte Carlo simulation, Black–Scholes modeling, stochastic processes, sensitivity analysis
