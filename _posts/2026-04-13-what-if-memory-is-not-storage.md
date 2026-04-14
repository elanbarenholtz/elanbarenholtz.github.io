---
layout: post
title: "Memory as Trajectory Regeneration"
date: 2026-04-13
tags: [memory, theory, autoregressive-brain, dynamical-systems]
description: "The storage-retrieval model of memory has dominated cognitive science for over a century. But if the brain is a non-Markovian dynamical system, memory is not retrieval at all — it is the regeneration of trajectories through cognitive state-space."
---

The storage-retrieval model of memory has been the default framework in cognitive science since Ebbinghaus. Experiences are encoded, consolidated into stable representations, and later retrieved. The metaphor shifts with each generation — wax tablets, filing cabinets, hard drives — but the computational claim remains the same: memory is a lookup operation over stored records.

This model has always been in tension with what memory actually does. The autoregressive brain framework offers a different account: memory is not retrieval from storage but the regeneration of trajectories through a high-dimensional cognitive state-space, constrained by distributional structure learned over a lifetime of experience.

## The empirical case against storage-retrieval

The problems with storage-retrieval are not edge cases. They are the central phenomena of memory research:

**Reconstructive distortion.** Bartlett (1932) demonstrated that recall is schematic reconstruction, not faithful playback. Subsequent work on misinformation effects (Loftus, 2005), imagination inflation (Garry et al., 1996), and false memory implantation (Loftus & Pickrell, 1995) has made the point inescapable: the content of a "memory" depends on what happens between encoding and recall. Under a storage model, these phenomena require auxiliary explanations — interference, source monitoring failure, trace degradation. Under a generative model, they are the expected behavior of a system that constructs each output anew.

**Context-dependent recall.** Godden and Baddeley (1975) showed that divers who learned word lists underwater recalled them better underwater than on land, and vice versa. Encoding specificity (Tulving & Thomson, 1973) generalized this: recall depends on the overlap between encoding and retrieval contexts. In storage-retrieval terms, this means retrieval cues must somehow match stored indices. In generative terms, it means the current state of the system — which includes contextual information — seeds the trajectory that gets generated. Different seeds produce different trajectories.

**Memory-imagination overlap.** The neural machinery for episodic memory and prospective imagination is largely shared (Schacter et al., 2012; Hassabis & Maguire, 2007). Amnesic patients who cannot recall their past also cannot imagine novel future scenarios. The constructive episodic simulation hypothesis (Schacter & Addis, 2007) acknowledges this but treats imagination as a *repurposing* of memory systems. The autoregressive account is simpler: remembering and imagining are both trajectory generation. They differ in their constraints — recall is seeded by cues linked to prior experience, imagination by novel or hypothetical prompts — but the generative process is identical.

**Reconsolidation.** Nader et al. (2000) demonstrated that reactivated memories become labile and require reconsolidation, during which they can be modified or disrupted. This makes little sense if memories are stable stored objects being accessed. It makes considerable sense if each act of "remembering" is a new generative event whose output gets folded back into the system's learned structure.

## The generative account

In the autoregressive brain framework, the cognitive system is a non-Markovian dynamical system: each state is the optimized generative outcome of the trajectory of states that preceded it. The system does not store snapshots and retrieve them. It learns distributional structure over experiential trajectories, and it uses that structure to generate new trajectories.

What we call "memory" is the capacity to regenerate a trajectory through cognitive state-space that is similar to a previously traversed trajectory. The fidelity of this regeneration depends on:

1. **The seed.** The current cognitive state provides the starting conditions. Contextual cues, emotional state, sensory input, and the preceding stream of thought all constrain where the trajectory begins.

2. **Learned distributional structure.** The system has learned, over a lifetime, the statistical regularities of experiential sequences. These regularities constrain which trajectories are probable given a particular seed.

3. **The trajectory history.** Because the system is non-Markovian, generation depends not just on the immediately preceding state but on the extended trajectory. This is what gives "memories" their narrative continuity — each generated state is conditioned on the unfolding sequence, not just the last snapshot.

This is not a metaphor. It is a specific computational claim: the operation that produces a "memory" is the same operation that produces every other cognitive state — sequential generation, constrained by learned structure, conditioned on the preceding trajectory.

## Why distortion is the default, not the exception

Under this account, the classic findings of memory research follow directly:

- **Reconstructive distortion** occurs because each recall is a new generation event. The seed differs each time (your current context, mood, and goals are never identical), so the generated trajectory diverges from previous ones. There is no "original" to corrupt — there are only trajectories, each generated under the constraints that happen to be active.

- **Context-dependent recall** occurs because context is part of the seed. Change the context and you change the initial conditions, which changes the trajectory. The information is not "stored" in one location and "inaccessible" from another — the system simply generates different trajectories from different starting points.

- **Memory-imagination overlap** occurs because both are the same process. Remembering your tenth birthday and imagining a birthday party on Mars both involve generating a trajectory through experiential state-space. The constraints differ — one is heavily shaped by prior experiential statistics, the other less so — but the mechanism is identical.

- **Reconsolidation** occurs because generating a trajectory modifies the system. Running a trajectory through a dynamical system is not a read-only operation. The act of generation itself alters the distributional structure, which means subsequent generation from similar seeds will produce subtly different trajectories. Memory is modified by remembering not because the "file" gets corrupted during access, but because generation is inherently a structure-modifying process.

## We already built systems that work this way

Large language models provide a concrete demonstration that this kind of system is computationally viable. An LLM has no explicit memory store. It generates each token as a function of the preceding context, constrained by distributional patterns learned during training. Yet it produces outputs that exhibit memory-like properties: contextual consistency, narrative coherence, sensitivity to prior "experience" within the context window.

The parallel is not that the brain *is* an LLM. The architectures differ enormously. The parallel is that autoregressive generation over learned distributional structure is *sufficient* to produce memory-like behavior without storage or retrieval. If next-token prediction can do this in silicon, we should take seriously the hypothesis that next-state prediction does it in neural tissue — and investigate what the non-Markovian, continuous, embodied version of this principle looks like.

## What this reframes

If memory is trajectory regeneration rather than storage-retrieval, several long-standing puzzles dissolve:

- **Forgetting** is not trace decay or interference with stored records. It is the divergence of generated trajectories over time as the system's distributional structure continues to evolve with ongoing experience.
- **Flashbulb memories** are not specially encoded snapshots. They are trajectories that are easy to regenerate because the emotional and contextual conditions that seed them are distinctive and frequently reactivated.
- **Childhood amnesia** is not the loss of early stored memories. It is the inability to generate trajectories consistent with early experience, because the distributional structure of the system has been so thoroughly reshaped by subsequent development.
- **Expertise effects on memory** — experts remember domain-relevant information better not because they store it more efficiently, but because their distributional structure over that domain is richer, supporting more constrained and therefore more faithful trajectory generation.

None of these reframings require new mechanisms. They follow from a single principle: the brain generates each state as the optimized outcome of the preceding trajectory, and what we call "memory" is one consequence of how that generation process works.
