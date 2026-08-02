# Week 2 - Day 2: Probability & Distributions

## Overview
Core probability concepts and common distributions that underpin how ML models reason about uncertainty.

## Topics Covered
- Probability basics (favorable / total outcomes)
- Core rules: complement, addition, multiplication
- Conditional probability P(A|B)
- Bayes' theorem: prior, likelihood, posterior
- Common distributions: normal, binomial, uniform

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`)

## What Was Done
- Simulated 10,000 coin flips to confirm empirical probability converges to 0.5 (Law of Large Numbers)
- Sampled from a normal distribution and visualized the bell-shaped histogram
- Computed P(IMDB_Rating >= 8.5 | Genre contains Drama) directly from the dataset
- Verified the conditional probability result via random-sampling simulation

## Key Takeaway
Conditional probability answers "given this evidence, how likely is this outcome?" - the same question every predictive model is implicitly answering. Simulation is a reliable way to sanity-check a probability calculated by hand.

## Files
- `day2_probability_distributions.ipynb`
