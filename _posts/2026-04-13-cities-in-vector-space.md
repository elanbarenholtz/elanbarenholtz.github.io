---
layout: post
title: "World Properties Without World Models: What Word Embeddings Know About Geography"
date: 2026-04-13
tags: [embeddings, geography, research, distributional-semantics]
description: "Ridge regression probes on GloVe and Word2Vec embeddings predict latitude, longitude, and temperature for 100 world cities — from co-occurrence statistics alone. Semantic ablation reveals where the signal lives."
---

A central claim of the autoregressive brain framework is that distributional structure learned over sequential experience is sufficient to support contextually appropriate generation about the world — without the system needing to maintain explicit world models, stored representations of physical reality, or any mechanism that "looks at" the external environment.

This is a strong claim. We tested one facet of it empirically: can static word embeddings — learned purely from text co-occurrence statistics — predict real-world physical properties of cities?

## Method

We selected 100 globally distributed cities and obtained their embeddings from two standard static models: GloVe (300-dimensional, trained on 6 billion tokens of web text) and Word2Vec (300-dimensional, trained on Google News). These models learn vector representations of words such that words appearing in similar contexts receive similar vectors. They have no access to geographic data, coordinates, temperature records, or any structured knowledge base.

For each city, we collected seven real-world properties: latitude, longitude, average annual temperature, year founded, elevation, GDP per capita, and population. We then trained ridge regression probes — simple linear models with L2 regularization — to predict each property from the 300-dimensional embedding vector. We used leave-one-out cross-validation to estimate prediction accuracy, ensuring that the model never sees the target city during training.

Ridge regression was chosen deliberately. It is a linear model: it can only exploit structure that is linearly decodable from the embedding space. Any predictive success means the relevant information is encoded in a form that is geometrically accessible — not buried in complex nonlinear interactions between dimensions.

## Results

The results split cleanly into two categories.

**Geography and climate are well-predicted:**

| Property | GloVe R² | Word2Vec R² |
|---|---|---|
| Latitude | 0.72 | 0.66 |
| Longitude | 0.63 | 0.47 |
| Temperature | 0.64 | 0.54 |

**Other properties are not:**

| Property | GloVe R² | Word2Vec R² |
|---|---|---|
| Year Founded | < 0.15 | < 0.15 |
| Elevation | < 0.10 | < 0.10 |
| GDP per capita | < 0.20 | < 0.20 |
| Population | < 0.15 | < 0.15 |

This selectivity is important. The embeddings do not encode "everything about cities." They encode properties that shape the distributional contexts in which city names appear. Geography and climate are deeply woven into how cities are discussed — references to region, weather, neighboring countries, cardinal directions, and geopolitical context all co-vary systematically with latitude, longitude, and temperature. Year founded, elevation, and GDP are mentioned in connection with specific cities, but they do not produce the kind of systematic, cross-city distributional variation that embeds into the vector space.

The correlation between latitude and temperature (r ≈ −0.85 across these cities) means the temperature prediction is partially mediated by the same distributional features that encode latitude. But ablation analysis (below) shows that temperature prediction also draws on climate-specific distributional structure that is partially independent of the geographic signal.

## Semantic ablation: Where does the signal come from?

To understand which aspects of distributional context drive the geographic predictions, we performed a semantic ablation analysis. The procedure:

1. Define semantic categories: cardinal direction terms (north, south, east, west, and derivatives), climate/weather terms, region/continent names, country names, economic terms, and cultural/language terms.
2. For each category, collect the embeddings of the terms in that category and compute the subspace they span (via PCA on the term embeddings).
3. Project the city embeddings into the orthogonal complement of that subspace — effectively removing any variance along the dimensions associated with that semantic category.
4. Re-run the ridge regression probes on the ablated embeddings and measure the change in R².

**What the ablation revealed:**

- **Cardinal direction terms** account for a significant portion of latitude prediction. Removing the subspace spanned by "north," "south," "northern," "southern," etc. substantially reduces latitude R². This is expected: cities in the northern hemisphere systematically co-occur with northern-associated terms.

- **Climate and weather terms** contribute to temperature prediction beyond what latitude alone provides. Removing the climate subspace reduces temperature R² even after accounting for the latitude-temperature correlation.

- **Region and continent names** carry both latitude and longitude information. "European," "African," "Southeast Asian" — these terms define distributional neighborhoods that jointly encode geographic position.

- **Country names** provide strong geographic signal, as expected — city-country co-occurrence is high, and countries have characteristic geographic positions.

- **Economic and cultural terms** contribute modestly, primarily to longitude (which correlates with the East-West economic and cultural axis).

The critical finding: **after removing all interpretable semantic subspaces, substantial predictive power remains.** The geographic information is not confined to obviously geographic dimensions of the embedding space. It is distributed throughout the full 300-dimensional geometry, encoded in co-occurrence patterns that are not reducible to a small set of semantically transparent features.

This is exactly what you would expect from a system that learns distributional structure holistically. The embedding does not have a "geography module." It has learned the statistical structure of how city names appear in text, and that structure happens to track physical geography — because physical geography shapes language use.

## Implications for the autoregressive framework

This result bears on the autoregressive brain framework in a specific way. A common objection to the framework is: "Distributional statistics over language can't capture real-world structure. You need grounded representations — sensory experience, embodied interaction — to know anything about the physical world."

The embedding results show that this objection is too strong. Co-occurrence statistics over text — which is already one step removed from sensory experience — capture enough physical-world structure to predict geographic coordinates and climate with moderate to high accuracy. The information is there, linearly decodable, from distributional learning alone.

Now extend the principle to a system that learns distributional structure not over text but over the full multimodal stream of embodied experience — visual, auditory, proprioceptive, interoceptive, linguistic. Such a system would have access to far richer co-occurrence statistics than any text corpus. The claim that distributional learning over experiential trajectories is sufficient to support world-appropriate generation becomes considerably more plausible.

The brain does not need a stored map of the world in the hippocampus. It does not need explicit representations of "Cairo is in North Africa" or "Stockholm is cold." It needs distributional structure over experience — and from that structure, it can generate contextually appropriate outputs about geography, climate, and spatial relationships. Not because it has looked at a map, but because the statistical structure of experience tracks the statistical structure of the world.

The full paper and all analysis code are available on [GitHub](https://github.com/elanbarenholtz/northiness).
