+++
title = 'Magic: The Gathering Search Engine by AI Recognition'
date = 2025-01-05T00:00:00+09:00
draft = false
tags = ['Machine Learning', 'Computer Vision', 'Personal Project']
summary = "A Magic: The Gathering card search engine that identifies a card from a photo using a staged pipeline of AI models instead of one slow full-image recognition pass."
+++

Naive card recognition — running a single heavy model directly on the full, centered image — is slow and wasteful: most of the search space isn't even a match, so paying the full recognition cost on every candidate doesn't scale.

Instead, I built a pipeline of models applied in stages:
- A corner-detection model first locates the card's corners in the image, isolating it from the background.
- A part-by-part model then checks specific regions of the card to quickly filter out the huge majority of candidates that clearly aren't a match.
- Only once the candidate set is small enough does the full recognition model run, on what's left.

This staged approach keeps the search fast by reserving the expensive full recognition step for the few candidates that actually survive the earlier filters.

**Stack:** Machine Learning, Computer Vision

**Source:** [github.com/Potoman/MtgDetector](https://github.com/Potoman/MtgDetector)
