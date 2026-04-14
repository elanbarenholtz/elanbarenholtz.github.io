---
layout: post
title: "What LLMs Prove About Language"
date: 2026-04-13
tags: [language, LLMs, syntax]
description: "LLMs acquire grammar without being taught it. That fact alone should reshape how we think about language."
---

There's a fact about large language models that should have reshaped linguistics the moment it became clear, but somehow hasn't: **LLMs acquire grammar without being taught it.**

No one gives GPT-4 a grammar textbook. No one labels parts of speech in the training data. No one writes rules for subject-verb agreement, or tense marking, or relative clause attachment. The model simply predicts the next token, over and over, across billions of examples --- and grammatical competence falls out.

This is not a curiosity. It is an existence proof with profound implications.

## The Received View

Mainstream linguistics, following Chomsky, holds that language is structured by an innate grammar --- a system of rules that humans are born with, which allows us to produce and understand an infinite number of sentences from a finite set of building blocks. This is the "Universal Grammar" hypothesis.

Under this view, the distributional patterns in language are *produced by* the grammar, but they aren't the grammar itself. The grammar is an abstract computational system, and learning it requires inductive biases specific to language.

LLMs challenge this picture at its foundation.

## What Next-Token Prediction Gives You

When you train a model to predict the next token, you get:

- **Subject-verb agreement** across long dependencies ("The keys to the cabinet *are* on the table")
- **Tense consistency** across discourse
- **Recursive embedding** ("The dog that the cat that the rat bit chased ran away")
- **Morphological regularity** and productive use of affixes
- **Pragmatic sensitivity** --- appropriate register, conversational implicature, presupposition

All of this from distributional statistics. No rules. No innate grammar. No language-specific module.

## Distributional Structure *Is* the Structure

Here's the reframe: what if there is no grammar separate from distributional statistics? What if what we call "syntax" is simply the high-level skeletal structure of co-occurrence patterns?

Function words --- THE, IS, WAS, TO, OF, THAT --- are the most frequent tokens in any language. They carry minimal semantic content on their own. But they are enormously informative about what comes next. They are *high-leverage prediction tokens*: they constrain the space of likely continuations more than content words do.

Morphological markers --- -ING, -ED, -LY, -TION --- do the same thing at the sub-word level. They tell you whether you're in a process or a completed event, whether you're dealing with a manner or a result, whether you're in a noun phrase or a verb phrase.

From this perspective, syntax is not a separate system that generates distributional patterns. Syntax *is* the distributional pattern --- specifically, the pattern created by high-leverage tokens that constrain sequential prediction.

## The Morphosyntax Experiment

We tested this directly. If function words and morphology constrain prediction independently of meaning, then they should reduce uncertainty even when surrounded by nonsense words.

We created Jabberwocky sentences --- "The blicket was florping the daxen grentily" --- where content words are replaced with pronounceable nonwords but function words and morphology are preserved. Then we measured how much uncertainty (entropy) language models have about the next token.

The result: **morphosyntax alone reduces entropy by about 1 bit**, even when every content word is meaningless. That's a substantial constraint on prediction from structure alone.

This is exactly what the distributional account predicts, and it's hard to explain if you think grammar and statistics are separate systems.

## What This Means for Human Language

Children don't learn language by being taught rules. They learn it by exposure --- by hearing millions of utterances and extracting patterns. The patterns they extract look like grammar because grammar *is* the pattern.

This doesn't mean that the brain and LLMs work the same way mechanistically. They clearly differ in architecture, training, and a hundred other details. But LLMs prove that a distributional approach to language is *sufficient* to produce grammatical competence. That fact alone should shift the burden of proof: if you claim that language requires something more than distributional learning, you now need to explain what that something is and why it's necessary --- given that we have working existence proofs that it isn't.
