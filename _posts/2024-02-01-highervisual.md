---
layout: post
title: Higher visual areas act like domain-general filters with strong selectivity and functional specialization
published: false
date: 2024-02-01
description: Khosla and Wehbe (2023), <em>bioRxiv</em>
tags: fMRI, Feature visualization, CNNs, Response-driven, Interpretability, Visual system
categories: paper-review
---

#### What *question* do they seek to answer? 
How can we develop a hypothesis neutral approach to model the selectivity of various regions throughout the visual system?

**Why?**
* In the past, methods have used either one of three approaches:
	1. Hypothesize the stimulus that a particular region is tuned to select for and then carefully design experiments to reveal if this is the case (*deductive approach*)
	2. Use naturalistic images/videos, then use encoding models to test voxel-level tuning (*hypothesis based on features*)
	3. Deep neural networks to optimize for task performance which then are tested to see if they align with brain activity (*hypothesis based on task*)
* All involve some hypothesis, so how can we simply reveal the properties without a priori assumptions?  

#### What's their *idea* to answer that question? 

Construct response-optimized models
* I.e., fitting model parameters to optimize accuracy of neural activity prediction
* If they generalize, that means they can provide a test to existing models or provide new theories (via feature visualization)

**How do they come up with it?**
Given the existence of large, high-quality datasets, such an approach is feasible and worth testing given the question at hand (and problem with existing approaches)

#### What *data/models* do they use to test it? 

**Data**: 7T fMRI NSD 

**Models**: Rotation-equivariant CNNs to model response properties of lower-level areas 
* ==Isn't this a hypothesis?==

**Why?**
Massive. Lot of natural variation in the dataset, including complex and crowded images of *everyday objects* from various viewpoints.
#### What *experiments* do they run? 
<u>1st Approach</u>
* Each network is randomly initialized and then trained from-scratch to predict voxel activity in a specified ROI for a particular stimulus image.
	* ==Are all stimulus images used when training response-optimized models?==
* Examine trained networks via network dissection methods -- namely, *feature visualization* and *feature verbalization* 
	* Measure IoU to quantify agreement between concept and individual voxel
<u>2nd Approach</u>
* Create specific changes in the visual input and study selectivity of model neurons given these specific changes
<u>3rd Approach</u>
* Show that proposed models generalize extremely well to different perceptual tasks given the ROI 
<u>4th Approach</u>
* Forget the ROIs, now find whether the category selective regions reveal themselves when trained on the broad voxel-level activity across the input stimuli

**Why?** 
<u>1st Approach</u>
* Hypothesis-neutral, so the goal is to see whether the responses in an ROI naturally reveal some structure towards what is being tuned for in the ROI
<u>2nd Approach</u>
* Do the ROIs simply respond "yes" or "no" based on whether the preferred stimulus is there, or is there some sort of non-category specific processing mechanism underneath?
<u>3rd Approach</u>
* How about on other related perceptual tasks?
<u>4th Approach</u>
* Instead of starting with the ROI, observe the whole brain and see if these category specific regions naturally are uncovered (otherwise the experiments are a little biased towards what the authors think the ROIs are to begin with)

#### Would *I* run different experiments? What else would *I* like to see?
* Very interesting ideas. Nothing comes to mind as of right now.
  
#### What do their results say (*my* interpretation)? Pick top 3 figures.
![[Screenshot 2024-02-01 at 12.10.23 PM.png]]
  * In Figure 1, we see that among all four regions considered, large portions are well-predicted by the model, meaning it is quite accurate to how voxel activity really is in that area
	  * ==Is there a test set on which to test activity, is that basically E?==
* Unsure how to interpret Figure 1F, ==what does noise-normalize R value mean?==
![[Screenshot 2024-02-01 at 12.26.31 PM.png]]
* Very interesting idea, to use a spatial mask for each voxel to then predict what area of the image is being attended to most by the voxel
* Each of the regions in B show that certain features are consistently more detected by certain areas over others
![[Screenshot 2024-02-01 at 12.33.37 PM.png]]
* ![[Screenshot 2024-02-01 at 12.33.46 PM.png]]
* Network verbalizations (above) and visualizations (below) to better understand what is learned by the response-optimized models
#### What do their results say (*their* interpretation)? Same three.
* For figure 1, they also mention how their model is one of the best at voxel-level prediction, even compared to category-selective models and task-optimized models (see first section)
* For the second figure, they observe that the visual features detected match up pretty well with the known function of the particular ROI (for instances, faces being highly selected for by FFA, along with verbalization results corroborating that)


#### What are their conclusions?
1. Response optimized models were better able to generalize to responses of novel test subjects than task optimized models
2. Probing and looking inside models can provide novel insights into properties of biological system without any priors (reduces complexity of what semantic and visual features actually contribute to voxel-level activity)
3. Encoding models fitted directly to neural activity offer complementary perspective from hypothesis-driven experiments (e.g., contrasts, etc.) $\rightarrow$ directly optimized to explain brain representations and *avoids including confounds from experimenter-defined constraints*
4. Could also explain biological function given the ability for such predictions to emerge 

**Do they make sense?**
Yes, more to cover as well.


- [x] Add 1 paper from references to list: 
Selectivity for food in human ventral visual cortex
