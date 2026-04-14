---
layout: page
title: Research
subtitle: Current projects testing and extending the autoregressive framework
permalink: /research/
---

<div class="card-grid" style="margin-bottom: 3rem;">

<div class="card card--accent">
  <h3>Reference Without Referents</h3>
  <p>A philosophical analysis arguing that LLMs demonstrate language has autonomous self-generative capacity without requiring reference to external objects or speaker intentions. Meaning emerges from distributional structure, not from words "pointing to" things in the world.</p>
  <p class="status">In preparation for Philosophical Review</p>
</div>

<div class="card card--accent">
  <h3>The Autoregressive Brain</h3>
  <p>A comprehensive theoretical paper reconceptualizing memory as generative potential rather than storage-retrieval. Integrates evidence from psychology, neuroscience, and machine learning to argue that cognition operates through sequential state generation.</p>
  <p class="status">In preparation for Trends in Cognitive Sciences</p>
</div>

<div class="card card--accent">
  <h3>Morphosyntactic Constraints in Language Models</h3>
  <p>An empirical test of whether function words and morphology constrain predictions independently of semantic content. Results show morphosyntax reduces next-token entropy by ~1 bit even with nonsense content words --- supporting the distributional account of syntax.</p>
  <p class="status">ArXiv preprint forthcoming</p>
</div>

<div class="card card--accent">
  <h3>World Properties Without World Models</h3>
  <p>Demonstrates that static word embeddings (GloVe, Word2Vec) encode real-world geographic and climate structure. Ridge regression probes on city-name embeddings predict latitude (R² = 0.72), longitude (R² = 0.63), and temperature (R² = 0.64) from distributional information alone.</p>
  <p class="status">Paper submitted &mdash; <a href="https://github.com/elanbarenholtz/northiness" style="text-decoration: underline;">Code on GitHub</a></p>
</div>

<div class="card card--accent">
  <h3>Autogenerative Learning</h3>
  <p>A suite of experiments testing whether transformers can learn to continue sequences they themselves have generated --- probing the boundary between learned patterns and genuinely generative behavior.</p>
  <p class="status"><a href="https://github.com/elanbarenholtz/Autogenerative_Learning" style="text-decoration: underline;">Code on GitHub</a></p>
</div>

<div class="card card--accent">
  <h3>Long-Range Token Influence Analysis</h3>
  <p>A causal intervention framework for measuring how far back in context language models actually use information. Probes the mechanisms of memory-like behavior in transformers by selectively ablating tokens at varying distances.</p>
  <p class="status"><a href="https://github.com/elanbarenholtz/lrtia" style="text-decoration: underline;">Code on GitHub</a></p>
</div>

</div>

<div class="prose">

## Research Philosophy

All of this work flows from a single question: **if cognition is autoregressive generation over learned distributional structure, what should we expect to find?**

Each project tests a different facet of that question. The morphosyntax work tests whether syntactic structure is distributional. The embedding geography work tests whether distributional learning captures world structure. The autogenerative learning work tests the boundaries of what sequential prediction can learn. The philosophical work addresses what the success of LLMs means for theories of meaning and reference.

The goal is not to prove that "the brain is an LLM." The goal is to take seriously what autoregressive prediction can accomplish, and to ask whether biological cognition might operate on the same principle --- even if the implementation details differ enormously.

</div>
