---
layout: distill
published: false
title: Brain Rhythms and their role in Language Processing
description: Exploring the function of a misunderstood player in the brain
date: 2024-07-08
---



### Language Comprehension

There is a big debate happening in the field of neurolinguistics. Roughly, this can be broken up into nature vs. nurture.

On the nature side (Chomskyans), there are those who believe that hierarchical syntactical structures are built in our brains as we process sounds into language.

On the nurture side, we have those who are skeptical of this claim, and instead argue that distributional semantics/language statistics (aka LLM gang) can perform the same job with respect to this task.

The setting for this debate is brain rhythms, which are a result of patterns of neuronal activity that repeat with some frequency. The work starts by Poeppel... and work using MEG data in a controlled setting

<!-- insert picture of task and key result-->


### What are brain rhythms?

explain...


### Huh? What does frequency have to do with word embeddings?

We can construct sequences (at the MEG sampling rate) of high-dimensional embeddings of the words in the stimulus set. Like word2vec, embeddings that are close in space imply the inputs also occur in similar contexts.

Interestingly (citing Frank & Yang), this approach actually works in replicating the results from the Ding et al. paper, *without* even using any of the constraints of the experiment design (i.e., didn't use the fact that some settings had sentences, others just arbitrary nouns put together)


### Um... if I'm an AI person, why should I care?

The brain is still the true benchmark for AGI in terms of capabilities. We'd be wise to turn to the algorithms and structures learned by the brain as a reference to see how to improve AI systems, including LLMs, to improve their performance (and perhaps also for AI alignment). 