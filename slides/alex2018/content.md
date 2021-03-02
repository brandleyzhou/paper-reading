
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

#### However

- Performance is highly dependent on an appropriate choice of weighting between each task’s loss

- Tuning these weights by hand is a difficult and expensive process, making multi-task learning prohibitive in practice.

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

---

## Method

---

#### Multi Task Learning with Homoscedastic Uncertainty

--

#### Homoscedastic uncertainty

--

#### Multi-task likehoods 

---

## Scene Understanding Model

---

## Experiments

--

#### Data

---

## Conclusions

--

### Qualitative Results

![results](assets/results.png)<!-- .element height="70%" width="70%" -->

---

# Thank you! 
## Questions?