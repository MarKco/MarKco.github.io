---
title: "ProPortion"
tagline: "Rescales recipes: by servings, by an ingredient on hand, by a factor, or by what's in your pantry."
language: "Kotlin"
tags: ["Android", "Jetpack Compose"]
playstore: null
private_repo: true
featured: true
order: 1
alt_url: /progetti/proportion/
---

<!-- playstore: add the Play Store link once you have it handy -->

ProPortion is an Android app that rescales cooking recipes. It works fully offline: no account,
no sync, no data collection.

You enter a recipe with its quantities and the number of people it's meant for, then rescale every
quantity from a single constraint — a different number of people, how much you have of one
ingredient, a straight multiplier, or what's actually in your pantry. The value over doing the math
in your head is correctness in the kitchen: the app knows eggs can't be halved, that "a pinch of
salt" doesn't scale, and that a cake baked at 1.5× the batch doesn't bake for 1.5× the time.

![ProPortion dashboard](/assets/images/projects/proportion/home.png)

## What it does

- **Four ways to rescale a recipe:** by servings, by an ingredient you have on hand, by a direct
  factor (×0.5, ×2, ×3, or any value), or by what's in your pantry — with limiting-factor
  calculation and a heads-up on the bottleneck ingredient.
- **Smart warnings:** rounding for discrete ingredients (eggs, cloves, slices...) and an oven
  warning when the scale factor falls outside the 0.7×–1.4× range, with a suggested new pan
  diameter.
- **Scalings you can save as variants**, sharing as plain text or a `.proportion` file, backup and
  restore of the whole library.
- **Cooking mode** with the screen kept on, a persistent shopping list, and conversion between
  weight, volume and count (including imperial units).
- Italian, English, Spanish and Catalan. Light/dark themes, Material You support.

![Cooking mode](/assets/images/projects/proportion/cook-mode.png)

## License and privacy

Free software, **GNU GPL v3.0**. No data ever leaves the device: no account, no cloud sync.
