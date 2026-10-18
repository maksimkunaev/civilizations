# Fermi Paradox Visualizer

An interactive, single-file visualization of how many alien civilizations might
exist right now, how far away the nearest one would be, and our odds of
hearing from it.

**[Try it live](https://maksimkunaev.github.io/civilizations/)**

<!-- Add a screenshot or GIF here: docs/screenshot.png -->

**Where is everybody?** In 1950, physicist Enrico Fermi asked this over lunch.
Given the billions of stars in our galaxy, many older than our Sun, where are
all the alien civilizations? This visualization explores one possible answer:
they may exist, but the universe is too big and time is too short. The
probability is very low, but not necessarily zero.

## What it does

- Five sliders: stars with habitable planets, chance life emerges, chance
  intelligence evolves, civilization window (how long a civilization lasts),
  and galaxy age.
- Pessimistic / Baseline / Optimistic presets.
- Shows **civilizations right now** (not throughout history, but existing at
  this moment), **distance to the nearest neighbor**, signal travel time, and
  **contact probability** (our chance of hearing from anyone in the next 100
  years).
- Draws a spiral-galaxy starfield on a canvas (3,000 dots, ~66.7M stars per
  dot) with planets where life may emerge and current civilizations highlighted
  (up to 100 shown), plus a marker for our own position.
- Breakdown stats: planets in the habitable zone, planets where life may
  emerge, technological civilizations ever, and temporal overlap chance.

Even if millions of civilizations have existed over the galaxy's 13-billion-year
history, only a handful exist simultaneously, scattered across 100,000
light-years. Our radio signals have traveled just ~100 light-years since the
1920s.

### How it works

A simplified Drake-equation model (constants: 200 billion stars, 100,000
light-year galaxy diameter, 100 light-year signal radius):

```
totalCivs     = stars × habitablePlanets × life × intelligence
concurrent    = totalCivs × (civilizationWindow / galaxyAge)
distance      = galaxyDiameter / ∛concurrent
P(contact)    = min(1, signalRadius / distance)
```

### Disclaimer

This is a thought experiment, not a scientific claim. The parameters
(probability of life, intelligence, civilization lifespan) are fundamentally
uncertain; estimates vary by 10+ orders of magnitude. The tool is for building
intuition about cosmic scale and time, not for making predictions. For a
rigorous treatment of these uncertainties, see Sandberg et al., *"Dissolving
the Fermi Paradox"* (2018).

## Tech stack

- Plain HTML, CSS and JavaScript in one file (`index.html`)
- Canvas 2D for the starfield
- No build step and no JS dependencies; fonts load from Google Fonts
- Hosted on GitHub Pages from the `gh-pages` branch

## Getting started

Open `index.html` in a browser, or serve the folder locally:

```bash
git clone https://github.com/maksimkunaev/civilizations.git
cd civilizations
python3 -m http.server 8000   # then open http://localhost:8000
```

## Project structure

```
civilizations/
├── index.html   # markup, styles, model, rendering and controls
└── README.md
```

## Roadmap

### Scientific accuracy

- Add a separate filter for multicellular life emergence (happens after simple life)
- Split "intelligence" into cognitive ability vs tool-using capability
- Add a parameter for the % of intelligent species that develop detectable technology
- Replace the single "civilization window" with a distribution (min/avg/max lifespan)
- Weight star formation history (most habitable planets formed ~5B years ago, not uniformly)
- Add a galactic habitable zone filter (exclude the galactic center due to radiation)
- Add a metallicity requirement filter (early-universe stars couldn't support rocky planets)

### Detection model

- Replace distance-based contact probability with a signal strength model (inverse square law)
- Add "broadcasting vs listening" asymmetry (civilizations might detect without transmitting)
- Add a detection threshold parameter (minimum signal strength we can detect)
- Show detection probability separately for radio, optical and infrared
- Add Kardashev scale consideration (Type II/III civilizations would be easier to detect)

### UX and features

- Add an "Advanced Mode" toggle to show/hide additional parameters
- Add uncertainty ranges to all calculations (min/max bounds)
- Add comparison to published estimates (SETI, Sandberg et al., etc.)
- Add a timeline view showing when civilizations might have existed
- Add export (save parameters / screenshot)
- Add educational tooltips explaining each filter
- Add a references/citations panel

### Nice to have

- Add a self-destruction probability parameter
- Model directed panspermia scenarios
- Add relativistic travel time calculations
- Show communication lag time for a two-way conversation

## License

[MIT](LICENSE)
