
## The Temporal Opportunist: Self-Supervised Multi-Frame Monocular Depth

#### CVPR 2021

---

Jamie Watson<sup>1</sup>, Oisin Mac Aodha<sup>2</sup>, Victor Prisacariu<sup>1,3</sup>, Gabriel Brostow<sup>1,4</sup>, Michael Firman<sup>1</sup>

<sup>1</sup> Niantic, <sup>2</sup> University of Edinburgh,

<sup>3</sup> University of Oxford,<sup>4</sup> UCL

---

## Resources

[Paper](https://arxiv.org/pdf/2104.14540.pdf)

[Code](https://github.com/nianticlabs/manydepth)


---

## Background

- Self-supervised monocular depth estimation methods are trained using nearby frames as a supervision signal.

- At test time, a trained network can output a depth map from a single RGB image.

--

- However:

  * For some applications, sequence information is also available

  * The vast majority of monocular methods ingore this extra information.

  * Or use test-time refinement techniques or recurrent networks.


---

## Contributions

---

* A deep end-to-end cost volume based self-supervised approach

* A novel consistency loss that encourages the network to ignore the cost volume when it is deemed unreliable.


---

### Model Overview

![overview](assets/network.png)<!-- .element height="100%" width="100%" -->

---

## Related Work

![overview](assets/ablation.png)<!-- .element height="80%" width="80%" -->

---

## IDEA

- Use homoscedastic uncertainty to weight the losses in a multi-task learning model

---

#### Multi Task Learning with Homoscedastic Uncertainty

- Homoscedastic uncertainty
- Multi-task likelihoods

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

#### Multi-task likelihoods 

--

- Definitions:
  - For regression task, Likelihood as a Gaussian with mean given by the model output, and an observation noise scalar σ:  
![overview](assets/eq2.png)<!-- .element height="65%" width="60%" -->

  - For classification:  
![overview](assets/eq3.png)<!-- .element height="70%" width="60%" -->

  - Multi-task likelihood:  
![overview](assets/eq4.png)<!-- .element height="60%" width="60%" -->

---

- Regression tasks' maximum likelihood inference

  - for Eq2, its written as  
  ![overview](assets/eq5.png)<!-- .element height="60%" width="60%" -->
  - for multi-output:  
  ![overview](assets/eq6.png)<!-- .element height="60%" width="60%" -->

--

  - Leading to the *minimisation* objective:  
    ![overview](assets/eq7.png)<!-- .element height="60%" width="60%" -->

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

### Robustness Test

![results](assets/robustness.png)<!-- .element height="90%" width="90%" -->

---

# Thank you! 

## Questions?
