---
layout: page
title: Formal Statement
subtitle: The mathematical architecture of autoregressive cognition
permalink: /formalism/
---

<div class="prose" markdown="1">

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.2/es5/tex-mml-chtml.min.js"></script>

*A formal statement of the core claims, architecture, and consequences*

Cognition is the operation of a single, multimodal, recursively closed generator. At each moment the system produces an output conditioned on its own prior output and on current sensation. Perception, memory, action, and language are not distinct faculties. They are aspects of this single generative process.

### The Universal Cognition Operator

The complete operational cycle of cognition is a single mapping \\(\mathcal{K}\\):

$$(W_{t+1},\; C_{t+1},\; y_t) = \mathcal{K}(W_t,\; C_t,\; y_{t-1},\; E_t)$$

The system's current output and its next internal state are jointly determined by these arguments. There are no other inputs, outputs, or state variables. Everything cognition does is an instance of \\(\mathcal{K}\\).

| Symbol | Definition |
|--------|-----------|
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

</div>
