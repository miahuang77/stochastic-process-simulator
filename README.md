# Stochastic Process Simulator

## An Exploration of Stochastic Processes and Their Limitations in Financial Markets

---

## Overview

This project is a progressive implementation of stochastic processes in financial modelling.

The project first documented how randomness is represented mathematically through random walks, Brownian motion, and Geometric Brownian Motion (GBM). While these models provide theoretical foundations for asset price dynamics, empirical analysis reveals significant discrepancies between their assumptions and observed market behavior.

In particular, financial returns exhibit volatility clustering, heavy tails, and time-varying risk, phenomena that are inconsistent with the constant-volatility assumption of GBM.

This observation motivates a transition toward more sophisticated models that can capture time-varying volatility. In particular, the presence of volatility clustering suggests that volatility itself follows a dynamic process rather than remaining constant through time. This insight motivates the following projects to introduce the ARCH/GARCH family of models.

If the notebooks can not render properly, visit:
- [Random Walk](https://miahuang77.github.io/stochastic-process-simulator/01_random_walk.html)
- [Brownian Motion](https://miahuang77.github.io/stochastic-process-simulator/02_brownian_motion.html)
- [Geometric Brownian Motion](https://miahuang77.github.io/stochastic-process-simulator/03_geometric_brownian_motion.html)

---

## Project Structure

### 1. Random Walk

The discrete random walk serves as the conceptual foundation for continuous-time stochastic processes.

- Definition and Visualization
- Mean and Variance
- Distribution (Possibility Mass Function)

---

### 2. Brownian Motion

As the time intervals between steps shrink toward zero, the random walk converges to Brownian Motion (Wiener Process). Brownian Motion is described as the continuous-time limit of random walks.

- Definition and Visualization
- Brownian Motion vs. Random Walk
- Properties of Random Walk

---

### 3. Geometric Brownian Motion (GBM)

Brownian Motion alone can take negative values and is therefore unsuitable for modeling asset prices. We introduced Geometric Brownian Motion:
dS_t = μS_t dt + σS_t dW_t

Topics explored:

- Definition and Visualization
- Comparison with Real Stock Data

---

## Empirical Investigation: Why GBM Fails

A key component of the third part (GBM) is the comparison between simulated GBM paths and real S&P500 data.

Several factors that may explain why the GBM model does not fully capture real market behavior:

### Volatility Clustering

In the real financial market, large price movements tend to be followed by large price movements, while calm periods tend to remain calm.

This phenomenon is inconsistent with the constant-volatility assumption embedded in GBM.

### Heavy-Tailed Returns

Extreme market events occur more frequently than predicted by the normal distribution implied by GBM.

### Jumps

GBM assumes that prices evolve continuously through Brownian motion. In reality, markets occasionally experience abrupt discontinuous movements caused by earnings announcements, macroeconomic news, geopolitical events, or financial crises.

---

## Future Directions

Planned extensions include:

### Volatility Clustering

Implementation of:

- ARCH
- GARCH

### Stochastic Volatility Models

Exploration of:

- Mean-reverting: Ornstein-Uhlenbeck Process
- Heston models

---

## Key Takeaway

This repository documents that progression from foundational stochastic processes toward modern volatility modeling.

The primary lesson from this project is that financial markets cannot be fully understood through a single stochastic process.

Random walks, Brownian motion, and GBM provide essential theoretical foundations, but empirical evidence reveals systematic departures from their assumptions.
