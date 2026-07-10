# Monte Carlo Simulation of World Cup Tournament Outcomes

## Overview
This project explores how stochastic processes and Monte Carlo simulation can be used to model FIFA World Cup knockout tournaments. Rather than predicting real tournament outcomes, it demonstrates how latent team strength and randomness interact in high-variance competitive systems.

## Mathematical Model
Each team is assigned a latent strength score based on attacking, defensive and midfield quality.

Match outcomes are simulated using a logistic probability model

P(i beats j)=1/(1+exp(-Δ/σ))

where Δ represents the difference in latent strength and σ controls tournament volatility.

## Simulation
- 10,000 Monte Carlo simulations
- Knockout tournament represented as an absorbing Markov process
- Implemented in R

## Results
Example championship probabilities:

France .......... 59%
Argentina ....... 21%
Spain ........... 13%
Portugal ........ 3%

The simulations illustrate that even highly rated teams remain vulnerable to randomness.

## Repository Contents

- World Cup Simulation.qmd
- World-Cup-Simulation2.pdf

## Skills Demonstrated

- Monte Carlo simulation
- Statistical modelling
- Stochastic processes
- Markov chains
- Probability theory
- R
