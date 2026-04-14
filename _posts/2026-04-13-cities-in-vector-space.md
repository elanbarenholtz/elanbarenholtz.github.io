---
layout: post
title: "Cities in Vector Space: What Word Embeddings Know About Geography"
date: 2026-04-13
tags: [embeddings, geography, research]
description: "GloVe and Word2Vec embeddings predict latitude, longitude, and temperature for world cities — from text statistics alone."
---

Here's a finding that surprised us: if you take the GloVe embedding for "Cairo" and run a simple linear regression, you can predict Cairo's latitude with reasonable accuracy. The same for Tokyo, Santiago, Oslo, and about a hundred other cities.

No maps. No coordinates in the training data. Just word co-occurrence statistics from a web corpus.

## The Setup

We took 100 global cities and looked up their embeddings in two standard static word embedding models: GloVe (trained on web text) and Word2Vec (trained on Google News). Then we asked: can a simple ridge regression probe predict real-world properties of these cities from their 300-dimensional embedding vectors?

We tested seven targets: latitude, longitude, average temperature, year founded, elevation, GDP per capita, and population.

## What Works and What Doesn't

The results split cleanly:

**Geography and climate are well-predicted:**
- Latitude: R² = 0.72 (GloVe), 0.66 (Word2Vec)
- Longitude: R² = 0.63 (GloVe), 0.47 (Word2Vec)
- Temperature: R² = 0.64 (GloVe), 0.54 (Word2Vec)

**Everything else is not:**
- Year Founded: R² < 0.15
- Elevation: R² < 0.10
- GDP per capita: R² < 0.20
- Population: R² < 0.15

This pattern is important. The embeddings don't just encode "stuff about cities" in some general way. They specifically encode properties that are reflected in how cities are talked about in text --- and geography and climate deeply shape the linguistic contexts in which city names appear.

## Where Does the Signal Come From?

We ran a semantic ablation analysis to find out. By systematically removing embedding subspaces associated with different semantic categories, we measured how much of the geographic prediction depends on each one:

- **Cardinal direction terms** (north, south, east, west, etc.) account for a significant chunk of latitude prediction
- **Climate and weather terms** contribute substantially to temperature prediction
- **Region and continent names** carry both latitude and longitude information
- **Country names** provide strong geographic signal

But here's what's interesting: even after removing all of these interpretable subspaces, substantial predictive power remains. The geographic information is distributed throughout the embedding space, not confined to obviously geographic dimensions.

## Why This Matters for the Autoregressive Framework

This result demonstrates something important about distributional learning: **co-occurrence statistics capture structure that tracks the physical world.**

Nobody told GloVe that Cairo is in North Africa. Nobody labeled training examples with geographic coordinates. But because Cairo co-occurs with other North African cities, with references to desert and heat, with particular geopolitical contexts --- and because these contexts systematically differ from those of, say, Stockholm --- the embedding ends up encoding geographic position.

This supports a key claim of the autoregressive brain framework: **you don't need stored world models to generate contextually appropriate outputs about the world.** Distributional structure learned over experience is sufficient to capture real-world regularities.

The brain doesn't need a map of the world stored somewhere in the hippocampus. It needs distributional structure over experience --- and from that structure, map-like behavior can be generated on the fly.

The paper and all code are available on [GitHub](https://github.com/elanbarenholtz/northiness).
