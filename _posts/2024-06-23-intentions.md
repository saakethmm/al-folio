---
layout: distill
published: true
title:  Intentions for the Future
date:   2024-06-23
description: Why am I doing what I'm doing?
tags: personal, AI, neuroscience
categories: general
comments: true # looks disgusting right now, need to fix this too...

authors:
  - name: Saaketh Medepalli
    affiliations: Carnegie Mellon University

bibliography: 2024-06-23-intentions.bib
---

## Why this post?

Inspired by Richard Hamming's famous talk, ["You and Your Research"](http://www.cs.virginia.edu/~robins/YouAndYourResearch.html), I've been thinking about what the most important questions to ask are.

The way he phrases the question is also quite interesting, in the sense that it's not just what is generally thought to be the most lucrative problems to solve (which might include things like time machines, a unified theory of physics, teleportation, telepathy (though some progress has been made here! <d-cite key="tang2022semantic"></d-cite>) or the mind-body problem/hard problem of consciousness).

Instead (from my interpretation) the best questions one can ask are subjective to the individual, specifically those where the individual has a good angle of attack to answer the question. In other words, one person's most important questions might not match another's (which has the broader implication that blindly following someone else's research because they are passionate about it doesn't mean you will be too - everyone needs to think carefully about their own skillsets and inclinations!).

## So, what are my intentions?

With this in mind, I want to lay out some of my core interests and some specific questions I'm currently investigating and hope to investigate in the future. I've also recently decided to apply for a PhD rather than go to industry after my MS (a topic for another post!), and I think it's important to have a clear idea of what I want to do and why I want to do it.

Since the summer after my freshman year of college, I've been captivated by the fields of neuroscience and AI.

*Why?* Two simple reasons:

1. The human brain is one of the most complex pieces of matter created by nature and understanding how it enables different behaviors can allow us to treat mental afflictions such as addiction, depression & anxiety and also enhance the human mind.

  * It will help us more deeply understand the universe through ties to several other fields (e.g., elucidating the role of the observer in the experiment from the quantum mechanical perspective).

  * On a side note, I have a (perhaps naïve) optimism that revealing some of the brain/mind's mysteries will have an extensive social impact as well, just by virtue of understanding ourselves further.

2. AI (more specifically deep learning) is undisputedly the most disruptive tool right now with the rise of data/compute. It has the potential to make tremendous impact on society (and already has in some ways... ahem Copilot <d-footnote> I promise I didn't use an LLM/Copilot to write this, though it was tempting</d-footnote>).

  * With the advent of LLMs (Large Language Models) such as GPT-4, Claude-3.5, etc., we now have the best models of intelligence so far seen in human history. It's nice to think these models are just doing next-word prediction, but the representations learned go far, far deeper to be able to perform this simple task.

Despite both fields somewhat diverging in their approaches (with AI especially becoming more engineering/product-driven), I think some of the **real** excitements will come at their intersection or *alignment* (NeuroAI!)<d-footnote> really the intersection between Cognitive Neuroscience and AI, which is where the level of comparison makes sense at this point in time (given deep learning really isn't biologically accurate, e.g., credit assignment problem <d-cite key="richards2019dendritic"></d-cite>) </d-footnote>, some already well-known while others just some predictions I have <d-footnote> To be clear, others have commented on these also, though these are generally less mainstream and my predictions on where things are headed in the future </d-footnote>

### Neuroscience $\rightarrow$ AI

#### *Popular Takes*

* Historical influence in building model architectures (e.g., Perceptron, Neocognitron, CNN, Attention mechanism <d-footnote>at least at a high level, if we define it as a [flexible mechanism for controlling limited computational resources] <d-cite key="lindsay2021attention"></d-cite> </d-footnote>) and potential for future contributions.

* The "AGI" Standard to which intelligence of models is held. Human brain is the demarcating line between low-level and super intelligence.

#### *My Predictions*

* The purpose of these models is for augmenting human capabilities (though inevitably replacing for more mundane tasks), so learning interactions with these models will be of tremendous value. Understanding our own minds is still a necessary endeavor that will be vital for future AI-human interactions and BMI (brain-machine interfaces <d-footnote> Not to be confused with body-mass index </d-footnote>).

### AI $\rightarrow$ Neuroscience

#### *Popular Takes*

* Language and vision models based on deep learning (e.g., Transformers for language, CNNs for vision) have proved to be the best models so far successful in predicting held-out brain activity <d-cite key="antonello2024scalinglawslanguageencoding"></d-cite> <d-cite key="margalit2024unifying"></d-cite>.

* By optimizing solutions for certain tasks across domains (e.g., object inpainting (CV), next-word prediction (NLP), robot stepping up a stair (robotics), etc.), representations to address those tasks will continue to improve and perhaps converge onto the brain <d-cite key="hermann2023human"></d-cite>.

#### *My Predictions*

* Though we've been treating neural networks as black boxes since their widespread adoption in 2012, recent work in interpretability  has shattered this notion <d-cite key="templeton2024scaling"></d-cite> <d-cite key="marks2024sparse"></d-cite>. Despite it being a work in progress, there are now clearer ways to reveal the role of circuits within the larger network.

  * Combined with the first popular take above, this means we can intervene on the circuits in the neural networks to elicit some behavioral change, upon which we can observe the causal effect of this intervention on the brain predictivity <d-cite key="lindsay2023groundingneurosciencebehavioralchanges"></d-cite>.

  * With enough brain data, we can directly train/fine-tune models to predict brain activity and peer into them using these methods. This line of work has already shown very cool results <d-cite key="khosla2022high"></d-cite> <d-cite key="luo2023braindiffusionvisualexploration"></d-cite>.

### AI $\leftrightarrow$ Neuroscience?

But the story doesn't end there folks. There's a rising notion that the representations learned by artificial and biological neural networks are converging <d-cite key="huh2024platonicrepresentationhypothesis"></d-cite> <d-cite key="khosla2024privileged"></d-cite>. In other words, we're seeing some form of *representational alignment*.

In my view, this idea, if shown to be valid, could have profound implications for a number of fields across science, not just cognitive science/neuroscience/AI. For instance, consider the question of how spoken words are perceived by humans/machines. If it were the case that the underlying representations are converging, this suggests that the high-level computations performed to get from language to comprehension are *also converging* (since the representations are the medium over which the computations occur) <d-footnote> Note: not necessarily the mechanism by which this is implemented, since things like weight sharing or pooling may not exist in the brain </d-footnote> (this is a difficult point that I'll cover in a later blog post).

One fuzzy and highly speculative possibility is that if this convergence is accurate, there might be a unification with ideas from quantum mechanics, which currently has to deal with the [observer effect](https://en.wikipedia.org/wiki/Observer_effect_(physics)#Quantum_mechanics). Perhaps if the theory of what exactly an observer is observing is solidified, advances can be made on this front.

## What are my important problems?

Given this overview, where do I fit in?

Though all domains are interesting and significant for the future, one that I find myself drawn to right now is language. The question is notoriously complex when broken down: how does a sound waveform entering our ears get translated into a coherent group of sounds that we interpret as a mode of communication (language)? To make matters more confusing, this language takes place in our mind as thoughts, but how does this even happen (i.e., mind-body problem)?

To be more specific, the problem I want to tackle is deciphering the mechanism of auditory/language processing, using deep learning models as a means to get there.

With my background in computational neuroscience, signal processing and machine learning, I believe I have the toolkit (attack) necessary for the task. Coupled with the rapid advancements in speech/language models along with interpretability research (angle), I think there is no better time to work on this problem.

There's tremendous value from this direction of research too. Philosophically, these question goes to the root of the mind-body problem (in both machines and humans). This direction can also help distinguish the intelligence of deep learning-based models from that of humans. In terms of applications, we might be able to create better AI systems that align more with the behavior of humans, along with better ways of understanding human thinking that could be useful in domains like education, law, and society at large.

Crucially, better understanding the mechanism of language processing can also help us work towards improvements in standards of living for those people with disabilities, such as aphasia or dyslexia.

## Future of Blog

I think this is a very exciting time to be in this field, and I'm looking forward to being a part of what's to come. Here's some I things I'm planning that you can expect to see on the blog:

* There's few different projects I'm toying with right now. In the future, I'll make each of these into its own blog post as I make more progress (and hopefully share some cool results)!

* A deep dive into certain papers which I find especially worth diggint into, along with its implications for the broader field.

* Inspired by Patrick Mineault's work at the [NeuroAI Archive](https://www.neuroai.science/archive), I'll post paper bundles (summary of 4-5 papers) around some topic?

* Workshop/conference reviews

* Other Reflections

<!-- 1. Brain rhythms seem to play a crucial role in chunking the sounds we hear into language. Can we elucidate this mechanism using speech/language models (building on top of the notion that when the task to be solved is the same, the representations/mechanisms begin aligning across artificial and natural systems)?

2. There's been a lot of recent buzz about the resurgence of recurrent models like RWKV and Mamba. Though it remains to be seen whether they can beat Transformers in practice, can these recurrent models beat the neural predictivity of attention-based models? What does this tell us about the language comprehension abilities of humans?

3. Mechanistic interpretability has been making waves in recent years for striving to peer inside the black box of deep neural networks. It's still a work in progress, but results involving the ability to steer LLMs to behave in different ways (link to Anthropic paper) along with the identification of circuits that have a causal role in specific behaviors (insert Bau citation) are too convincing to ignore. By tweaking LMs in a systematic way, can we use encoding models methods to elucidate the causal mechanisms behind language processing in the brain/mind? -->

Overall, I'm hoping to post something weekly to biweekly. Stay tuned!


<!-- #### Post-credits Note: *Why does any of this even matter? AGI is coming soon anyways, right?*

A community in Silicon Valley are noting the possibility of human-level intelligence in the next few years, as we continue to scale foundation models with more data and compute. This is a whole other topic for another time, but to keep it short and sweet I'm quite skeptical of this claim, if not for the sole reason that everyone needs to clarify what precisely is meant by human-level intelligence (all AI people care about is Turing test across multiple domains, ... don't know if I'm on board with this). One of the best ways to do that is to more closely inspect the principles underlying intelligence, which is a natural result of representational alignment.

But let's suppose all of the AI doomers are correct and we have "superintelligent" AI (ASI) within the next five years or so (insert citation regarding this claim). *Even if* this is the case, humans aren't going anywhere. In fact, I'd argue more than ever how crucial it is to understand ourselves...   -->
