
## Multi-Task Learning Using Uncertainty to Weigh Losses for Scene Geometry and Semantics

#### CVPR 2018

---

Alex Kendall<sup>1</sup>, Yarin Gal<sup>2</sup>, Roberto Cipolla<sup>1</sup>

<sup>1</sup> University of Cambridge, <sup>2</sup> University of Oxford

---

## Resources

[Paper](https://arxiv.org/pdf/1705.07115.pdf)

[Code](https://github.com/yaringal/multi-task-learning-example)

[Alex Kendall's Homepage](https://alexgkendall.com/research/)

---

##  Motivation

- Scene understanding algorithms must understand both the geometry and
semantics of the scene at the same time.

- Combining all tasks into a single model reduces computation and allows these systems to run in real-time.

--

- However:

  * Performance is highly dependent on an appropriate choice of weighting between each task’s loss

  * Tuning these weights by hand is a difficult and expensive process, making multi-task learning prohibitive in practice.
  
  * The optimal weighting of each task is dependent on the measurement scale (e.g. meters, centimetres or millimetres) and ultimately the magnitude of the task’s noise.

---

## Research Goals

---

- A model trained under multi-task learning can outperform separate models trained individually on each task:
  * Sematic Segmentation
  * Instance Segmentation
  * Depth Estimation

---

## Contributions

---

* A  multi-task loss to simultaneously learn various classification and regression losses of varying quantities and units using *homoscedastic* task uncertainty

* A unified architecture for semantic segmentation, instance segmentation and depth regression

* Demonstrating the importance of loss weighting in multi-task deep learning and how to obtain superior performance compared to equivalent separately trained models.

---

### Model Overview

![overview](assets/network.png)<!-- .element height="100%" width="100%" -->

---

## Related Work

![overview](assets/ablation.png)<!-- .element height="80%" width="80%" -->

---

## IDEAS

- Use homoscedastic uncertainty to weight the losses in multi-task learning models

---

#### Multi Task Learning with Homoscedastic Uncertainty

- Homoscedastic uncertainty
- Multi-task likehoods

---

#### Homoscedastic uncertainty

- In Bayesian modelling
  * *Epistemic Uncertainty*
  * Aleatoric Uncertainty
    * Data-dependent or  Heteroscedastic uncertainty
    * <mark>Task-dependent or Homoscedastic uncertainty </mark> 

---

- In a multi-task setting, the task uncertainty captures the relative confidence between tasks, reflecting the uncertainty inherent to the regression or classification task. 

---

#### Multi-task likehoods 

--

- Definations:
  - For regression task, Likelihood as a Gaussian with mean given by the model output, and an observation noise scalar σ:  
![overview](assets/eq2.png)<!-- .element height="65%" width="60%" -->

  - For classification:  
![overview](assets/eq3.png)<!-- .element height="70%" width="60%" -->

  - Multi-task likehood:  
![overview](assets/eq4.png)<!-- .element height="60%" width="60%" -->

---

- Regression tasks' maximum likelihood inference

  - for Eq2, its written as  
![overview](assets/eq5.png)<!-- .element height="60%" width="60%" -->

  - for multi-output:  
![overview](assets/eq6.png)<!-- .element height="50%" width="60%" -->

  - Leading to the *minimisation* objective:  
![overview](assets/eq7.png)<!-- .element height="50%" width="80%" -->

---

- Classification tasks' maximum likelihood inference

  - with a positive scalar σ. (Boltzmann distribution)  
![overview](assets/eq8.png)<!-- .element height="70%" width="60%" -->

  - log likelihood  
![overview](assets/eq9.png)<!-- .element height="25%" width="225%" -->

---

#### Loss function
- ![overview](assets/eq10.png)<!-- .element height="100%" width="100%" -->

---

## Scene Understanding Model

![overview](assets/instance_seg.png)<!-- .element height="10%" width="100%" -->

---

## Experiments

--

#### Dataset

- CItyScapes

---

### Quantitive Comparison

![results](assets/comparison.png)<!-- .element height="100%" width="100%" -->

---

### Ablation experiments

![results](assets/comparison_1.png)<!-- .element height="100%" width="100%" -->

---

### Qualitative Results

--

![overview](assets/occlusion.png)<!-- .element height="80%" width="80%" -->

---

![results](assets/results.png)<!-- .element height="90%" width="90%" -->

---

# Thank you! 
## Questions?