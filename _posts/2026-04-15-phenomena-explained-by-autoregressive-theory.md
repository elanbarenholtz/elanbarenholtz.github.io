---
layout: post
title: "Comprehensive List: 74 Phenomena Explained by Autoregressive Theory"
date: 2026-04-15
tags: [autoregressive-cognition, theory, evidence, phenomena, unification]
description: "A complete compilation of 74 cognitive, neural, and behavioral phenomena unified under the autoregressive theory of cognition — from language processing and memory to consciousness and clinical disorders."
---

The autoregressive brain framework proposes a single computational principle underlying cognition: each mental state is generated as the optimal continuation of the preceding trajectory. Below is the full compilation of phenomena this principle explains.

---

## Language Phenomena

**1. Garden-path sentences** — Mandatory commitment to single parse, costly reanalysis when wrong (e.g., "The horse raced past the barn fell")

**2. Incremental parsing** — Each word processed as it arrives; architectural necessity, not choice

**3. Structural priming** — Recent syntactic structures bias subsequent generation

**4. N400** — Neural signature of prediction error; graded metabolic cost for low-probability continuations

**5. Lexical ambiguity resolution** (Swinney) — Brief activation of multiple meanings, then commitment to one

**6. Distance-dependent decay** — Longer syntactic dependencies are harder to maintain

**7. Arrow of time in language** — Forward generation easy, backward extremely difficult

---

## Memory Phenomena

**8. Episodic memory as generation** — "Remembering" isn't replay of stored episodes; it's autoregressive generation seeded by cues. Explains why memory is sequential, constructive, and shares machinery with imagination. The temporal unfolding IS the memory, not a byproduct of retrieval.

**9. False memories** (DRM paradigm, War of the Ghosts) — Memory IS generation along learned trajectories; confident false memories emerge naturally

**10. Priming** (repetition, semantic, perceptual) — Residual activation biases subsequent generation + weight modification

**11. Serial position effects** (primacy/recency) — Single system with activation gradient, not two stores

**12. Temporal contiguity in recall** — Items recalled in temporal clusters; each output seeds next (this IS autoregressive generation)

**13. Reconsolidation** — "Reactivating" memory = regenerating it, which naturally allows updating

**14. Context-dependent memory** — Generation depends on current state; context effects are inherent

**15. Extended context** — Discourse coherence beyond 7±2 items; two thresholds (explicit retrieval vs generative influence)

**16. Unification of STM/LTM** — Not separate stores; same generative system at different timescales

**17. Continual distractor free recall** — Destroys buffer models; recency without buffer

**18. IQ-STM correlation** — Both reflect same underlying capacity for maintaining extended context

**19. Rehearsal** — Trajectory strengthening through repeated generation, not transfer between stores

**20. Amnesia dissociations (H.M., Clive Wearing)** — The preserved/impaired dissociation in dense amnesia doesn't require separate episodic and procedural memory systems. What's lost is not the ability to generate sequences, but the ability to generate when the current step depends on information from beyond the local context window. What survives — piano playing, mirror tracing, conversational turns — are trajectories where each step depends only on immediately preceding steps (locally Markovian). What fails is any task requiring long-range dependencies: integrating information from minutes ago, building on earlier parts of a conversation, knowing what you just learned. The procedural/episodic distinction is thus not about memory systems but about dependency distance.

**21. Hippocampus as dependency-bridging mechanism** — Short-range sequential dependencies can be handled via STDP-based cortical/cerebellar chaining: each step directly predicts the next through local synaptic connections within the STDP temporal window. But when generating the current step requires information from beyond that window — when there's no local chain connecting now to then — the hippocampus provides the bridging mechanism. It maintains earlier trajectory elements in active form so they can constrain current generation across temporal gaps that STDP cannot span. H.M. and Clive Wearing lost this bridging capacity, leaving them limited to locally-Markovian trajectories. This reframes hippocampal function: not a gateway to a separate memory system, but an attention-like mechanism that extends effective dependency range — functionally analogous to what attention heads do in transformers. Supported by: hippocampal recruitment increasing with temporal gaps between to-be-associated stimuli; time cells encoding elapsed durations in the seconds range; CA3 integrating sequential items within shared context representations.

**22. Working memory as perceptual-generative loop (CSA)** — The "phonological loop" and "visuospatial sketchpad" are not memory stores but self-triggered reactivation of perceptual processing. Cortical sustained activity (CSA) in the seconds range re-invokes sensory/perceptual representations — you literally re-hear or re-see the content. But this reactivation doesn't feed a separate "workspace" — it feeds back into the one generative process as input. "Holding in mind" = generating perception internally = providing short-range context for continued generation. Rehearsal is a perceptual-generative loop: generate, perceive (internally), generate... This dissolves Baddeley's architecture: there are no slave systems feeding a central executive, just perceptual systems that can be self-triggered, feeding the same autoregressive process that handles everything else. Capacity limits reflect perceptual processing bandwidth, not storage slots. Articulatory suppression disrupts the phonological loop because it competes for the same sensory/motor resources, not because it blocks access to a store.

---

## Perception & Consciousness

**23. Perceptual completion** (blind spot filling, phonemic restoration) — Generation fills gaps based on learned patterns

**24. Change blindness** — We don't store detailed representations; we generate on demand

**25. McGurk effect** — Top-down generation influences perceptual experience

**26. Stream of consciousness** — Continuity = chain of autoregressive generation; James's "stream" is literally the generative flow

**27. The specious present** (~3 sec) — Consciousness = moving context window; "now" = current span of active context

**28. Binocular rivalry** — Commitment to one interpretation, periodic switching (temperature-driven exploration)

---

## Imagery, Memory & Thinking

*Core claim: "Thinking" is self-generated autoregressive streams without (or with weak) sensory grounding. Imagery, episodic memory, dreams, deliberation, planning, daydreaming are all the same process under different conditions.*

**29. Mental imagery** — Generation without current sensory input; same system as perception, different conditions

**30. Mental rotation** (Shepard & Metzler) — NOT rotating a 3D mental model; generating the learned visual sequence of how objects look as they rotate. Linear time cost = more sequence to generate. Dissolves Kosslyn vs. Pylyshyn debate: Pylyshyn said it feels like running a movie but that's epiphenomenal (real computation is propositional). We say: it feels like running a movie because you ARE running a movie. The phenomenology IS the computation. Neither pictorial representation nor propositional manipulation, just trajectory generation.

**31. Mental scanning** (Kosslyn) — Generating the visual trajectory of scanning across a learned scene; time proportional to "distance" because more trajectory to generate

**32. Imagery-perception overlap** — Same generative system; imagery = unconstrained generation, perception = input-constrained generation

**33. Dreams** — Generation without sensory grounding and with weak executive control. Same process as imagery and episodic memory, but unconstrained. Bizarreness = no input to correct implausible continuations. Narrative structure = still autoregressive. Discontinuities = context collapse and restart.

**34. Daydreaming/mind-wandering** — Free-running generation from own output; default mode when external input doesn't constrain

**35. Planning/prospection** — Generating possible future trajectories; same machinery as episodic memory but running into unexperienced territory

**36. Deliberation** — Controlled generation with evaluation; running multiple trajectory branches before committing

**37. Inner speech** — Linguistic trajectory generation without vocalization; thinking in words is generating words

---

## Everyday Phenomenology

**38. Tip-of-tongue states** — Stalled trajectory; partial activation insufficient to complete generation

**39. Deja vu** — Near-miss reactivation; current input partially matches learned trajectory, generating false sense of continuation

**40. Freudian slips** — Wrong trajectory completion; highly activated alternative wins over intended continuation

**41. Musical earworms** — Attractor basin loops; melodies that reenter their own continuation space, self-perpetuating

**42. Sudden insight** — Trajectory suddenly finds high-coherence path after exploration; "aha" = landing on strong attractor

---

## System 1/2 & Deliberation

**43. System 1 (fast/automatic)** — Default autoregressive generation; follows strongest learned trajectories

**44. System 2 (slow/deliberate)** — Controlled autoregression; holding elements in workspace, generating multiple branches before committing

**45. Cognitive load effects** — Limited capacity for maintaining multiple trajectory branches simultaneously

---

## Learning & Pedagogy

**46. The testing effect / generation effect** — Passive review is not generation. Re-reading provides external scaffolding that carries the reader to the output without their generative system running. Retrieval practice forces the system to bootstrap from degraded context, actually running the generative process and thereby strengthening the underlying structure. "Desirable difficulty" is just the phenomenology of effortful generation under sparse context. This explains why self-testing produces durable learning and re-reading does not, at a mechanistic rather than merely empirical level.

---

## Social Cognition & Bias

**47. Confirmation bias** — Committed interpretation biases what gets generated; trajectory attracts consistent evidence

**48. Belief perseverance** — Costly to regenerate from different starting point; sunk cost in current trajectory

**49. Functional fixedness** — Committed to one object interpretation; hard to regenerate alternative uses

**50. Cognitive dissonance** — Conflicting committed trajectories create tension; resolution = aligning them

**51. Post-choice spreading** (Sharot) — After commitment, trajectory divergence increases; chosen option's trajectory strengthened

**52. Anchoring** — Initial value seeds generation; subsequent estimates are continuations from anchor

**53. Hindsight bias** — Current knowledge contaminates regeneration of past state; can't uncommit from what you now know

---

## Aesthetics

**54. Musical tension and release** — Controlled trajectory curvature; tension = departure from expected path, release = return

**55. Rhythm** — Temporal scaffolding for generation; provides predictable structure to deviate from

**56. Humor/jokes** — Low-probability continuation under coherence constraint; punchline as trajectory jump that retrospectively fits

**57. Catchiness** — Melodies with high autogenerative potential; they complete themselves

---

## Clinical Phenomena

**58. Schizophrenia (positive symptoms)** — Dysregulated generation; temperature too high, weak constraint from input

**59. Depression (rumination)** — Stuck in negative attractor basins; same trajectories regenerate repeatedly

**60. OCD** — Compulsive trajectory completion; incomplete actions demand finishing

**61. Anxiety** — Threat-biased generation; negative continuations more accessible

**62. PTSD intrusions** — Trauma trajectories have extremely strong weights; easily triggered, hard to escape

**63. Confabulation** — Generation proceeds without adequate constraint; produces confident false content

---

## Consciousness

**64. Unity of consciousness / binding problem dissolved** — Unity is not constructed from parts; it's intrinsic to global autoregressive computation. Each generation step is holistically unified. There's nothing to bind because there are no separate fragments. The binding problem was an artifact of the wrong computational model.

**65. Subjectivity / first-person perspective** — Arises from recursive self-input. The system's own outputs become part of its input context. "The 'I' is the felt shape of recursion." Consciousness is what recursive global computation feels like from within.

**66. The hard problem reframed** — Subjective experience isn't added to computation. The recursive, self-reading, holistic generation IS the experience. The phenomenology is the computation (same insight as mental imagery).

**67. Attention as weighting, not binding** — Attention doesn't unify separate streams; it tunes the balance of contributions within already-unified global computation.

**68. Phenomenology as generative input** — Conscious experience is the processed, interpreted output of generative inference in its role as input to the next generative step. We perceive objects, depth, causation, phonemes — not pixels and pressure waves — because these are the formats that feed forward into behavioral generation. The format of phenomenology is the format of generative context. Subjectivity doesn't "arise" from this computation — it is this computation. Egocentric, action-formatted information serving as input to behavioral generation just IS first-person experience.

---

## Neural Validation

**69. Schrimpf et al. (2021)** — GPT-2 predicts brain activity during language processing

**70. Goldstein et al. (2022)** — Shared computational principles between LLMs and neural responses

**71. Caucheteux & King (2022)** — Autoregressive models predict comprehension

**72. Hosseini et al. (2024)** — Works even with child-scale training data

**73. Ruchkin et al.** — Sustained activation predicts LTM encoding

**74. Daume et al.** — Delay period activity predicts subsequent memory

---

## Summary: 74 Phenomena, One Principle

All of these are autoregressive generation under different conditions:

- **With/without sensory input** (perception vs. imagery vs. thinking)
- **With/without executive control** (System 2 vs. System 1)
- **With different temperature settings** (exploration vs. exploitation)
- **With different context lengths** (simple vs. complex tasks)
- **With intact vs. disrupted mechanisms** (normal vs. clinical)
- **With recursive self-inclusion** (consciousness, subjectivity)

### Key Unifications

Imagery, episodic memory, dreams, daydreaming, planning, deliberation, and inner speech are all "thinking" = self-generated autoregressive streams without sensory grounding.

Unity and subjectivity of consciousness are intrinsic to recursive global autoregressive computation, not added features.

Phenomenology is the format of generative context — egocentric, action-formatted, serving behavioral generation.

**The theory's power is unification**: these aren't 74 separate explanations. They're 74 manifestations of one process.
