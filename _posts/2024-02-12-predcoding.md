---
title: Evidence of a predictive coding hierarchy in the human brain listening to speech
authors: Charlotte Caucheteux, Alexandre Gramfort, Jean-Rémi King
year: 2023
published: false
---
2024-02-12, 1027

Status: #paper

Tags: [[fMRI]], [[Encoding]], [[LLMs]], [[Language]], [[Predictive coding]], [[Representational Alignment]], [[Cognitive Neuroscience]], [[Computational Neuroscience]], [[Research]]

#### What *question* do they seek to answer? 
Despite massive progress in deep learning with regards to text generation, translation and completion, language models still lag behind (despite being provided so much training data) humans. How can this gap be explained?

**Why?**
* Language models have some key flaws in things like long story generation, syntactic accuracy, and deep language understanding
* It is an interesting question to ask regarding the key differences between humans and language models
* Additionally, what makes the brain able to do such tasks

#### What's their *idea* to answer that question? 
* Why not apply predictive coding theory to this question to see if this can help explain the difference (since LMs only predict the next word)
	* **Predictive Coding Theory**: Human brain uses multiple timescales across the cortical hierarchy to represent information


**What's their contribution?**
* Most prior work only studies surprisal of next word under different tasks, while this work shows that long-range & multi-level predictions actually *improves* brain prediction accuracy, demonstrating predictive coding

#### What *data/models* do they use to test it? 

**Data**:
* Narratives dataset with fMRI of 304 people listening to short stories

**Models**:
* GPT-2 to draw activations from, ridge regression for mapping activations to fMRI signal

##### Why?

**Data**:
* No reasoning given

**Models**:
* **GPT-2** (12-layer, causal) was used for the LM since it has performed the best in prior work
	* Specifically the eighth layer performs the best 

#### What *experiments* do they run? Pick main ones.
1. Encoding model
	* Encoding activations from LM onto fMRI activity (ridge regression) to observe prediction performance ('brain score')
	* Also observe brain scores when concatenating embeddings of different windows with the current word and mapping activity (specifically $w=7$ words at varying distances $d$)
2. Model layer analysis
	* Proceed similarly, but also observe how layer depth of the model impacts prediction performance (very similar in analysis to [[@tonevaInterpretingImprovingNaturallanguage2019]])
3. Syntax vs. Semantics
	* Also observe how syntax and semantics can be explained by the predictive coding hypothesis
	* From this, can any changes be made to the original model (via fine-tuning) to verify the observations made?

##### **Why?** 
* Concatenated future words in some sense represents potential predictions that would be made by the brain, which tests the original hypothesis


#### What else would *I* like to see?
* Perhaps would be interesting to dive a little deeper into the syntax/semantics distinctions (simply taking the residual between $X$ and $X_{syn}$ seems a little basic?)
  
#### What do their results say (*my* interpretation)? Same ones.
1. Figure 2![[Screenshot 2024-02-12 at 11.23.47 AM.png]]
  * Overall several regions of brain are quite accurately predicted by the model 
  * Trend in forecast score shows that models which do account for future words actually map better to the brain, which shows that the brain does indeed try to look ahead 
	  * ==I wonder how this could be extended apart from just concatenation?==
2. Figure 3![[Screenshot 2024-02-12 at 11.33.34 AM.png]]
	* Interesting analysis to observe nature of predictions (i.e., which layer predicts each area best?)
	* Observed that different brain ROIs (correlating to known theories about these areas) actually are predicted by different activations in GPT-2 better than others!
3. Figure 4 ![[Screenshot 2024-02-12 at 11.40.27 AM.png]]
	* Generate several syntactically similar sentences to particular phrases, then observe  activations in model ($X_{syn}$, where $X_{sem}$ is the residual $X - X_{syn}$)
	* Similarly compute forecast score (after concatenating varying future phrases)
	* Syntax in the brain clearly not represented by future words, only present words (whereas semantics more so) 


#### What do their results say (*their* interpretation)? Same ones.
1. Figure 2
	* $\mathcal{F}$ is maximized when $d=8$, so a gap of words between current word and end of concatenated string is ideal 
	* Prior work has shown that different brain ROIs predict different aspects of language
		* Low-level acoustics $\rightarrow$ Heschl's Gyrus
		* Phonemes $\rightarrow$ Superior temporal gyrus
		* Semantics $\rightarrow$ associative cortices
	* Indeed it can be seen that there is a difference between in preferred distance between different regions, which shows the hierarchy to an extent
2. Figure 3
	* Associative cortices better modeled by later layers in GPT-2 (>6 layers)
	* Low-level language areas better modeled by earlier layers 
	* Small difference but very significant
3. Figure 4
	* Semantic features are longer range which peak in the frontal and parietal lobes
	* Syntactic features are much shorter range which peak in the superior temporal and left frontal areas
	* GPT-2 trained explicitly on long-range objectives actually improves prediction performance on frontal/parietal areas (cementing their role in high-level representations of language, or at least prediction)

#### What are their conclusions?
1. Those regions at the top of the language hierarchy are not limited to processing past stimuli but also predicting the future
2. The brain is not limited to predicting just word-level representation but also longer-range representations which vary across the position in the hierarchy (*unlike modern LMs*)
3. Semantic features drive the long-range forecast results, while syntax could be even encoded at the level of neural activity itself

##### **Any future directions to extend?**
* Link between *hierarchical nature of syntax* and whether similar structure exists in LMs/brain is still to be explored 
	* Cannot be explored with fMRI due to how slow it is 
* Characterizing the precise representations along the hierarchy (i.e., interpretability) $\rightarrow$ new probing techniques (==mech interp?==)
* Predicting multiple levels of representations could be key to improving performance of LMs in generating more meaningful long-form generation




