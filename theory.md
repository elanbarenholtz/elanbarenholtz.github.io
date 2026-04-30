---
layout: page
title: The Autoregressive Brain
subtitle: A new framework for cognition, memory, and language
permalink: /theory/
---

<div class="prose" markdown="1">

## The Problem with Storage-Retrieval

For over a century, cognitive science has assumed that memory works like a warehouse: experiences are encoded, stored, and later retrieved. But this storage-retrieval model has always struggled with basic facts about how memory actually behaves --- its reconstructive nature, its sensitivity to context, its seamless integration with imagination and prediction.

Every time you "remember" something, you reconstruct it. The memory changes depending on your current mood, the question someone asks, the context you're in. Sometimes you remember things that never happened. Sometimes you can't retrieve something you definitely know. These aren't bugs in a storage system --- they're fundamental features of a generative one.

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

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.2/es5/tex-mml-chtml.min.js"></script>

*A formal statement of the core claims, architecture, and consequences*

Cognition is the operation of a single, multimodal, recursively closed generator. At each moment the system produces an output conditioned on its own prior output and on current sensation. Perception, memory, action, and language are not distinct faculties. They are aspects of this single generative process.

### The Universal Cognition Operator

The complete operational cycle of cognition is a single mapping \\(\mathcal{K}\\):

$$(W_{t+1},\; C_{t+1},\; y_t) = \mathcal{K}(W_t,\; C_t,\; y_{t-1},\; E_t)$$

The system's current output and its next internal state are jointly determined by these arguments. There are no other inputs, outputs, or state variables. Everything cognition does is an instance of \\(\mathcal{K}\\).

| Symbol | Definition |
|--------|----------|
| \\(\mathcal{K}\\) | The complete operational cycle. Everything the system does is one application of this operator, repeated. |
| \\(y_t\\) | The system's output: percepts, inner speech, efference copies, and any other internally generated content. Motor commands as received by the body are not included --- they exit the loop. |
| \\(y_{t-1}\\) | Prior output, fed back as the conditioning substrate for the next cycle. This is what makes the system autoregressive. |
| \\(E_t\\) | Exogenous sensation: raw input from the environment and body, including sensory consequences of the system's own prior motor activity. |
| \\(W_t\\) | Slow structure: the cumulative shaping of connectivity by the system's history. Modified continuously during operation --- no separate training regime. |
| \\(C_t\\) | Fast state: transient activation carrying immediate sequence context. Decays on short timescales. |

### Core Claims

**01. Perception is output, not input.** The system generates percepts; it does not receive them. Sensation (\\(E_t\\)) arrives; the percept (\\(y_t\\)) is produced. These are not the same thing.

**02. Autoregression is forced, not chosen.** The structure that matters for behavior is temporally extended and not present in any instantaneous slice of sensation. It must be generated. A cognitive system is autoregressive or it is not cognitive.

**03. Behavior is not in the loop.** Motor commands exit to the body and return only as sensation. The system is structurally always a brain in a vat --- it issues impulses, and what gets reinforced is whatever returns as favorable sensation. The resulting behavior is beyond its computational purview.

**04. Memory is the loop, not storage.** \\(C\\) carries the recent trajectory of generation. \\(W\\) accumulates shaping from many cycles. Neither is storage. The loop remembers by continuing.

**05. Memory operates over generated content.** In Sperling's partial report, subjects retain letters, not retinal patterns. Working memory tracks disambiguated percepts, not ambiguous inputs. Illusory contours, McGurk percepts, apparent motion: memory everywhere preserves the generated output, not the sensory input.

**06. Covert and overt are the same operation.** Imagining an action and performing it differ only in whether the motor channel produces environmental effects. Inner speech, mental imagery, covert rehearsal: computationally identical to their overt counterparts.

**07. Language and perception are the same architecture.** Tokens are to linguistic autoregression as percepts are to perceptual autoregression. Language did not introduce autoregression into cognition --- it plugged into preexisting machinery already generating perceptual sequences.

**08. LLMs are not simulating cognition.** They are running the linguistic case of the architecture cognition runs.

**09. Learning is continuous.** Every cycle of the loop is also a cycle of structural modification. There is no inference regime distinct from a learning regime. \\(W\\) is reshaped during operation, not in a separate phase.

**10. The system optimizes on two targets, one external and one internal.** External: shape \\(W\\) to favor trajectories whose motor consequences return as reinforcing sensation. Internal: shape \\(W\\) to generate \\(y_t\\) in a format that the system's own generative machinery can most effectively condition on. This second target is entirely within the loop. The representational format of the output is itself a learned quantity --- the system does not just learn what to generate, it learns how to generate in a form optimized for its own subsequent ingestion. Perception improves not only by representing the world more accurately but by representing it in the format the generative machinery needs. Inner speech may be specifically useful because linguistic tokens are a format that has been co-optimized with the machinery that runs on them. Development, on this view, is partly the progressive refinement of output format, not just the accumulation of knowledge.

> Perception, memory, action, learning, language, reasoning, and imagination are all the same operation seen from different angles or at different timescales. All of these are \\(\mathcal{K}\\).

### Why This Architecture

Behavior must be conditioned on a coherent sequential substrate, because the structure that matters for behavior lives in the temporal flow of experience, not in any instantaneous slice of it. Objects, events, actions, utterances, intentions, affordances: none of these are present in \\(E_t\\) at a single moment. They are constituted across time.

Not all temporally sensitive processing requires autoregression. Sensation-local filters --- Reichardt-style motion detection, onset and offset responses --- extract features directly from \\(E\\). These are real and biologically widespread. What they cannot do is build trajectories, track content across gaps in sensation, or generate structure the signal does not contain. Cognition is the regime that does.

The move from sensation-local processing to autoregressive generation is a real architectural transition. It also provides a principled axis for ordering cognitive capacity across species: by the depth and richness of autoregressive machinery.

### Contrast: Predictive Coding

**Predictive coding** holds that the brain continuously generates predictions of its next input, compares them to actual input, and propagates prediction error upward through a processing hierarchy. Feedback carries predictions; feedforward carries errors. Error minimization is the fundamental currency of both perception and learning.

**The autoregressive theory** rejects this architecture. There is no dedicated predictive engine, no explicit error computation, no free-energy functional being minimized. Generation is implicitly sensitive to statistical regularities without requiring anticipation and comparison as a structural feature.

The appearance of prediction-like behavior --- expectation effects, surprise responses, adaptation to statistical structure --- is produced by a generative process whose structure \\(W\\) has been shaped by past regularities. When sensation fits poorly with that structure, the generative process is more disrupted. Neural responses scale with degree of violation as a natural consequence, without requiring explicit error-computing architecture.

Explicit prediction is a generated behavior --- one output among many --- not a continuously running architectural feature. The brain does not have a prediction engine. It has a generator that can, among other things, produce predictions.

### The Physiology: A Sketch

Cortex is characterized by dense feedback projections running from higher-order to lower-order regions, typically outnumbering feedforward connections. The standard interpretation under predictive coding: feedback carries top-down predictions to be tested against bottom-up input.

The autoregressive interpretation: feedback carries the prior generative state \\(y_{t-1}\\) as conditioning content for the current cycle. The descending activity is not a prediction waiting to be confirmed. It is the continuation of generation --- the prior output, held partially active and projected back to participate in the next round of computation.

The density of feedback relative to feedforward reflects a deep fact about the loop: the dominant conditioning content in any generative cycle is prior output, not current sensation. Neuromodulatory systems already handle diffuse gain control. The topographically organized, laminar-specific, anatomically dense feedback projections are overengineered for that job. They must be carrying something richer --- a representation of the prior state projected back so the forward pass unfolds in a context shaped by what was just generated.

On this view there is no moment at which sensory regions perform pure feedforward processing. V1's response to a stimulus is always a response in a cortex already shaped by what the system has been generating.

**Plasticity across timescales.** STDP operates at millisecond timescales, differentially strengthening synapses that carried the just-completed activity pattern. Hippocampal sharp-wave ripple replay provides additional shaping of recent trajectories during rest --- not transfer of stored content, but the generator running recent sequences again, reinforcing the cortical patterns they produced. Longer-timescale synaptic remodeling accumulates the durable structure of \\(W\\).

### The Information Geometry of Memory

A further consequence of the autoregressive view concerns the temporal shape of memory accessibility. The standard picture treats forgetting as degradation: representations stored at time of encoding fade with elapsed time, and the forgetting curve measures the rate of that fade. The autoregressive view requires a different account, because there are no stored representations to degrade. What needs explaining is why the influence of past content on current generation declines with distance at all, given that past content is fully expressed in the current state.

The answer is that successive autoregressive steps are compressive. Each generative step preserves what is needed to shape continuation while shedding specificity that does not contribute to the trajectory going forward. After many such steps, what remains of a distant past state is its influence on the trajectory, not the specificity required to reconstruct it. The further back in the chain, the more steps of compression have intervened, and the less of the original specificity survives. This is not loss of stored content. It is the natural information geometry of chained generation.

This account predicts a specific empirical signature. The marginal influence of past content on next-token generation should fall off with distance as a power law rather than an exponential, because the specificity-loss process is scale-free: the proportional reduction in influence per unit distance is constant, not the absolute reduction. Influence of token at distance \\(d\\) should be proportional to \\(d^{-\alpha}\\). We find this signature in human language production, with exponents clustering between \\(-0.69\\) and \\(-0.88\\) across written and spoken corpora spanning eight languages and six language families. Formal model comparison selects the power law over exponential alternatives in 75% of cases. The exponential form, predicted by discrete buffer models of working memory, is not selected by the better-calibrated probe for any dataset.

The same exponent range appears in two independent measurements of memory: Anderson and Schooler's environmental information recurrence statistics (\\(\alpha = -0.77\\)) and Kahana et al.'s associative influence decay in free recall (\\(\alpha = -0.82\\)). Within the storage-and-retrieval view this convergence is mysterious: three different processes --- language statistics, environmental recurrence, episodic recall --- happening to share a decay shape. Within the autoregressive view it is expected: all three are measurements of the same underlying process, the compression of generative trajectory information under successive chaining. The power law is not a property of memory traces. It is the information-geometric signature of an autoregressive cognitive system observed at the population level.

This also resolves a tension. The autoregressive view denies a separate memory substrate, but explicit recall declines with elapsed time in ways that seem to require fading representations. The resolution is that explicit recall is reconstruction from the current state, and reconstruction depends on enough non-redundant specificity surviving the chain to allow the original state to be regenerated. Recent past has gone through few steps and retains specificity. Distant past has been compressed through many steps; its influence on the trajectory is preserved but the specificity required for reconstruction is not. What looks like decay of stored memories is the specificity-loss function of autoregressive compression, sampled by a reconstruction process that demands more than mere influence.

The forgetting curve, in this framing, is not the rate at which the brain loses what it stored. It is the rate at which an autoregressive system loses the ability to regenerate its own past, given that the past is present only as compressed influence on the current state.

### Open Questions

**Is prior sequence decodable from the forward pass?** The critical experiment: present the same stimuli in different temporal orders and ask whether V1 responses to a fixed probe carry decodable information about the specific prior sequence --- not just the prior stimulus set. Order specificity is the uniquely autoregressive prediction. Predictive coding does not require it.

**Consciousness.** If the autoregressive loop generates the percept stream, and conscious experience is the sequence of percepts the system generates, then consciousness may be specifically the autoregressive loop. Unity of consciousness follows structurally: one generator, one output at each moment. The binding problem dissolves at the architectural level --- components were never separate in the generator --- while the physiological question of how distributed neural processing produces unified \\(y_t\\) remains open.

**The cognitive hierarchy.** Ordering species by the depth and richness of their autoregressive machinery gives a principled account of cognitive complexity. Diagnostic behaviors: object permanence, trace vs. delay conditioning, working memory span, planning horizon, language. The acquisition of autoregressive machinery and the emergence of memory may be the same evolutionary event.

---

## The Evidence: 74 Phenomena, One Principle

This framework doesn't just offer a new metaphor --- it generates specific, testable explanations across the full range of cognitive phenomena. From garden-path sentences to false memories, from mental rotation to musical earworms, from schizophrenia to the binding problem --- 74 phenomena unified under a single computational principle.

<a href="/blog/2026/04/phenomena-explained-by-autoregressive-theory/" class="btn">Explore All 74 Phenomena &rarr;</a>

</div>
