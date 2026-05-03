---
layout: page
title: Formal Statement
subtitle: The mathematical architecture of autoregressive cognition
permalink: /formalism/
---

<div class="prose" markdown="1">

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.2/es5/tex-mml-chtml.min.js"></script>

<style>
.theory-tabs { display: flex; gap: 0; margin-bottom: 2rem; border-bottom: 2px solid #e2e8f0; }
.theory-tab { padding: 0.75rem 1.5rem; text-decoration: none; font-weight: 600; color: #718096; }
.theory-tab--active { color: #2d3748; border-bottom: 3px solid #2d3748; margin-bottom: -2px; }
</style>

<div class="theory-tabs">
  <a href="/theory/" class="theory-tab">Overview</a>
  <a href="/formalism/" class="theory-tab theory-tab--active">Formal Statement</a>
</div>

The entire theory reduces to one equation:

#### The Generator

$$y_t = \mathcal{G}(W_t,\; C_t,\; y_{t-1},\; E_t)$$

At each moment the system produces a new state \\(y_t\\). This state is the system's generated experience: percepts, thoughts, inner speech, imagery. It is the perceptual-cognitive token --- what the system produces and what it ingests on the next cycle. The system does not distinguish between "I am perceiving" and "I am thinking" at the point of generation. It just generates its next experience.

The generated state \\(y_t\\) is conditioned on:

- \\(y_{t-1}\\) --- the system's own prior output, fed back as the primary conditioning substrate. **This is what makes the system autoregressive.**
- \\(E_t\\) --- current sensation, arriving from the environment and body. The output of the brain's extensive parallel processing, funneled into the generator.
- \\(C_t\\) --- fast state: transient activation carrying the recent trajectory of generation.
- \\(W_t\\) --- slow structure: the cumulative shaping of connectivity by the system's history.

Each \\(y_t\\) feeds back into the next cycle as \\(y_{t-1}\\). The system's input is what it has already produced --- its own prior experience, not its prior behavior.

The generator does not compute behavior. Motor commands, hormonal signals, autonomic activation --- these are consequences of the neural activity that produces \\(y_t\\), not outputs of the generator itself. The same tissue that generates experience is connected, via anatomy, to muscles and glands. That connectivity has consequences in the world and body. But from the computational perspective of the autoregressive loop, those consequences are invisible until they return as sensation.

The system never feels a motor command. It feels the position of its limb --- proprioception processed into a percept. It never feels sympathetic activation directly. It feels its heart racing --- interoception processed into a percept. The only thing the system ever ingests is its own perceptual output.

#### The Environment

$$E_{t+1} = \text{Env}(E_t,\; a_t)$$

where \\(a_t\\) denotes the behavioral consequences of the neural activity underlying the generation of \\(y_t\\). The world evolves, partly in response to whatever the body did as a consequence of the most recent generative cycle. The perceptual consequences of those actions return as ordinary sensation \\(E_{t+1}\\). There is no action-feedback channel. The system's own speech, the visual consequences of its movements, the tactile results of its grasps --- all arrive as \\(E\\), indistinguishable in kind from any other sensation. The system never observes its own behavior. It only experiences what comes back.

#### State Updates

$$C_{t+1} = f_C(C_t,\; y_t)$$

$$W_{t+1} = f_W(W_t,\; y_t,\; E_t)$$

Every cycle of generation is simultaneously a cycle of encoding and learning. \\(C\\) is updated with the current trajectory; \\(W\\) is reshaped by the current activity. There is no separate write operation, no distinct training phase. The act of generating the current state *is* the encoding of that state into the system's structure.

| Symbol | Definition |
|--------|-----------|
| \\(\mathcal{G}\\) | The generator. Every cognitive act is one application of this operator. |
| \\(y_t\\) | The system's generated experience: percepts, thoughts, inner speech, imagery. The perceptual-cognitive token. Everything the system experiences in a single cycle. Does not include motor or autonomic outputs, which are downstream consequences of the neural activity underlying generation. |
| \\(y_{t-1}\\) | Prior generated experience, fed back as the primary conditioning substrate. This is what makes the system autoregressive. |
| \\(E_t\\) | Exogenous sensation: input from the environment and body, including the perceptual consequences of the system's own prior behavior. Sensation is not perception --- it is raw input that the generator processes into the perceptual content of \\(y_t\\). |
| \\(a_t\\) | Behavioral output: motor commands, hormonal signals, autonomic activation. These are consequences of the neural activity that produces \\(y_t\\), not computed outputs of the generator. The system has no direct access to \\(a_t\\). |
| \\(W_t\\) | Slow structure: cumulative shaping of connectivity. Modified continuously during operation. No separate training regime. |
| \\(C_t\\) | Fast state: transient activation carrying recent trajectory. Decays on short timescales. |

---

### Core Claims

**01. Behavior is a consequence of generation, not a computed output.** The neural activity that produces each perceptual-cognitive state \\(y_t\\) also drives muscles, glands, and autonomic pathways --- by anatomy, not by computation. The system does not generate motor commands as outputs of the autoregressive loop. It generates experience. Behavior happens because the tissue that generates experience is connected to effectors. The consequences of that behavior return as ordinary sensation, indistinguishable from any other input.

**02. The sequence is self-generated.** The sequence over which cognition operates is the system's own prior output. This is what makes it autoregressive. Perception is the system generating its processed version of the world, informed by sensation but not identical to it. Thought is the same process with sensation playing a lesser role. Both are instances of the system feeding itself the processed output of the previous cycle as input to the next.

**03. Perception is output, not input.** Sensation \\(E_t\\) arrives; the percept \\(y_t\\) is produced. These are not the same thing. What the system "sees" is what it generates, not what it receives. Sensation constrains generation but does not constitute it. This is why illusions, filling-in, amodal completion, and inattentional blindness exist: perception is authored by the system, not delivered to it.

**04. Attention is the autoregressive process itself.** The serial nature of conscious experience is not a limitation imposed by a bottleneck or a resource constraint. It is a structural necessity: multiple modalities converge into the generation of a single next state \\(y_t\\). Attention is this convergence. The system can only generate one \\(y_t\\) at a time, and what we call "attending" to something is that thing dominating the current generation step. Inattentional blindness is not a failure to notice --- it is a failure to generate.

**05. The system has no direct access to its own behavior.** The system generates experience; behavior is a downstream consequence of the neural activity underlying that generation. The system never observes \\(a_t\\) --- it only experiences \\(E_{t+1}\\), the sensation that returns. It cannot distinguish self-caused sensation from world-caused sensation. Optimization occurs because temporal contiguity in the trajectory provides statistical structure: states that tend to be followed by favorable sensation get reinforced in \\(W\\). But the system never learns "when I do X, Y happens." It learns "states like this tend to be followed by sensation like that." Attribution of agency is itself a generated construct --- a compression of trajectory regularities into an efficient token, not a report from a privileged self-monitoring channel.

**06. Memory is continuous encoding.** There is no discrete storage event, no separate write operation. Every cycle of the generator simultaneously produces the current state and encodes it into the system's structure --- \\(C\\) is updated with the current trajectory, \\(W\\) is reshaped by the current activity. Generation *is* encoding.

**07. Memory is influence, not storage.** The past shapes current generation through the trajectory, not through retrieval from a store. Remembering is regeneration: the system produces a trajectory through state-space that recapitulates an earlier one, constrained by available cues. This is why memories are context-sensitive, malleable, and continuous with imagination --- generation and "retrieval" are the same process with different seeds.

**08. The short-term/long-term distinction dissolves.** There are not two memory systems. There is influence at different timescales. \\(C\\) carries influence that decays over seconds --- what is traditionally called working memory. \\(W\\) carries influence that persists across a lifetime --- what is traditionally called long-term memory. The difference is the time constant of the substrate, not the nature of the operation. The forgetting curve is not the rate at which the brain loses what it stored. It is the rate at which successive autoregressive compression reduces the specificity needed for regeneration.

**09. A single optimization process shapes both the trajectory and its format.** \\(W\\) is continuously modified by a process that jointly achieves two outcomes. First, it shapes the system to generate experiential states that tend to be followed by favorable returning sensation --- this is behavioral optimization, achieved indirectly through temporal contiguity. Second, it shapes the system to generate \\(y_t\\) in a format that the generator can most effectively condition on in the next cycle --- this is representational optimization, entirely within the loop. The system does not just learn *what* to generate; it learns *how* to generate in a form optimized for its own subsequent ingestion. Development is partly the progressive refinement of output format. Inner speech may be specifically useful because linguistic tokens are a format co-optimized with the machinery that runs on them.

**10. Consciousness is the autoregressive stream.** The serial, contextual sequence of generated states \\(y_t\\) is not merely correlated with conscious experience. It *is* conscious experience. Unity of consciousness follows structurally: one generator, one output at each moment. The stream quality of experience follows from the autoregressive dependence of each state on its predecessor. The binding problem dissolves at the architectural level --- components were never separate in the generator. What enters the generated sequence is conscious; what remains in \\(E\\) without being integrated into \\(y\\) is not. Attention and consciousness are the same thing: the funneling of parallel state into serial generation. The deeper question --- why this architecture constitutes subjectivity --- is addressed in the <a href="/theory/#consciousness">full theoretical treatment</a>.

> Perception, memory, learning, language, reasoning, consciousness, and imagination are all instances of \\(\mathcal{G}\\) --- the same operation seen from different angles or at different timescales. Behavior is a consequence of that operation, not a separate computation. Cognition is one equation.

---

### Why This Architecture

Behavior must be conditioned on a coherent sequential substrate, because the structure that matters for behavior lives in the temporal flow of experience, not in any instantaneous slice of it. Objects, events, actions, utterances, intentions, affordances: none of these are present in \\(E_t\\) at a single moment. They are constituted across time.

The move from sensation-local processing to autoregressive generation is a real architectural transition. It also provides a principled axis for ordering cognitive capacity across species: by the depth and richness of autoregressive machinery.

---

### Contrast: Predictive Coding

**Predictive coding** holds that the brain continuously generates predictions of its next input, compares them to actual input, and propagates prediction error upward through a processing hierarchy. Feedback carries predictions; feedforward carries errors. Error minimization is the fundamental currency of both perception and learning.

**The autoregressive theory** rejects this architecture. There is no dedicated predictive engine, no explicit error computation, no free-energy functional being minimized. Generation is implicitly sensitive to statistical regularities without requiring anticipation and comparison as a structural feature.

The appearance of prediction-like behavior --- expectation effects, surprise responses, adaptation to statistical structure --- is produced by a generative process whose structure \\(W\\) has been shaped by past regularities. When sensation fits poorly with that structure, the generative process is more disrupted. Neural responses scale with degree of violation as a natural consequence, without requiring explicit error-computing architecture.

Explicit prediction is a generated behavior --- one output among many --- not a continuously running architectural feature. The brain does not have a prediction engine. It has a generator that can, among other things, produce predictions.

---

### The Physiology: A Sketch

Cortex is characterized by dense feedback projections running from higher-order to lower-order regions, typically outnumbering feedforward connections. The standard interpretation under predictive coding: feedback carries top-down predictions to be tested against bottom-up input.

The autoregressive interpretation: feedback carries the prior generative state \\(y_{t-1}\\) as conditioning content for the current cycle. The descending activity is not a prediction waiting to be confirmed. It is the continuation of generation --- the prior output, held partially active and projected back to participate in the next round of computation.

The density of feedback relative to feedforward reflects a deep fact about the loop: the dominant conditioning content in any generative cycle is prior output, not current sensation. Neuromodulatory systems already handle diffuse gain control. The topographically organized, laminar-specific, anatomically dense feedback projections are overengineered for that job. They must be carrying something richer --- a representation of the prior state projected back so the forward pass unfolds in a context shaped by what was just generated.

On this view there is no moment at which sensory regions perform pure feedforward processing. V1's response to a stimulus is always a response in a cortex already shaped by what the system has been generating.

**Plasticity across timescales.** STDP operates at millisecond timescales, differentially strengthening synapses that carried the just-completed activity pattern. Hippocampal sharp-wave ripple replay provides additional shaping of recent trajectories during rest --- not transfer of stored content, but the generator running recent sequences again, reinforcing the cortical patterns they produced. Longer-timescale synaptic remodeling accumulates the durable structure of \\(W\\).

---

### The Information Geometry of Memory

A further consequence of the autoregressive view concerns the temporal shape of memory accessibility. The standard picture treats forgetting as degradation: representations stored at time of encoding fade with elapsed time, and the forgetting curve measures the rate of that fade. The autoregressive view requires a different account, because there are no stored representations to degrade. What needs explaining is why the influence of past content on current generation declines with distance at all, given that past content is fully expressed in the current state.

The answer is that successive autoregressive steps are compressive. Each generative step preserves what is needed to shape continuation while shedding specificity that does not contribute to the trajectory going forward. After many such steps, what remains of a distant past state is its influence on the trajectory, not the specificity required to reconstruct it. The further back in the chain, the more steps of compression have intervened, and the less of the original specificity survives. This is not loss of stored content. It is the natural information geometry of chained generation.

This account predicts a specific empirical signature. The marginal influence of past content on next-token generation should fall off with distance as a power law rather than an exponential, because the specificity-loss process is scale-free: the proportional reduction in influence per unit distance is constant, not the absolute reduction. Influence of token at distance \\(d\\) should be proportional to \\(d^{-\alpha}\\). We find this signature in human language production, with exponents clustering between \\(-0.69\\) and \\(-0.88\\) across written and spoken corpora spanning eight languages and six language families. Formal model comparison selects the power law over exponential alternatives in 75% of cases. The exponential form, predicted by discrete buffer models of working memory, is not selected by the better-calibrated probe for any dataset.

The same exponent range appears in two independent measurements of memory: Anderson and Schooler's environmental information recurrence statistics (\\(\alpha = -0.77\\)) and Kahana et al.'s associative influence decay in free recall (\\(\alpha = -0.82\\)). Within the storage-and-retrieval view this convergence is mysterious: three different processes --- language statistics, environmental recurrence, episodic recall --- happening to share a decay shape. Within the autoregressive view it is expected: all three are measurements of the same underlying process, the compression of generative trajectory information under successive chaining. The power law is not a property of memory traces. It is the information-geometric signature of an autoregressive cognitive system observed at the population level.

This also resolves a tension. The autoregressive view denies a separate memory substrate, but explicit recall declines with elapsed time in ways that seem to require fading representations. The resolution is that explicit recall is reconstruction from the current state, and reconstruction depends on enough non-redundant specificity surviving the chain to allow the original state to be regenerated. Recent past has gone through few steps and retains specificity. Distant past has been compressed through many steps; its influence on the trajectory is preserved but the specificity required for reconstruction is not. What looks like decay of stored memories is the specificity-loss function of autoregressive compression, sampled by a reconstruction process that demands more than mere influence.

The forgetting curve, in this framing, is not the rate at which the brain loses what it stored. It is the rate at which an autoregressive system loses the ability to regenerate its own past, given that the past is present only as compressed influence on the current state.

---

### Open Questions

**Is prior sequence decodable from the forward pass?** The critical experiment: present the same stimuli in different temporal orders and ask whether V1 responses to a fixed probe carry decodable information about the specific prior sequence --- not just the prior stimulus set. Order specificity is the uniquely autoregressive prediction. Predictive coding does not require it.

**The hard problem: dissolved or solved?** Claim 10 identifies consciousness with the autoregressive stream. The <a href="/theory/#consciousness">theoretical treatment</a> argues that subjectivity *is* recursive output-intake navigation of an egocentric decision space --- that there is nothing to add to this process to make it conscious. Whether this constitutes a dissolution of the hard problem (showing the explanatory gap was an artifact of separating processing from experience) or a solution (providing the missing bridge) remains a question the theory frames but does not settle.

**The cognitive hierarchy.** Ordering species by the depth and richness of their autoregressive machinery gives a principled account of cognitive complexity. Diagnostic behaviors: object permanence, trace vs. delay conditioning, working memory span, planning horizon, language. The acquisition of autoregressive machinery and the emergence of memory may be the same evolutionary event.

**How does distributed neural processing produce unified \\(y_t\\)?** The architectural claim is clear: one generator, one state per cycle. The physiological question of how spatially distributed cortical activity converges into a single generated state remains open. This is the residual binding question --- not *why* experience is unified (that follows from the architecture) but *how* the neural hardware implements a single \\(\mathcal{G}\\).

</div>
