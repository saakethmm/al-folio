---
title: Interpreting and improving natural-language processing (in machines) with natural language-processing (in the brain)
authors: Mariya Toneva, Leila Wehbe
year: 2019
published: false
---
2024-02-08, 0957

Status: #paper

Tags: [[Research]], [[Encoding]], [[MEG]], [[fMRI]], [[Transformers]], [[NLP]], [[Representational Alignment]], [[LSTM]], [[Computational Neuroscience]], [[Cognitive Neuroscience]]

#### What *question* do they seek to answer? 
Pre-trained models fine-tuned on a particular task do *better* than a model solely trained to do that task. As a result, language models based on neural networks seem to capture something more general about language - *what exactly are those representations*?

**Why?**
General scientific question, similar to what really interests me.

#### What's their *idea* to answer that question? 
1. Observe brain activity of subjects reading naturalistic text for interpreting neural networks
	* Use fMRI/MEG recordings of brain activity as text is presented one word at a time
2. Present same text to NLP models and extract representations from intermediate layers
	* Learn alignment between extracted representations and brain recordings for same text and see what we can find!
	* ==Why should this work?==

*Full-data driven approach* 
* Use priors based on what has been empirically found to be the different language centers in the brain (group 1b, group 2)

**How do they come up with it?**
Brain recordings have inherent structure when it comes to language
* Locations determined by fMRI, latencies and order determined by MEG
* If we align the data with network representations (which might be learning completely uninterpretable correlations in data), then we might be able to decompose the representation into "parts" (like the brain) which should be more interpretable!

Previous studies have primarily look at:
* condition contrasting models (absence or presence of linguistic property, semantic features, etc.)

#### What *data/models* do they use to test it? 

**Data**: 
* fMRI data published by Wehbe et al. (2014b)
* MEG data published by Wehbe et al. (2014a)

**Models**: 
1. **2-layered ELMo** (bidirectional language model) comprising several LSTMs
2. **Base BERT** model (bidirectional model) comprising stacked Transformers
3. **USE** encodes sentences into embeddings
4. **T-XL** incorporates *segment-level* recurrence with the goal of longer context

**Why?**
MEG has temporal resolution, fMRI has spatial resolution

Each of the different models captures some level of bidirectionality with varied context lengths which helps for testing.
#### What *experiments* do they run? Consider 3 experiments. 
1. Encoding models
	* Take network representation $x_{l, k}$ as input ($l$ = layer, $k$ = set of words)
	* Learn a function $f$ using regularized ridge *linear* regression to estimate $y$ (corresponding brain recording for same $k$ words)
2. Compare models with multiple layers to test prediction across context lengths (to see how context affects performance)

**Why?** 


#### Would *I* run different experiments? What else would *I* like to see?
* What about analyzing fMRI and MEG activity together?
* Analysis only seems to be done separately 

  
#### What do their results say (*my* interpretation)? Same three.
1. Performance of encoding models (Fig 3) ![[Screenshot 2024-02-08 at 10.51.18 AM.png]]
	  * Longer context models (e.g., T-XL and BERT) appear to do better at predicting voxels over context
	  * ELMo does a surprisingly good job of predicting voxels over both word embeddings and context
2. Comparison of encoding performance with different context lengths (Fig 4) 
![[Screenshot 2024-02-08 at 11.06.24 AM.png]]
* Middle layers across the board seem to perform the best over all context lengths 
* As context length increases, the later layers do better while at lower context lengths, the early layers do a little better

#### What do their results say (*their* interpretation)? Same three.
1. Fig 3
	* *Proof of Concept*: Word's POS and ELMo embedding predict shared brain activity around 200ms after word onset 
		* Known from electrophys studies that around 200 ms after onset is when POS violations recorded
		* Conclude that ELMo embedding contains some information about POS of word
		* ==Very general finding right? But interesting nonetheless...== 
	* Most places predicted by word-embedding also predicted by long contexts $\implies$ long context representation also contain enough local information
2. Fig 4
	* Middle layers perform best for contexts longer than 15 words
	* T-XL is the only model which *improves* performance over context length

#### What are their conclusions?
* Introduced novel approach of using brain activity to interpret different representations from NNs
* Uniform attention on previous layer improved brain prediction performance in shallow layers
	* On NLP tasks with the same alterations, NLP task performance improves!
* Altering NLP model to align with brain recordings could help understanding of NLP models since we know certain characteristics of brain function

**Do they make sense?**
Yes, but I think the claim is a little broad since there are still many aspects not understood about the brain, so by simply predicting brain activity with high accuracy is trading black boxes, no?
