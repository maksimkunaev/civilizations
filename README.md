# 🌌 Fermi Paradox Visualizer

**Where is everybody?**

In 1950, physicist Enrico Fermi asked this simple question over lunch. Given the billions of stars in our galaxy, many older than our Sun — where are all the alien civilizations? Why the silence?

This interactive visualization lets you explore one possible answer: **they may exist, but the universe is just too big and time is too short.**

The probability is very low — **but it's not necessarily zero.**

## 🚀 Demo

**[→ Try it live](https://maksimkunaev.github.io/civilizations/)**

## What This Shows

Play with the parameters and watch the galaxy respond:

- **Civilizations right now** — not throughout history, but existing *at this very moment*
- **Distance to nearest neighbor** — we can see how far it is 
- **Contact probability** — our chance of hearing from anyone in the next 100 years

Even if millions of civilizations have existed throughout the galaxy's 13 billion year history, only a handful exist *simultaneously*. And they're scattered across 100,000 light-years.

Our radio signals have traveled just ~100 light-years since the 1920s. A tiny bubble in an ocean of silence.

## How It Works

Based on a simplified Drake Equation model:

```
totalCivs     = stars × habitablePlanets × life × intelligence
concurrent    = totalCivs × (civilizationWindow / galaxyAge)  
distance      = galaxyDiameter / ∛concurrent
P(contact)    = signalRadius / distance
```

## ⚠️ Disclaimer

**This is a thought experiment, not a scientific claim.**

The parameters (probability of life, intelligence, civilization lifespan) are fundamentally uncertain — estimates vary by 10+ orders of magnitude.

This tool is for building intuition about cosmic scale and time, not for making predictions. For rigorous treatment of these uncertainties, see Sandberg et al. *"Dissolving the Fermi Paradox"* (2018).

## 📁 Files

- `index.html` — self-contained visualization, no dependencies

## 📋 TODO

### High Priority (Scientific Accuracy)
- Add separate filter for multicellular life emergence (happens after simple life)
- Split "intelligence" into cognitive ability vs tool-using capability
- Add parameter for % of intelligent species that develop detectable technology
- Replace single "civilization window" with distribution (min/avg/max lifespan)
- Weight star formation history (most habitable planets formed ~5B years ago, not uniformly)
- Add galactic habitable zone filter (exclude galactic center due to radiation)
- Add metallicity requirement filter (early universe stars couldn't support rocky planets)

### Medium Priority (Detection Model)
- Replace distance-based contact probability with signal strength model (inverse square law)
- Add "broadcasting vs listening" asymmetry (civilizations might detect without transmitting)
- Add detection threshold parameter (minimum signal strength we can detect)
- Show detection probability separately for radio, optical, infrared
- Add Kardashev scale consideration (Type II/III civs would be easier to detect)

### Low Priority (UX/Features)
- Add "Advanced Mode" toggle to show/hide additional parameters
- Add uncertainty ranges to all calculations (show min/max bounds)
- Add comparison to published estimates (SETI, Sandberg et al., etc.)
- Add timeline view showing when civilizations might have existed
- Add export functionality (save parameters/screenshot)
- Add educational tooltips explaining each filter
- Add references/citations panel

### Nice to Have
- Add self-destruction probability parameter
- Model directed panspermia scenarios
- Add relativistic travel time calculations
- Show communication lag time for two-way conversation