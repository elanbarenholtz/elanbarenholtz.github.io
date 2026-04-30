---
layout: page
title: The Autoregressive Brain
subtitle: A new framework for cognition, memory, and language
permalink: /theory/
---

<div class="prose" markdown="1">

## The Missing Framework

Cognitive science has no unified theory of cognition. There are theories of memory, theories of perception, theories of language, theories of motor control --- each with its own mechanisms, its own vocabulary, its own computational assumptions. The brain, apparently, runs dozens of specialized systems in parallel, coordinated by means no one can quite specify.

This fragmentation is not for lack of effort. It reflects a deeper problem: the foundational assumptions shared across most of these theories may be wrong. Storage-retrieval models of memory, rule-based accounts of syntax, modular architectures for perception --- each works tolerably within its own domain, but none connects to the others in a way that explains how a single organ does all of these things simultaneously, in real time, with the same tissue.

What is missing is not another domain-specific model. What is missing is an account of the basic computational operation the brain performs --- one operation, from which perception, memory, language, reasoning, and consciousness emerge as different views of the same process.

The autoregressive framework is that account. The brain generates each next cognitive state as the optimal continuation of its own prior output, conditioned on current sensation. This single principle --- sequential self-conditioned generation --- unifies phenomena that have traditionally required separate explanations.

## What LLMs Revealed

Large language models offer a different picture. LLMs have no explicit memory store, yet they exhibit sophisticated memory-like behaviors. They generate contextually appropriate continuations by predicting each token from the preceding sequence, constrained by distributional patterns learned during training.

This is not an analogy. It is an existence proof: sequential prediction over learned distributional structure is sufficient to produce behaviors that look like memory, reasoning, composition, and understanding --- without any of the machinery that cognitive science traditionally assumes is required.

I propose that biological cognition works the same way.

## The Core Framework

What we call "memory" is not retrieval from storage but **generative potential** --- the capacity to regenerate trajectories through cognitive state-space. Each mental state generates the next, constrained by patterns learned over a lifetime of experience.

This reconceptualizes not just memory, but language, consciousness, and cognition more broadly:

### Generation, Not Retrieval

Remembering is reconstructive generation. When you recall your tenth birthday, you don't play back a recording. You generate a plausible trajectory through experiential state-space, constrained by whatever cues are available. This is why memories are context-sensitive, malleable, and seamlessly continuous with imagination --- generation and "retrieval" are the same process with different seeds.

### Syntax as Distributional Epiphenomenon

What linguists call "grammar" is not a rule system that the brain implements. It is the skeletal structure of distributional statistics. Function words (THE, WAS, TO) and morphological markers (-ING, -ED, -LY) are high-leverage tokens that constrain sequential prediction. They don't carry meaning themselves --- they scaffold the trajectory that meaning-bearing tokens will follow.

This explains why children don't learn grammar by learning rules, why grammatical violations feel wrong before you can explain why, and why LLMs acquire syntax without being taught it.

### Consciousness as Recursive Autoregression

Subjective experience emerges from the cognitive system modeling its own generative process. The "self" that seems to persist across time is not an entity doing the experiencing --- it is a trajectory through state-space that includes a model of itself. Unity of consciousness reflects continuity of generation.

This is not mystical. It is the same principle by which LLMs can discuss their own outputs: recursive modeling of the generative process that produces each next state.

### LLMs as Existence Proofs

Large language models are not models of the brain. They differ from biological systems in architecture, training, and substrate. But they prove something important: that autoregressive prediction over learned distributional structure can produce composition, apparent reasoning, memory-like behavior, and contextual sensitivity --- without explicit storage, retrieval, or rule systems.

If next-token prediction can do all of this in silicon, we should take seriously the possibility that next-state prediction does the same in neural tissue.

## Empirical Evidence

### The Morphosyntax Experiment

If syntax is distributional structure over high-leverage tokens, then function words and morphology should constrain predictions even when surrounded by nonsense. We tested this directly by measuring next-token entropy in language models across four conditions:

<div class="experiment-box">

<div class="conditions">
  <div class="condition">
    <div class="condition-label">Real Sentences:</div>
    <div class="condition-example">"The teacher was explaining the concept clearly"</div>
  </div>
  <div class="condition">
    <div class="condition-label">Jabberwocky:</div>
    <div class="condition-example">"The blicket was florping the daxen grentily" (function words + morphology intact)</div>
  </div>
  <div class="condition">
    <div class="condition-label">Stripped:</div>
    <div class="condition-example">"Ke blicket nar florp ke daxen grenti" (all nonwords, no morphology)</div>
  </div>
  <div class="condition">
    <div class="condition-label">Random Nonwords:</div>
    <div class="condition-example">Completely unstructured</div>
  </div>
</div>

<div class="results">
  <p><strong>Results:</strong></p>
  <p class="formula">Sentences (7.45 bits) &lt; Jabberwocky (8.04) &lt; Stripped (9.07) &lt; Random (9.27)</p>
  <p>Morphosyntax alone reduces entropy by ~1 bit (p &lt; 0.0001, d = -1.75). Function words and morphological markers constrain prediction independently of semantic content --- exactly as predicted by the distributional account.</p>
</div>

</div>

### Neural Evidence Reinterpreted

Fedorenko et al. (2016) showed that gamma-band activity increases monotonically as people read sentences --- but not for word-lists, Jabberwocky, or nonword strings. The standard interpretation: the brain is "building meaning" compositionally.

**The autoregressive interpretation:** the brain is generating a trajectory through semantic state-space. Sentences produce full build-up because both morphosyntactic scaffolding and semantic content constrain the trajectory. Jabberwocky and word-lists produce partial build-up because only one constraint source is present. The gamma increase reflects trajectory construction, not compositional semantics per se.

### World Properties Without World Models

Our work on static word embeddings shows that simple co-occurrence statistics encode real-world geographic and climate structure. GloVe and Word2Vec embeddings for city names predict latitude (R² = 0.72), longitude (R² = 0.63), and temperature (R² = 0.64) using only distributional information --- no maps, no thermometers, no explicit world knowledge.

This demonstrates that distributional learning over text captures structure that tracks the physical world, supporting the claim that autoregressive generation over learned distributions can produce contextually appropriate outputs without stored representations of external reality.

## Implications

If cognition is autoregressive generation rather than storage-retrieval, several things follow:

- **Memory failures** are not retrieval failures but generation failures --- the system generates a trajectory that diverges from a previous one
- **Imagination** is not separate from memory --- both are generative processes, differing only in their constraints
- **Understanding** is not the activation of stored concepts but successful trajectory generation through a semantically structured state-space
- **The self** is not an entity but a narrative trajectory that includes a model of its own generation

This is not a metaphor. It is a mechanistic proposal: cognition is sequential state generation, constrained by distributional structure learned over a lifetime.



---

## Formal Statement

The mathematical architecture underlying this framework --- the universal cognition operator, ten core claims, physiological predictions, and the information geometry of memory --- is developed in full on a dedicated page.

<a href="/formalism/" class="btn">Read the Formal Statement &rarr;</a>

---

## The Evidence: 74 Phenomena, One Principle

This framework doesn't just offer a new metaphor --- it generates specific, testable explanations across the full range of cognitive phenomena. From garden-path sentences to false memories, from mental rotation to musical earworms, from schizophrenia to the binding problem --- 74 phenomena unified under a single computational principle.

<a href="/blog/2026/04/phenomena-explained-by-autoregressive-theory/" class="btn">Explore All 74 Phenomena &rarr;</a>

</div>
