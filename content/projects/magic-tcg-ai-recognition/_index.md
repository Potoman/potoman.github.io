+++
title = 'Magic: The Gathering Search Engine by AI Recognition'
date = 2026-11-22T00:00:00+09:00
draft = false
tags = ['Machine Learning', 'Computer Vision', 'Personal Project']
summary = "A Magic: The Gathering card search engine that identifies a card from a photo using a staged pipeline of AI models instead of one slow full-image recognition pass."
status = 'Very Active'

[cover]
  image = "card_found.png"
  alt = "The Magic: The Gathering card Metalworker found from its detected mana cost, power/toughness, rarity and set"
  hiddenInSingle = true
+++

Naive card recognition — running a single heavy model directly on the full, centered image — is slow and wasteful: most of the search space isn't even a match, so paying the full recognition cost on every candidate doesn't scale.

Instead, I built a pipeline of models applied in stages:
- A corner-detection model first locates the card's corners in the image, isolating it from the background.
- A part-by-part model then checks specific regions of the card to quickly filter out the huge majority of candidates that clearly aren't a match.
- Only once the candidate set is small enough does the full recognition model run, on what's left.

This staged approach keeps the search fast by reserving the expensive full recognition step for the few candidates that actually survive the earlier filters.

See [Use Yolo Pose from Ultralytics](/projects/magic-tcg-ai-recognition/use-yolo-pose-from-ultralytics/) for how the corner-detection stage works and how its training dataset was generated from Scryfall without any manual labeling.

See [Detect the Set and the Mana Cost](/projects/magic-tcg-ai-recognition/detect-set-and-mana-cost/) for the set and mana cost detection features.

See [Data Augmentation for the Mana Cost](/projects/magic-tcg-ai-recognition/data-augmentation-for-mana-cost/) for how a generated training set improved the mana cost detection.

See [Set + Rarity and Power + Toughness Detection Works](/projects/magic-tcg-ai-recognition/set-rarity-and-power-toughness-detection/) for the set with its rarity, the power/toughness detection, and the search for the matching card.

**Source:** [github.com/Potoman/MtgDetector](https://github.com/Potoman/MtgDetector)
