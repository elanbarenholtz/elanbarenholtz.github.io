---
layout: page
title: The Framework
subtitle: A unified theory of memory, attention, perception, learning, and behavior
permalink: /theory/
---

<div class="prose" markdown="1">

<style>
.theory-tabs { display: flex; gap: 0; margin-bottom: 2rem; border-bottom: 2px solid #e2e8f0; }
.theory-tab { padding: 0.75rem 1.5rem; text-decoration: none; font-weight: 600; color: #718096; }
.theory-tab--active { color: #2d3748; border-bottom: 3px solid #2d3748; margin-bottom: -2px; }
</style>

<div class="theory-tabs">
  <a href="/theory/" class="theory-tab theory-tab--active">Overview</a>
  <a href="/formalism/" class="theory-tab">Formal Statement</a>
</div>

## A Unified Theory

The autoregressive framework is a unified theory of memory, attention, perception, learning, and behavior. It rests on a single claim: the brain generates each next perceptual-cognitive state --- each next experience --- as the optimal continuation of its own prior output, conditioned on current sensation. This single operation --- sequential self-conditioned generation --- produces what we call perceiving, remembering, attending, speaking, reasoning, and acting. Behavior is not computed by this process; it is a consequence of the neural activity that generates experience, driven by the same tissue's anatomical connections to muscles and glands. These are not separate faculties requiring separate explanations. They are aspects of the same autoregressive process, observed at different timescales or from different angles.

Traditional accounts treat these as independent systems: storage-retrieval models of memory, rule-based accounts of syntax, modular architectures for perception. Each works tolerably within its own domain, but none connects to the others in a way that explains how a single organ does all of these things simultaneously, in real time, with the same tissue. The autoregressive framework replaces this collection of domain-specific mechanisms with one computational principle from which all of them emerge.

## Why Autoregression

The world has temporally extended structure. Objects persist, events unfold, causes precede effects, actions produce consequences. None of this is available in an instantaneous sensory slice. Any system that must act on this structure needs to maintain and operate over sequences.

Not all sequential processing requires autoregression. Sensation-local filters --- Reichardt-style motion detection, onset and offset responses --- extract temporal features directly from the input stream. These are real and biologically widespread. What they cannot do is build trajectories, track content across gaps in sensation, or generate structure the signal does not contain. Cognition is the regime that does.

The brain performs extensive parallel processing that is not autoregressive --- sensory transduction, feature extraction, homeostatic regulation, autonomic control, reflexes. This processing is real, biologically critical, and not the subject of this theory. Cognition is a computationally distinct process that takes this massive parallel state and generates a serial, contextual stream. The move from parallel sensory state to integrated cognitive state is what the generator does, and it matches the intuition of what attention is: the funneling of an enormous concurrent state into a single sequential stream.

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

The autoregressive process has properties that are strikingly coincident with the structure of subjective experience: it is serial, self-conditioned, egocentric, and temporally continuous. The framework does not claim to have solved the question of how matter gives rise to subjectivity --- but that question may itself be ill-posed, since "physical matter" is a construct generated within an autoregressive system for the purposes of coordination and reasoning, not a foundation from which experience must be derived. The full argument is developed in the <a href="#consciousness">consciousness section</a> below.

### LLMs as Existence Proofs

Large language models are not models of the brain. They differ from biological systems in architecture, training, and substrate. But they prove something important: that autoregressive prediction over learned distributional structure can produce composition, apparent reasoning, memory-like behavior, and contextual sensitivity --- without explicit storage, retrieval, or rule systems.

If next-token prediction can do all of this in silicon, we should take seriously the possibility that next-state prediction does the same in neural tissue.

## Empirical Evidence

### 74 Phenomena, One Principle

The autoregressive framework is not a theory of one domain. It generates specific, testable accounts across the full range of cognitive phenomena --- behavioral, psychological, neurophysiological, and neuroanatomical.

In **language**, the framework explains garden-path sentences, incremental parsing, structural priming, and the N400 as natural consequences of serial commitment to generated continuations. In **memory**, it accounts for false memories, context-dependent recall, reconsolidation, serial position effects, and the dissolution of the short-term/long-term distinction --- all without positing separate storage systems. In **perception and consciousness**, it explains change blindness, perceptual completion, binocular rivalry, and the stream of consciousness as properties of a system that generates rather than records experience. In **imagery and thought**, mental rotation, mental scanning, and the shared neural substrates of memory and imagination follow from the same generative process running under different constraints. The framework extends to **deliberation and reasoning** (reframing System 1/System 2 as low- vs. high-depth generation), **social cognition** (stereotypes as distributional priors), **aesthetics** (the pleasure of well-constrained generation), and **clinical phenomena** including schizophrenia, confabulation, PTSD, and aphasia. At the **neural level**, it reinterprets feedback-dominant cortical connectivity, gamma-band dynamics, hippocampal replay, and place cells as components of the autoregressive architecture.

74 phenomena across 12 domains, unified under a single computational principle.

<a href="/blog/2026/04/phenomena-explained-by-autoregressive-theory/" class="btn">Explore All 74 Phenomena &rarr;</a>

## Implications

If cognition is autoregressive generation rather than storage-retrieval, several things follow:

- **Memory failures** are not retrieval failures but generation failures --- the system generates a trajectory that diverges from a previous one
- **Imagination** is not separate from memory --- both are generative processes, differing only in their constraints
- **Understanding** is not the activation of stored concepts but successful trajectory generation through a semantically structured state-space
- **The self** is not an entity but a narrative trajectory that includes a model of its own generation

This is not a metaphor. It is a mechanistic proposal: cognition is sequential state generation, constrained by distributional structure learned over a lifetime.

## Consciousness {#consciousness}

### The Autoregressive Stream Is Conscious Experience

The autoregressive framework does not merely accommodate consciousness --- it identifies it. The serial, contextual sequence of generated states is not correlated with conscious experience. It *is* conscious experience. What enters the generated sequence is conscious; what remains in the parallel sensory state without being integrated into that sequence is not. Attention and consciousness are the same thing: the funneling of an enormous parallel state into a single serial stream.

This gives unity of consciousness for free: there is one generator, producing one state at a time. It gives the stream quality of experience: each state conditions the next, producing the continuous temporal flow that characterizes subjective life. And it gives the relationship between attention and consciousness without remainder: you cannot be conscious of what you have not generated.

### Subjectivity as Recursive Navigation

The deeper question --- why this process constitutes subjective experience, why there is something it is like to be a system running this architecture --- has traditionally been treated as unanswerable by physical theory. The autoregressive framework gets closer than any account I am aware of.

Subjectivity is what recursive output-intake navigation of an egocentric decision space *is*, from the only perspective available to the system: its own generated trajectory.

Consider what the architecture entails. The system's only access to anything --- the world, its own body, its own prior states --- is through the sequence it generates. It is constitutively locked into its own perspective. There is no view from outside, because "outside" is not a location in the system's state-space. The system navigates a space of possibilities structured by consequences to itself, generating each next position from where it currently stands, conditioned on where it has been. That navigation --- egocentric, sequential, self-conditioned --- is not a process that *produces* experience as a byproduct. It is what experience *is*.

The hard problem assumes that processing and experience are two things that need connecting: there is the computation, and then there is the "what it's like," and the mystery is how one gives rise to the other. But if subjectivity just *is* what it is to be a system recursively navigating an egocentric decision space through its own generated output, there is no second thing to explain. The computation, done this way --- self-conditioned, serial, egocentric, consequential --- *is* the subjective experience. You do not need to add qualia to the process. The process, structured this way, is qualia.

### What Falls Out

This account explains several features of consciousness that are otherwise mysterious:

**Why consciousness is serial.** Not because of limited resources, but because the generator produces one state at a time. Seriality is not a constraint on consciousness; it is a constitutive feature of the autoregressive process that consciousness is.

**Why anesthesia abolishes consciousness.** It disrupts the autoregressive loop. The parallel processing in the sensory state may continue, but the generator stops producing the serial, contextual stream. No stream, no experience.

**Why dreams are conscious.** The generator runs with sensation largely disconnected. The autoregressive process continues --- self-conditioned generation proceeds --- and so experience continues, even though the content is unconstrained by external input.

**Why flow states feel different.** The generator runs with reduced self-modeling in the generated state. The autoregressive stream continues, but it contains less recursive content about its own operation. The system is still conscious but less conscious *of itself*.

**Why the binding problem dissolves.** Components of experience were never separate in the generator. The question "how does the brain bind color, shape, and motion into a unified percept?" presupposes that these are computed separately and then combined. In the autoregressive framework, they are generated together as aspects of a single output state. There is nothing to bind.

---

## Formal Statement

The mathematical architecture underlying this framework --- the generator equation, core claims, physiological predictions, and the information geometry of memory --- is developed in full on a dedicated page.

<a href="/formalism/" class="btn">Read the Formal Statement &rarr;</a>

---

## Research

Several lines of empirical and theoretical work are currently testing and extending this framework --- from morphosyntactic constraints in language models to the information geometry of long-range token influence to philosophical accounts of reference without referents.

<a href="/research/" class="btn">Current Projects &rarr;</a>

</div>
