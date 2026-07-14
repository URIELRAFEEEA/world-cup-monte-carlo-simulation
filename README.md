# Dynamic Monte Carlo Simulation of World Cup Tournament Outcomes

## Overview

This project explores how stochastic processes, probability theory and Monte Carlo simulation can be used to model FIFA World Cup knockout tournaments.

The aim is not to predict football outcomes with certainty, but rather to investigate how latent team strength and randomness interact within a high-variance competitive system.

The project develops from a static tournament model into a dynamic framework where team strength estimates are updated as new information becomes available during the tournament.

---

# Mathematical Framework

Each team is represented through a latent strength parameter based on football quality across different dimensions such as:

- Attacking ability
- Defensive stability
- Midfield control

Match outcomes are simulated using a logistic probability model:

\[
P(i \text{ wins}) =
\frac{1}{1+\exp(-\Delta_{ij}/\sigma)}
\]

where:

- \( \Delta_{ij} \) represents the difference in latent strength between teams.
- \( \sigma \) represents tournament volatility.

Higher volatility allows greater uncertainty, while lower volatility allows strength differences to dominate outcomes.

---

# Methods

The model uses:

- Monte Carlo simulation
- Logistic probability modelling
- Markov chain representation of knockout tournaments
- Absorbing state processes
- Dynamic updating of latent strengths
- R programming

---

# Simulation Framework

The tournament is represented as a stochastic process:

\[
32 \rightarrow 16 \rightarrow 8 \rightarrow 4 \rightarrow 2 \rightarrow 1
\]

Each simulation represents one possible tournament path.

Thousands of tournament realizations are generated to estimate the empirical probability distribution of possible champions.

---

# Dynamic Updating

The updated version introduces information-based updating.

As the tournament progresses, new information enters the filtration:

- Match results
- Defensive performances
- Tactical observations
- Player availability
- Tournament momentum

The latent strength of each team is therefore allowed to evolve:

\[
S_i(t+1)=S_i(t)+U_i(t)
\]

where \(U_i(t)\) represents the adjustment after incorporating new information.

---

# Repository Contents
