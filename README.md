# Fermi Paradox Visualizer

Interactive visualization of why we haven't detected other civilizations.

## What it does

Calculates probability of civilizations existing simultaneously in our galaxy based on:
- Stars with habitable planets
- Probability of life emerging
- Probability of intelligence evolving
- Lifespan of detectable civilizations
- Galaxy age

## Core formulas

```
totalCivs = galaxyStars × habitablePlanets × life × intelligence
concurrent = totalCivs × (civilizationWindow / galaxyAge)
distance = galaxyDiameter / ∛concurrent
P(contact) = ourSignalRadius / distance
```

## Key insight

Even with millions of civilizations throughout galaxy history, very few exist *at the same time*. And those that do are typically tens of thousands of light-years apart.

Our radio signals have traveled only ~100 light-years since the 1920s.

## Usage

Open `index.html` in browser. Adjust sliders or use presets (Pessimistic / Baseline / Optimistic).

## Files

- `index.html` — main visualization (self-contained, no dependencies)