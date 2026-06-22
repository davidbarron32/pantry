[pantry-README.md](https://github.com/user-attachments/files/29186259/pantry-README.md)
# Pantry → Recipes

**Find what you can cook with the ingredients you already have — in English or Spanish.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-open_app-111111?style=flat-square)](https://davidbarron32.github.io/pantry/)
![Stack](https://img.shields.io/badge/built_with-Vanilla_JS-555555?style=flat-square)
![Dependencies](https://img.shields.io/badge/dependencies-none-555555?style=flat-square)
![Hosting](https://img.shields.io/badge/hosted_on-GitHub_Pages-555555?style=flat-square)

**Live demo → https://davidbarron32.github.io/pantry/**

---

## Overview

Pantry → Recipes is a single-page web app that takes the ingredients you have on hand and instantly surfaces recipes you can actually make, drawn from a curated dataset of **250 bilingual (English / Spanish) recipes**. It runs entirely in the browser — no backend, no build step, no network calls after the page loads — so it works offline and responds instantly. It solves a small but constant problem: deciding what to cook with what's already in the kitchen, without a trip to the store.

## Features

- **Ingredient-based matching** — enter what you have and get back the recipes that use it, with the closest matches surfaced first.
- **250-recipe curated dataset** — hand-built and structured for clean matching.
- **Fully bilingual (EN / ES)** — switch languages without losing your place.
- **100% client-side** — no server, no API keys, no tracking; works offline once loaded.
- **Single-file architecture** — the entire app ships as one self-contained HTML file, making it trivial to host or share.
- **Zero-reload** — results update instantly as you change your ingredients.

## How it works

The recipe dataset is embedded directly in the page as structured data, with each recipe tagged by its ingredients and stored in both English and Spanish. When you enter the ingredients you have, a client-side matching engine compares them against every recipe's ingredient list, scores each recipe by how closely it matches, and ranks the results so the best fits appear first. Because all of this happens in the browser, there is no server round-trip — matching is instant, and the app keeps working with no connection.

## Tech stack

- **HTML5, CSS3, vanilla JavaScript** — no frameworks, no dependencies, no build tooling
- **GitHub Pages** for hosting

## Run locally

It's a single static file, so there's nothing to install:

```bash
git clone https://github.com/DavidBarron32/pantry.git
cd pantry
open index.html        # macOS — or just double-click the file
```

Or serve it locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Roadmap

- Filter by cuisine, meal type, or dietary preference
- "Almost there" results — recipes you can make by adding one or two ingredients
- Save favorite recipes (`localStorage`)
- Grow the dataset and allow user-submitted recipes

## About

Built by **David Barron**, a data science student in San Diego, as part of a portfolio of small, fully deployed, genuinely useful web tools.

## License

Released under the [MIT License](LICENSE).
