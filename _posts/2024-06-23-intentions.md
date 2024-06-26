---
layout: post
published: true
title:  Intentions for the Future
date:   2024-06-23
description: Why am I doing what I'm doing?
tags: persona, AI, neuroscience
categories: reflections
comments: false # looks disgusting right now, need to fix this too...
---


### Why this post?

Inspired by Richard Hamming's famous talk, ["You and Your Research"](http://www.cs.virginia.edu/~robins/YouAndYourResearch.html), I've been thinking about what are the most important questions to ask. 

The way he phrases the question is also quite interesting, in the sense that it's not just what is generally thought to be the most lucrative problems to solve (which might include things like time machines, a unified theory of physics, teleportation, telepathy (though some progress has been made here! - insert citation to Tang paper) or the mind-body problem).

Instead (from my interpretation) the best questions one can ask are subjective to the individual, specifically those where the individual has a good angle of attack to answer the question. In other words, one person's most important questions might not match another's (which has the broader implication that blindly following someone else's research because they are passionate about it doesn't mean you will be too - everyone needs to think carefully about their own skillsets and inclinations!).

### So, what are my intentions?

With this in mind, I want to lay out some of my core interests and some specific questions I'm currently investigating and hope to investigate in the future. I've also recently decided to apply for a PhD (rather than go to industry), and I think it's important to have a clear idea of what I want to do and why I want to do it.

Since the summer after my freshman year of college, I've been captivated by the fields of neuroscience and AI.

*Why?* Two simple reasons:

* The human brain is one of the most complex pieces of matter created by nature and understanding how it enables different behaviors can allow us to improve mental afflictions such as addiction, depression & anxiety and also build enhancements to the human mind.

  * It will help us more deeply understand the universe through ties to several other fields (e.g., elucidating the role of the observer in the experiment from the quantum mechanical perspective).

  * On a side note, I think revealing some of the brain/mind's mysteries will unite people across the world more, just by virtue of understanding ourselves further.

* AI (more specifically deep learning) is undisputedly the most disruptive tool right now with the rise of data/compute. It has the potential to make tremendous impact on society (and already has in some ways... ahem Copilot$^1$).

  * With the rise of LLMs (Large Language Models) such as GPT-4, Claude-3.5, etc., we now have the best models of intelligence so far seen in human history. It's nice to think these models are just doing next-word prediction, but the representations learned go far, far deeper to be able to perform this simple task.

But this is all very high-level and general. I think some of the real excitements will come at their *intersection* (NeuroAI!), some mainstream and some not so.

#### Neuroscience $\rightarrow$ AI

##### *Mainstream*

* Historical influence in building model architectures (e.g., Perceptron, Neocognitron, CNN, Attention mechanism$^2$)

* The "AGI" Standard to which intelligence of models is held. Human brain is the demarcating line between low-level and superintelligence.

##### *Not so mainstream?*

* The purpose of these models is for augmenting human capabilities (inevitably, sometimes replacing), so the interactions with these models will be of tremendous value. Understanding our own minds is still a necessary endeavor that will be vital for future AI-human interactions and BMI (brain-machine interfaces$^3$)

#### AI $\rightarrow$ Neuroscience

##### *Mainstream*

* Language and vision models based on deep learning (e.g., GPT-2 for language, ResNet for vision) have proved immensely successful (Antontello et al., 2024, brain-score, ...) in predicting held-out brain activity.

* By optimizing solutions for certain tasks across domains (e.g., object inpainting (CV), next-word prediction (NLP), robot stepping up a stair (robotics), etc.), representations to address those tasks will continue to improve and perhaps converge onto the brain (cite Nayebi...)

##### *Not so mainstream?*

* Though we've been treating neural networks as black boxes since their widespread adoption in 2012, recent work in mechanistic interpretability (cite Bau, Nanda, Anthropic) has shattered this notion. Despite it being a work in progress, there are now clearer ways (e.g., Sparse Autoencoders, probing methods) to reveal the role of circuits within the larger network.

  * Combined with the first mainstream point above, this means we can intervene on the circuits in the neural networks to elicit some behavioral change, upon which we can observe the causal effect of this intervention on the brain predictivity.

  * With enough brain data, we can directly optimize models to predict brain activity and peer into them using these methods. This line of work has already shown very cool results (Khosla & Wehbe...)

### What are my important problems?

Though all domains are interesting and significant for the future, one that I find quite profound is language. The question is notoriously complex when broken down: how does a sound waveform entering our ears get translated into a coherent group of sounds that we interpret as a mode of communication (language)? To make matters more confusing, language occurs within our mind as thoughts, but how does this even happen?

That all being said, the challenge is what makes the problem interesting to tackle. In addition, with my background in signal processing and machine learning, I believe I have the toolkit (attack) necessary for the task. Coupled with the rapid advancements in speech/language models along with interpretability research (angle), I think there is no better time to work on this problem.

There's tremendous value from this direction of research too. Philosophically, this question goes to the root of the mind-body problem (in both machines and humans). This direction can also help distinguish the intelligence of deep learning-based models and that of humans. In terms of applications, we might be able to create better AI systems that align more with the behavior of human language processing, along with better ways to understand human thinking that could be useful in domains like education, law, etc.

#### Current Projects

There's few different ideas I'm toying with right now. I hope to make each of these into its own blog post as I make more progress, but for now here's a synopsis:

1. Brain rhythms seem to play a crucial role in chunking the sounds we hear into language. Can we test this mechanism using speech/language models?

2. There's been a lot of recent buzz about the resurgence of recurrent models like RWKV and Mamba. Though it remains to be seen whether they can beat Transformers in practice, can these recurrent models beat the neural predictivity of attention-based models? What does this tell us about the language comprehension abilities of humans?

3. Mechanistic interpretability has been making waves in recent years for striving to peer inside the black box of deep neural networks. It's still a work in progress, but results involving the ability to steer LLMs to behave in different ways (link to Anthropic paper) along with the identification of circuits that have a causal role in specific behaviors (insert Bau citation) are too convincing to ignore. By tweaking LMs in a systematic way, can we use encoding models methods to elucidate the causal mechanisms behind language processing in the brain/mind?

Stay tuned for more...

$^1$ I promise I didn't use Copilot to write this, though it was tempting

$^2$ TODO: write about Bengio's work on this as influenced by neuroscience

$^3$ Not to be confused with the other BMI, though maybe that too in some indirect way


#### Post-credits Note: *Why does any of this even matter? AGI is coming soon anyways, right?*

Some enlightened individuals in Silicon Valley are noting the possibility (even certainty -citation) of human-level intelligence in the next few years, as we continue to scale foundation models with more data and compute. This is a whole other topic for another time, but to keep it short and sweet I'm quite skeptical of this claim, if not for the sole reason that we need to clarify what we mean by human-level intelligence. I personally don't even think ChatGPT is even on the same track as humans with regards to intelligence.

But let's suppose all of the AI doomers are correct and we have "superintelligent" AI (ASI) within the next five years or so (insert citation regarding this claim). *Even if* this is the case, humans aren't going anywhere. In fact, I'd argue more than ever how crucial it is to understand ourselves...  