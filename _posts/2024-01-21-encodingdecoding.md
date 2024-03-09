---
layout: post
title: Encoding and decoding in fMRI
published: true
date:   2024-01-21
description: Naselaris et al. (2011), <em>NeuroImage</em>
tags: encoding, decoding, fMRI, cognitive-neuroscience
categories: paper-review
---

### Overview

* **Goal** of many fMRI studies is to understand what sort of information is located in an area of interest in the brain
* **Encoding** and **Decoding** are two sides of the same coin
	* *Encoding* seeks to predict activity given information about the world
	* *Decoding* seeks to make predictions about the world only given activity

* **Primary Methods**
	* *Encoding* uses voxel-based encoding methods to predict activity of individual voxels
		* Traditional approach includes *Statistical Parametric Mapping (SPM)*, which uses independent variables in experiment as features in a *GLM*
		* Then statistical significance is measured for the GLM across all voxels 
	* *Decoding* commonly uses linear classifiers (e.g., SVM, logistic regression with decision boundary)
		* *Identification*: Classify which stimulus or task used from a known set given activity
		* *Reconstruction*: Reconstruct the activity by obtaining the stimulus used to generate the given activity
* **Key Question**: When is it appropriate to use encoding vs. decoding models to study the representations of the brain?

### Encoding Models
* Kay et al. (2008) did an analysis using encoding models using Gabor wavelet basis combined with linear regression to predict activity from stimuli $$\rightarrow$$$ best at the time
* *Components*
	* Set of stimuli (input space)
	* Set of features (feature space)
	* ROIs in the brain to record voxel activity from (activity space)
	* Algorithm used to estimate activity
* Input space $$\rightarrow$$ feature space: non-linear (modeling complexity of brain)
* Feature space $$\rightarrow$$ activity space: *linear*
	* Works well if non-linear feature map models what brain is doing well
	* Ideally should be linear because features at this point should be directly comparable to activity

### Decoding Models
* Same components as earlier
* Activity space $$\rightarrow$$ feature space: *linear*
	* Linear Discriminant Analysis (LDA): assume data drawn from Gaussian for each class
	* Linear SVM
* Feature space $$\rightarrow$$ input space: non-linear
* Form of *hypothesis testing*
	* Linearizing feature space reflects hypothesis about how well certain features appear in some ROI

### Comparison
1. Does an ROI contain info about specific set of features?
	* Necessary to construct encoding/decoding model whose accuracy is much better than chance
	* Encoding +, Decoding +
2. Is the info represented within an ROI important for behavior?
	* Difficult to use encoding models, since making the leap from behavior to activity is somewhat unclear 
		* Just bc features relating to behavior help achieve high prediction accuracy doesn't mean much unless there is link between behaviors and activity
	* Decoding models are much better for this $$\rightarrow$$ outputs feature predictions from activity
	* Encoding -, Decoding +
3. Specific ROIs that contain more about specific set of features?
	* For encoding models, ROIs that contain more info about given features should have higher accuracy (***plotting prediction accuracy on cortical map***)
	* Same with decoding models, if decoding accuracy of features particularly high for certain ROIs, then those are most informative
	* Encoding +, Decoding +
4. Specific features preferentially represented by ROIs?
	* Compare across encoding models, and use prediction accuracy to see if specific features are consistently active
	* Much more difficult for decoding models since feature space is distinct 
	* Encoding +, Decoding -
5. What set of features to get complete functional description of ROI?
	* Main purpose of encoding model (combine all of those encoding models which achieve good performance)
	* Decoding is not the same... can keep going dividing up feature space
	* Encoding +, Decoding -

### More on Encoding Models
* Select stimuli to test whether ROI contains info about a feature
* **Main hypothesis** determines feature space, and each axis is a different level of independent variable 
* Unfortunately, encoding models *cannot* achieve perfect prediction accuracy of fMRI activity because fMRI data is noisy...
	* Physiological, cognitive (uncontrolled), equipment factors
* An encoding model that reaches the upper limit satisfies $$H^T f(s) = \arg \underset{r}{\max} \hspace{2pt} p(r\mid f(s))$$
	* $$H$$ is the weight matrix (each row is weights for a single voxel over all feat)

### Encoding $$\rightarrow$$ Decoding
* Decoding models also useful for judging what all is represented by activity and for BCI
* Simply use Bayes' theorem to move between both!

 $$
 p(f(s) \mid r) \sim p(r \mid f(s))p(f(s))
 $$

* One approach to decoding this way is by using MAP to determine features that maximize probability given some activity
* Prior $$p(f(s))$$ is simply over features
* Going other way not easy since estimating $$p(f(s) \mid r)$$ requires knowing the features that evoke some activity, but this noisy

### Procedure
1. Collect data and split into training and test data
2. Use data to train an encoding model per voxel
3. Apply model to test activity data and get accuracy (can be compared across models now since activity space the same)
4. Use encoding model to get decoding model and evaluate features on test feature data 

### Conclusions
Should be common practice to construct both encoding and decoding models!

### References
1. Naselaris, T., Kay, K. N., Nishimoto, S., & Gallant, J. L. (2011). Encoding and decoding in fMRI. *NeuroImage*, 56(2), 400-410. [https://doi.org/10.1016/j.neuroimage.2010.07.073](https://doi.org/10.1016/j.neuroimage.2010.07.073)

