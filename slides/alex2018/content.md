
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

--

- A model trained under multi-task learning can outperform separate models trained individually on each task:
  * Sematic Segmentation
  * Instance Segmentation
  * Depth Estimation

---

## Contributions

--

* A novel and principled multi-task loss to simultaneously learn various classification and regression losses of varying quantities and units using *homoscedastic* task uncertainty

* A unified architecture for semantic segmentation, instance segmentation and depth regression

* Demonstrating the importance of loss weighting in multi-task deep learning and how to obtain superior performance compared to equivalent separately trained models.

---

### Model Overview

![overview](assets/network.png)<!-- .element height="80%" width="80%" -->

---

## Related Work

![overview](assets/ablation.png)<!-- .element height="80%" width="80%" -->

---

## IDEAS

- Use homoscedastic uncertainty to weight the losses in multi-task learning models

- Since homoscedastic uncertainty does not vary with input data, they interpret it as task uncertainty. 

---

#### Multi Task Learning with Homoscedastic Uncertainty

- Homoscedastic uncertainty
- Multi-task likehoods

--

#### Homoscedastic uncertainty

--

#### Multi-task likehoods 

---

## Scene Understanding Model

---

## Experiments

--

#### Dataset

- CItyScpaes

---

### Quantatiive Comparison

![results](assets/comparison.png)<!-- .element height="70%" width="70%" -->

---

### Ablation experiments

![results](assets/comparison_1.png)<!-- .element height="50%" width="50%" -->

---

### Qualitative Results

![results](assets/results.png)<!-- .element height="70%" width="70%" -->

---

# Thank you! 
## Questions?