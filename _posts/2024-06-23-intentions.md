---
layout: distill
published: true
title:  Me and My Research
date:   2024-08-18
description: Why am I doing what I'm doing?
tags: personal, AI, neuroscience
categories: essays
comments: true # looks disgusting right now, need to fix this too...

authors:
  - name: Saaketh Medepalli
    affiliations: 
      name: Machine Learning Department, Carnegie Mellon University

bibliography: 2024-06-23-intentions.bib
---

Inspired by Richard Hamming's famous talk, ["You and Your Research"](http://www.cs.virginia.edu/~robins/YouAndYourResearch.html), I've been thinking about what the most important questions to ask are.

The way he phrases the question is also quite interesting, in the sense that it's not just what is generally thought to be the most lucrative problems to solve (which might include things like time machines, a unified theory of physics, teleportation, telepathy (though some progress has been made here! <d-cite key="tang2022semantic"></d-cite>) or the mind-body problem/hard problem of consciousness).

Instead (from my interpretation) the best questions one can ask are subjective to the individual, specifically those where the individual has a good angle of attack to answer the question. In other words, one person's most important questions might not match another's (which has the broader implication that blindly following someone else's research because they are passionate about it doesn't mean you will be too - everyone needs to think carefully about their own skillsets and inclinations!).

## So, what are my intentions?

With this in mind, I want to lay out some of my core interests and some specific questions I'm currently investigating and hope to investigate in the future. At the core, I think it's important to have a clear idea of what I want to do and why I want to do it.

Since the summer after my freshman year of college, I've been very fascinated by the fields of neuroscience and AI, along with their intersection.

*Why?* Mainly two reasons:

1. The human brain is one of the most complex pieces of matter created by nature and it is one of science's great mysteries as to how it enables such complex behavior. In addition:

   * Understanding how it enables different behaviors can allow us to treat mental afflictions such as addiction, depression & anxiety and also enhance the human mind.

   * It will help us more deeply understand *universal truths* through ties to several other fields (physics, philosophy, etc.).

   * ~~Perhaps naïvely, I optimistically believe that revealing some of the brain/mind's mysteries will have an extensive social impact as well, just by virtue of understanding ourselves further.~~

2. AI (more specifically deep learning) is undisputedly the most disruptive tool right now with the rise of big data/compute. It has the potential to make tremendous impact on society (and already has in some ways <d-footnote> I promise I didn't use ChatGPT to write this, though it was tempting</d-footnote>).

   * With the advent of LLMs (Large Language Models) such as GPT-4, Claude-3.5, etc., we now have the best models of intelligence so far seen in human history. It's nice to think these models are just doing next-word prediction, but the representations learned go far, far deeper than what this simple task might give away.

Despite both fields somewhat diverging in their approaches (with AI especially becoming more engineering/product-driven), there are some **real** excitements coming at their intersection or *alignment* <d-footnote> In my view, the intersection between Cognitive Neuroscience and AI is where the level of comparison makes sense at this point (i.e., algorithmic level) in time (given deep learning really isn't biologically accurate, e.g., credit assignment problem <d-cite key="richards2019dendritic"></d-cite>) </d-footnote>, some already mainstream while others just some opinions I have <d-footnote> To be clear, others have commented on these also, though these seem to be less mainstream </d-footnote>.

### Neuroscience $\rightarrow$ AI

#### *Popular Takes*

* Historical influence in building model architectures (e.g., Perceptron, Neocognitron, CNN, Attention mechanism <d-footnote>at least at a high level, if we define it as a flexible mechanism for controlling limited computational resources <d-cite key="lindsay2021attention"></d-cite> </d-footnote>) and potential for future contributions.

* The "AGI" Standard to which intelligence of models is held. Human brain is the demarcating line between low-level and super intelligence.

#### *My Predictions*

* The purpose of these models is for augmenting human capabilities (though inevitably replacing for more mundane tasks), so learning interactions with these models will be of tremendous value. Understanding our own minds is still a necessary endeavor that will be vital for future AI-human interactions and BMI (brain-machine interfaces <d-footnote> Not to be confused with body-mass index </d-footnote>).

### AI $\rightarrow$ Neuroscience

#### *Popular Takes*

* Language and vision models based on deep learning (e.g., Transformers for language, CNNs for vision) have proved to be the best models so far successful in predicting held-out brain activity <d-cite key="antonello2024scalinglawslanguageencoding"></d-cite> <d-cite key="margalit2024unifying"></d-cite>.

* By optimizing solutions for certain tasks across domains (e.g., object inpainting (CV), next-word prediction (NLP), robot stepping up a stair (robotics), etc.), representations to address those tasks will continue to improve and perhaps converge onto the brain <d-cite key="hermann2023human"></d-cite>.

#### *My Predictions*

* Though we've been treating neural networks as black boxes since their widespread adoption in 2012, recent work in interpretability has shattered this notion <d-cite key="templeton2024scaling"></d-cite> <d-cite key="marks2024sparsefeaturecircuitsdiscovering"></d-cite>. Despite it being a work in progress, there are now clearer ways to reveal the role of circuits within the larger network.

  * Combined with the first popular take above, this means we can intervene on the circuits in the neural networks to elicit some behavioral change, upon which we can observe the causal effect of this intervention on the brain predictivity <d-cite key="lindsay2023groundingneurosciencebehavioralchanges"></d-cite>.

  * With enough brain data, we can directly train/fine-tune models to predict brain activity and peer into the resulting *in silico* models using these methods. This line of work has already shown very cool results <d-cite key="khosla2022high"></d-cite> <d-cite key="luo2023braindiffusionvisualexploration"></d-cite> and will prove to be very promising.

### AI $\leftrightarrow$ Neuroscience?

But the story doesn't end there folks. There's a rising notion that apart from the higher-level behaviors that seem to be converging (evidenced by consistent improvement on the latest benchmarks), the representations learned by artificial and biological neural networks are *also* converging <d-cite key="huh2024platonicrepresentationhypothesis"></d-cite>. In other words, we're seeing *representational alignment* <d-footnote> A natural question to ask is what exactly what we are aligning to. This paper argues that there is an underlying, objective reality, akin to Plato's Theory of Forms, that all intelligent systems learn some form of</d-footnote>.

In my view, this idea, if shown to be valid, could have profound implications for a number of fields across science, not just cognitive science/neuroscience/AI. One example has already been briefly mentioned - representing the brain via *in silico* models, upon which we can do extensive analysis since every attribute of the model (now brain) is fully accessible and modifiable.  <d-footnote> Note: The focus so far has been on Marr's 1st and 2nd levels, but we havent't discussed the 3rd. Folks are working on alignment here as well (e.g., neuromorphic engineering) but representational alignment is somewhat independent of the mechanism by which the algorithms are implemented, since things like weight sharing or pooling may not exist within neuronal circuits in the brain </d-footnote>.

Another fuzzy and highly speculative possibility is that if this convergence is accurate, there might be a [unification with ideas from quantum mechanics](https://www.psychologytoday.com/us/blog/the-digital-self/202405/ais-quest-for-a-grand-unification-theory), which currently has to deal with the [observer effect](https://en.wikipedia.org/wiki/Observer_effect_(physics)#Quantum_mechanics). To be more specific, if the hypothesis turns out to be accurate, maybe we could use *in silico* models to represent the **first-person experience** of a quantum mechanical process <d-footnote> 

<!-- I explore the potential impact *in silico* modeling will have on science here  -->

## What are my important problems?

As a whole, I find that my core interests lean towards this broad question of AI-human alignment at the representational level, but also at the behavioral/value level.

I've explored the former question thoroughly in this blog post, which is what I'm currently working on, in the domain of language. The question is notoriously complex when broken down: how do vibrations entering our ears get translated into a coherent group of sounds that we interpret as language? To make matters more confusing, this language takes place in our mind as thoughts, but how does this even happen (i.e., mind-body problem)? Due to the rapid advancements in language models along with interpretability research, it is an interesting time to be studying how LLMs process language and how that compares to the mechanisms by which the brain processes language. Discovering some shared principles could be fruitful to neuroscience research along with building more human-aligned, interpretable AI systems.

Another question (on a rather different, but related, note) that is very dear to me is how to build AI systems that are aligned with our goals of constructing meaningful, happy lives, akin to what folks over at the [Meaning Alignment Institute](https://www.meaningalignment.org/) are working on. This is definitely a topic for another post, but to keep it short, many people in my generation (Gen Z) are suffering. From anxiety and depression to comparisons and short-attention spans, high-speed access to very potent stimuli (e.g., social media, video games, pornography, YouTube, etc.) has allowed mental health issues to skyrocket at unprecedented rates. AI has the potential to profoundly exacerbate these problems or improve people's lives. The other important problem for me in the future is to help construct AI models/frameworks/applications that can steer people's lives in a positive direction.

## Future of Blog

I see two roles for this blog:

### 1. Exploring Technical Topics

This is an exciting time to be in the field of machine learning, and for all the ups and downs, I'm fascinated by what people are working on. I hope to write about relevant topics that I find worth clarifying (for myself & hopefully others), across topics in machine learning, AI alignment, AI ethics, neuroscience, philosophy and more. I'd like to also use this as an avenue to learn about cool and relevant new ideas/papers (see list below), and experiment with ways to distill these into useful explanations.

Here's a list of topics that I'm interested in diving deeper into:

* Foundation Models <!-- Past-transformers (Can we improve them to be more useful?), Flash Attention, MoE to gating information? Similarly, JEPA for vision, other RL models, KAN -->
* Representation Learning  <!-- What features are learned? During training, what is really going on? (grokking paper, mechanistic analysis of training process) -->
* Interpreting Representations <!-- Interpretability techniques -->
* Retrieval-Augmented Generation (RAG)
* LLM Personalization
* Alignment Metrics  <!-- Predictivity (regression), RSA, etc.  -->
* Improving Alignment <!-- Better tasks (Aran's work), Flash Attention, etc. -->
* Human-AI Alignment <!-- RLHF, Meaning alignment (moral graphs) -->
* ... and more!

### 2. Essays

I tend to go down rabbit holes quite often when something strikes me as curious, so I'll use the blog also as an avenue to explore miscellaneous topics that I find interesting in the moment and perhaps want to elucidate more for myself. Some topics of interest are philosophy (Western & Eastern), Indian history/culture, future of technology/AI, mental health, etc.


### The End is Just the Beginning

Due to other obligations, the posting schedule will be pretty random since I'm just getting into the hang of it, though hopefully I'll find a more regular schedule in the future. Stay tuned!

*Last modified on 1/23/2025*