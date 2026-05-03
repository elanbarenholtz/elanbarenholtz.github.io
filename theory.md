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

The autoregressive framework is a unified theory of memory, attention, perception, learning, and behavior. It rests on a single claim: the brain generates each next perceptual-cognitive state --- each next experience --- as the optimal continuation of its own prior output, conditioned on current sensation. This single operation --- sequential self-conditioned generation --- produces what we call perceiving, remembering, attending, speaking, reasoning, and acting. Behavior is not computed by this process; it is a consequence of the neural activity that generates experience --- that activity drives muscles and glands through anatomical connections, but the system never observes its own behavioral output. These are not separate faculties requiring separate explanations. They are aspects of the same autoregressive process, observed at different timescales or from different angles.

Traditional accounts treat these as independent systems: storage-retrieval models of memory, rule-based accounts of syntax, modular architectures for perception. Each works tolerably within its own domain, but none connects to the others in a way that explains how a single organ does all of these things simultaneously, in real time, with the same tissue. The autoregressive framework replaces this collection of domain-specific mechanisms with one computational principle from which all of them emerge.

## Why Autoregression

The world has temporally extended structure. Objects persist, events unfold, causes precede effects, actions produce consequences. None of this is available in an instantaneous sensory slice. Any system that must act on this structure needs to maintain and operate over sequences.

Not all sequential processing requires autoregression. Sensation-local filters --- Reichardt-style motion detection, onset and offset responses --- extract temporal features directly from the input stream. These are real and biologically widespread. What they cannot do is build trajectories, track content across gaps in sensation, or generate structure the signal does not contain. Cognition is the regime that does.

The brain performs extensive parallel processing that is not autoregressive --- sensory transduction, feature extraction, homeostatic regulation, autonomic control, reflexes. This processing is real, biologically critical, and not the subject of this theory. Cognition is a computationally distinct process that takes this massive parallel state and generates a serial, contextual stream. The move from parallel sensory state to integrated cognitive state is what the generator does, and it matches the intuition of what attention is: the funneling of an enormous concurrent state into a single sequential stream.

## What LLMs Revealed

Large language models offer a different picture. LLMs have no explicit memory store, yet they exhibit sophisticated memory-like behaviors. They generate contextually appropriate continuations by predicting each token from the preceding sequence, constrained by distributional patterns learned during training.

This is not an analogy. It is an existence proof: sequential prediction over learned distributional structure is sufficient to produce behaviors that look like memory, reasoning, composition, and understanding --- without any of the machinery that cognitive science traditionally assumes is required. LLMs are not models of the brain. They differ from biological systems in architecture, training, and substrate. But if next-token prediction can do all of this in silicon, we should take seriously the possibility that next-state prediction does the same in neural tissue.

## Cognition Reconceived

The autoregressive framework does not merely offer a new metaphor for cognition. It reconceives each cognitive faculty as a specific expression of a single underlying operation: the generator producing the next perceptual-cognitive state as a continuation of the preceding trajectory, conditioned on current sensation. What follows is a systematic account of what this means for each domain.

### Perception

Perception is output, not input. Sensation arrives from the environment and body; the percept is what the generator produces in response. These are not the same thing. What the system "sees" is what it generates, not what it receives. Sensation constrains generation but does not constitute it.

This is why illusions exist. The generator produces a coherent experiential state shaped by its learned structure, and that structure sometimes overrides the sensory signal. Filling-in, amodal completion, size constancy, and the Gestalt grouping principles are not errors or heuristics --- they are the generator doing exactly what it does: producing the most probable continuation of the perceptual trajectory given the available constraints. Change blindness follows naturally: if the change does not disrupt the generator's continuation, it is not generated as part of the perceptual state, and so it is not perceived. There is no "failure to detect" because there is nothing that detects. There is only generation.

The distinction between sensation and perception also explains why perceptual experience is always richer than the sensory signal warrants. The system generates a full experiential state from partial, noisy, ambiguous input because generation is the only operation it performs. It cannot deliver raw sensation to experience. It can only generate a state that is consistent with sensation, shaped by everything the generator has learned.

### Attention

Attention is not a spotlight, a filter, or a resource. It is the autoregressive process itself. The brain performs massive parallel processing --- sensory transduction across millions of receptors, feature extraction in early cortical areas, autonomic regulation, reflexive loops. All of this runs concurrently. But cognition is the regime in which this enormous parallel state is funneled into a single serial stream: one generated state at a time.

What we call "attending" to something is that thing dominating the current generation step. The system can only generate one perceptual-cognitive state per cycle, and whatever content shapes that state is what the system is attending to. Inattentional blindness is not a failure to notice something that was there --- it is a failure to generate it. If it was not part of the generated state, it was not part of experience. There is nothing it was like to miss it, because the missing content was never produced.

This dissolves the longstanding puzzle of how attention relates to consciousness --- a question taken up in full in the <a href="#consciousness">consciousness section</a> below. The serial nature of conscious experience is not a limitation imposed by scarce resources. It is a structural feature of the architecture.

### Memory

Memory is not storage and retrieval. It is the continued influence of past generation on present generation, operating at multiple timescales.

What we call "remembering" is reconstructive generation. When you recall your tenth birthday, you do not play back a recording. You generate a plausible trajectory through experiential state-space, constrained by whatever cues are available and by the distributional structure learned over a lifetime. This is why memories are context-sensitive --- different cues seed different trajectories through the same region of state-space. It is why memories are malleable --- each act of remembering is a new act of generation, shaped by the current state, not a readout of fixed content. And it is why memory is seamlessly continuous with imagination --- both are generative processes, differing only in their constraints. Remembering is generation seeded by a cue that points toward a prior trajectory. Imagining is generation seeded by a cue that points somewhere new. The process is identical.

The traditional distinction between short-term and long-term memory dissolves. There are not two memory systems with different operating principles and a transfer mechanism between them. There is influence at different timescales. Fast state carries influence that decays over seconds --- what is traditionally called working memory. Slow structure carries influence that persists across a lifetime --- what is traditionally called long-term memory. The difference is the time constant of the substrate, not the nature of the operation.

Memory failures are not retrieval failures. They are generation failures --- the system generates a trajectory that diverges from a previous one. False memories are not corrupted files. They are trajectories that were generated coherently but happened to diverge from the historical trajectory at some point, often because the available cues were compatible with multiple continuations. The system has no way to distinguish a "true" memory from a "false" one, because both are generated by the same process. There is no original to compare against.

The forgetting curve is not the rate at which the brain loses what it stored. It is the rate at which successive autoregressive compression reduces the specificity needed for regeneration. Each generative step preserves what is needed to shape continuation while shedding detail that does not contribute to the trajectory going forward. After many such steps, the influence of a distant past state persists --- but the specificity required to reconstruct it does not. This is developed formally in the <a href="/formalism/#the-information-geometry-of-memory">information geometry of memory</a>.

### Language

Human language is literally next-token generation. The same autoregressive process that produces perception produces speech. Each word conditions the next, shaped by distributional structure learned over a lifetime of linguistic experience. The system does not retrieve sentences from storage or assemble them from rules. It generates them as trajectories through a linguistically structured state-space.

What linguists call "grammar" is not a rule system that the brain implements. It is the skeletal structure of distributional statistics. Function words (THE, WAS, TO) and morphological markers (-ING, -ED, -LY) are high-leverage tokens that constrain sequential prediction. They do not carry meaning themselves --- they scaffold the trajectory that meaning-bearing tokens will follow. This explains why children do not learn grammar by learning rules, why grammatical violations feel wrong before you can explain why, and why LLMs acquire syntax without being taught it. Grammar is what distributional regularity looks like when you examine the scaffolding tokens.

Garden-path sentences are natural consequences of serial commitment. The generator commits to a continuation at each step; when later input is incompatible with that commitment, the trajectory must be revised, producing the characteristic experience of surprise and reprocessing. Structural priming --- the tendency to reuse recently generated syntactic structures --- follows directly: the prior trajectory shapes the next one. The N400 component, traditionally interpreted as a measure of semantic expectation violation, is the neural signature of the generator encountering input that disrupts the current trajectory.

This account unifies language production and comprehension. Both are generation. In production, the system generates a linguistic trajectory that exits through speech musculature. In comprehension, the system generates a linguistic trajectory conditioned on incoming speech, effectively regenerating the speaker's trajectory in its own state-space. Understanding is successful trajectory alignment between generator and signal.

### Reasoning and Decision Making

What is traditionally called "reasoning" is extended autoregressive generation with the generated trajectory itself as the dominant conditioning content. The system generates a state, that state conditions the next, and the chain extends through a sequence of inferential steps. There is no separate reasoning module or logic engine. There is depth of generation.

The distinction between System 1 and System 2 thinking is reframed as the difference between low-depth and high-depth generation. Fast, automatic responses are shallow trajectories --- the generator produces a continuation in one or a few steps, driven primarily by well-learned distributional structure. Deliberate reasoning is deep generation --- the system extends the trajectory through many steps, with each generated state conditioning the next, producing the serial, effortful character of conscious thought.

Decision making is generation under outcome constraint. The system generates possible trajectories forward from the current state, and the trajectory that dominates is the one most consistent with the generator's learned structure --- which has been shaped, over a lifetime, by the sensation that followed similar states. The system does not compute expected utility. It generates continuations and is shaped to favor those whose downstream sensation has historically been favorable. This is why decisions feel like something: they are experienced as generated trajectories, not as computed outputs. Indecision is the generator failing to settle on a single continuation. Regret is generating the alternative trajectory after the fact.

### Imagination and Creativity

Imagination is generation with sensation playing a reduced or absent role. The same process that produces perception --- the generator operating over its prior output, conditioned on sensation --- produces imagery when sensation is attenuated or absent. This is why mental imagery shares neural substrates with perception, why imagined actions activate motor-associated areas, and why vivid imagination can be confused with memory. The generator does not distinguish between generating a percept from sensation and generating an image from a cue. The process is identical; the constraints differ.

Creativity is generation at the edge of learned distributional structure. The generator produces trajectories that are improbable but not impossible given its learned constraints --- novel enough to be interesting, coherent enough to be intelligible. Highly creative states often involve the relaxation of the most constraining distributional priors, allowing the generator to explore regions of state-space it would not normally visit. This is consistent with the association between creativity and states of reduced cognitive control, including mind-wandering, dreaming, and certain pharmacological states --- all conditions in which the tightest distributional constraints are loosened.

### The Self and Agency

The autoregressive framework has a radical implication for the self: it is a generated construct, not a foundational entity. The "I" that appears in thought and speech is a token --- perhaps the most powerful token in the system's repertoire --- that compresses an enormous amount of trajectory regularity into a form the generator can efficiently condition on. "I" organizes the relationship between generated states and returning sensation into a coherent narrative. But it is authored by the generator, not observed by it.

The system has no direct access to its own behavior. Motor commands, hormonal signals, autonomic activation --- these are consequences of the neural activity that generates experience, not outputs that the system observes. What the system feels is not the motor command but proprioception --- the position of its limb, processed into a percept. Not sympathetic activation but its heart racing --- interoception, processed into a percept. Every channel through which the system might "know" what it is doing is mediated by sensation and processed into perception. There is no shortcut.

This means attribution of agency is always a generated inference, never a direct observation. The system cannot distinguish self-caused sensation from world-caused sensation. Both arrive as ordinary input. What the system learns is temporal contiguity: states like this tend to be followed by sensation like that. Over time, this regularity gets compressed into the construct of agency --- "I did that" --- which is an efficient generative token, not a report from a privileged self-monitoring channel. Attribution errors are not failures of an otherwise reliable system. They are the baseline. Attribution is always confabulation that happens to align, more or less, with external causal structure.

LLMs exhibit the same phenomenon: they use "I" with apparent coherence, not because they have a self-model, but because "I" is a statistically powerful token that constrains continuation. The difference between biological and artificial systems here is not qualitative. Both generate "I" because it is useful for shaping what comes next.

### Learning and Development

Learning is not a separate phase of operation. Every cycle of the generator simultaneously produces the current experiential state and encodes it into the system's structure. Fast state is updated with the current trajectory; slow structure is reshaped by the current activity. There is no distinct write operation, no training regime that operates offline. Generation *is* encoding.

A single optimization process shapes both behavior and representation. Slow structure is continuously modified by a process that jointly achieves two outcomes. First, it shapes the system to generate experiential states that tend to be followed by favorable returning sensation --- behavioral optimization, achieved indirectly through temporal contiguity in the trajectory. Second, it shapes the system to generate states in a format that the generator can most effectively condition on in the next cycle --- representational optimization, entirely within the loop.

The system does not just learn *what* to generate; it learns *how* to generate in a form optimized for its own subsequent ingestion. Development is partly the progressive refinement of output format. The babbling infant is not practicing motor commands --- it is calibrating the generator's output format against returning sensation. Inner speech may be specifically useful because linguistic tokens are a format co-optimized with the machinery that runs on them --- language is not just a communication tool but an internal representational technology that makes the generator more effective at conditioning on its own output.

### Behavior

Behavior occupies a unique position in the framework: it is the entire reason the system exists, but it is computationally invisible to the system that produces it. The neural activity that generates each perceptual-cognitive state also drives muscles, glands, and autonomic pathways --- by anatomy, not by computation. The generator does not compute motor commands as outputs. It generates experience. Behavior happens because the tissue that generates experience is connected to effectors.

The consequences of behavior return to the system only as ordinary sensation, indistinguishable from any other input. The system's own speech arrives as audition. The visual consequences of its movements arrive as vision. The proprioceptive consequences of its grasps arrive as somatosensation. There is no action-feedback channel, no efference copy that the system can introspect on. The system never observes what it does. It only experiences what comes back.

This indirection is the architecture. The system optimizes over what it can see --- its own generated experiential trajectory --- for outcomes it cannot see --- the behavioral consequences that exit the body and change the world. It can only learn to generate states that tend to produce favorable returning sensation. This is why credit assignment is hard, why delayed consequences are difficult to learn from, why immediate reinforcement is so much more effective than delayed reinforcement, and why superstitious behavior exists. The system is learning from temporal contiguity in a stream where self-caused and world-caused sensation were never distinguished.

---

## Empirical Evidence

### 74 Phenomena, One Principle

The autoregressive framework is not a theory of one domain. It generates specific, testable accounts across the full range of cognitive phenomena --- behavioral, psychological, neurophysiological, and neuroanatomical.

In **language**, the framework explains garden-path sentences, incremental parsing, structural priming, and the N400 as natural consequences of serial commitment to generated continuations. In **memory**, it accounts for false memories, context-dependent recall, reconsolidation, serial position effects, and the dissolution of the short-term/long-term distinction --- all without positing separate storage systems. In **perception and consciousness**, it explains change blindness, perceptual completion, binocular rivalry, and the stream of consciousness as properties of a system that generates rather than records experience. In **imagery and thought**, mental rotation, mental scanning, and the shared neural substrates of memory and imagination follow from the same generative process running under different constraints. The framework extends to **deliberation and reasoning** (reframing System 1/System 2 as low- vs. high-depth generation), **social cognition** (stereotypes as distributional priors), **aesthetics** (the pleasure of well-constrained generation), and **clinical phenomena** including schizophrenia, confabulation, PTSD, and aphasia. At the **neural level**, it reinterprets feedback-dominant cortical connectivity, gamma-band dynamics, hippocampal replay, and place cells as components of the autoregressive architecture.

74 phenomena across 12 domains, unified under a single computational principle.

<a href="/blog/2026/04/phenomena-explained-by-autoregressive-theory/" class="btn">Explore All 74 Phenomena &rarr;</a>

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
