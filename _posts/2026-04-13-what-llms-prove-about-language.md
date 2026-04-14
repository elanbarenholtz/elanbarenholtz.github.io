---
layout: post
title: "Syntax Without Rules: The Distributional Skeleton of Language"
date: 2026-04-13
tags: [language, LLMs, syntax, morphosyntax]
description: "LLMs acquire grammatical competence from distributional statistics alone. This is not a curiosity — it is evidence that what we call syntax is the skeletal structure of sequential prediction, not a separate rule system."
---

The most consequential finding in modern linguistics did not come from a linguistics department. It came from scaling next-token prediction: large language models acquire grammatical competence — subject-verb agreement across long dependencies, recursive embedding, tense consistency, productive morphology, pragmatic sensitivity — without being taught any grammar at all.

This is routinely treated as an engineering achievement. It should be treated as an empirical result about the nature of language.

## The claim

The autoregressive brain framework makes a specific proposal about syntax: what linguists call "grammar" is not a rule system that generates distributional patterns. It *is* the distributional pattern — specifically, the skeletal structure of high-leverage tokens that constrain sequential prediction.

This inverts the standard relationship between grammar and statistics. Under the Chomskyan program, distributional regularities are *produced by* an underlying grammar — an abstract computational system, possibly innate, that specifies the set of well-formed sentences. Statistics are surface phenomena; the grammar is the deep structure.

The distributional account says: there is no deep structure separate from the statistics. The regularities are the thing itself. Function words (THE, IS, WAS, TO, OF, THAT) and morphological markers (-ING, -ED, -LY, -TION) are high-leverage tokens — they carry minimal semantic content but are enormously informative about what comes next. They constrain the trajectory of sequential prediction, narrowing the space of probable continuations far more than content words do. This constraining function is what "grammar" is.

## Why function words are high-leverage

Consider the predictive consequences of encountering "the" in a sequence. This single token immediately constrains the next state: a noun phrase is coming. Adjectives become probable. Verbs become improbable. The space of likely continuations narrows dramatically.

Now consider encountering "was" after a noun phrase. The system is now in a past-tense predicate. The -ING morpheme becomes probable (progressive aspect), as do past participles and predicate adjectives. Each function word and morphological marker acts as a constraint on the generative trajectory — not because it carries meaning, but because it specifies the distributional neighborhood of what follows.

In the autoregressive brain framework, this is not limited to language. The cognitive system generates each state as the optimized outcome of the preceding trajectory. In the specific domain of language production and comprehension, function words and morphology are the tokens that most efficiently constrain this generation. They are the scaffolding that makes the trajectory predictable enough for communication to work.

## Empirical test: The morphosyntax experiment

If syntax is the constraining function of high-leverage tokens, then this constraint should operate independently of semantic content. Function words and morphology should reduce prediction uncertainty even when surrounded by meaningless content.

We tested this by measuring next-token entropy across four conditions in language models:

**Real sentences:** "The teacher was explaining the concept clearly"
Full morphosyntactic and semantic constraint. Entropy: 7.45 bits.

**Jabberwocky:** "The blicket was florping the daxen grentily"
Content words replaced with pronounceable nonwords, but function words and morphology preserved. Entropy: 8.04 bits.

**Stripped:** "Ke blicket nar florp ke daxen grenti"
All words replaced with nonwords, morphology removed. Entropy: 9.07 bits.

**Random nonwords:** Completely unstructured sequences. Entropy: 9.27 bits.

The critical comparison is Jabberwocky vs. Stripped. The only difference is the presence of real function words and morphological markers. This difference reduces entropy by approximately 1 bit (p < 0.0001, Cohen's d = −1.75). One bit is substantial — it means morphosyntax alone cuts the prediction space roughly in half, even when every content word is meaningless.

This is what the distributional account predicts: function words and morphology constrain sequential prediction as a structural property, independent of semantic content. It is difficult to reconcile with a view in which grammar and distributional statistics are separate systems.

## What LLMs demonstrate

The standard objection is that LLMs might learn grammar through some mechanism that is irrelevant to human cognition — that their success is an engineering curiosity, not evidence about language. This objection misses the structure of the argument.

The claim is not that the brain is an LLM, or that children learn language the way GPT is trained. The claim is about *sufficiency*: distributional learning over sequential data is sufficient to produce grammatical competence. LLMs prove this constructively. They are existence proofs.

Before LLMs, it was reasonable to argue that distributional statistics could not, in principle, capture the recursive, hierarchical structure of natural language. Chomsky's poverty-of-the-stimulus argument held that the input children receive underdetermines the grammar they acquire, therefore innate structure must bridge the gap. The success of LLMs does not prove this argument wrong in every detail, but it eliminates the *in-principle* objection. Distributional learning over naturalistic input demonstrably produces recursive syntactic competence. If you want to argue that human language acquisition requires something more, the burden has shifted: you need to specify what that additional mechanism is and why it is necessary, given that we have working systems that achieve grammatical competence without it.

## Convergence with acquisition research

The distributional account is consistent with what developmental research actually shows about language acquisition. Children are statistical learners. Saffran et al. (1996) demonstrated that 8-month-old infants extract transitional probabilities from speech streams after minutes of exposure. Subsequent work has shown statistical learning of phonotactic patterns, word boundaries, morphological regularities, and syntactic categories.

Children do not learn grammar by being corrected — explicit negative evidence plays minimal role in acquisition (Marcus, 1993). They do not learn it from instruction — preschoolers acquire complex syntax before any formal teaching. They learn it from exposure, and the patterns they extract look like grammar because grammar *is* the pattern.

This reframes the poverty-of-the-stimulus argument. The stimulus is not "poor" — it is enormously rich in distributional structure. The question is not whether the input contains enough information (it does — LLMs prove this), but whether the learning mechanism can extract it. Statistical learning research suggests that biological systems can.

## Syntax as trajectory constraint

Within the autoregressive brain framework, this connects to the broader picture. The brain generates cognitive states sequentially, with each state optimized as the generative outcome of the preceding trajectory. In the domain of language, this means:

- **Production** is trajectory generation through a linguistic state-space. Function words and morphology are generated early in local sequences because they constrain the trajectory — they narrow the space of continuations and make the subsequent content words more predictable to both the speaker and the listener.

- **Comprehension** is trajectory tracking. The listener's cognitive system generates predictions about upcoming states, constrained by the same distributional structure. Function words and morphology allow rapid constraint of these predictions, which is why processing difficulty increases when syntactic expectations are violated (Hale, 2001; Levy, 2008).

- **Grammaticality judgments** are not rule-checks. They are assessments of trajectory plausibility — a sequence "feels" ungrammatical when it deviates sharply from the distributional structure that constrains generation. This explains why grammaticality is gradient rather than binary, and why it is sensitive to frequency and context.

The syntactic structure of language is not a separate module that the brain implements. It is what distributional constraint over sequential generation looks like in the domain of linguistic communication.
