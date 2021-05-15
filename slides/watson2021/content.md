
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

* A novel self-supervised multi-frame depth estimation model

* Showing moving objects and static scenes impact self-supervised multi-view matching approaches and introduce solutions

* An adaptive cost volume to overcome the scale ambiguity 

---

### Model Overview

![overview](assets/overview.png)<!-- .element height="100%" width="100%" -->

---

## Related Work

* Monocular depth estimation

* Multi-frames monocular depth estimation

* Deep multi-view depth estimation

---

![overview](assets/table1.png)<!-- .element height="80%" width="80%" -->

---

## Problem setup


![overview](assets/eq1.png)<!-- .element height="70%" width="60%" -->

![overview](assets/eq2.png)<!-- .element height="60%" width="60%" -->

---

## Methods

- self-supervised projection based training
- Multi-view cost volume:
- <mark>Adaptive cost volumes </mark>
- <mark>Addressing cost volume overfitting</mark>
- <mark>Static cameras and start of sequences</mark>


---

####  self-supervised projection based training


![overview](assets/eq3.png)<!-- .element height="70%" width="60%" -->

![overview](assets/eq4.png)<!-- .element height="60%" width="60%" -->

---

####  multi-view cost volume


![overview](assets/overview.png)<!-- .element height="100%" width="100%" -->

---


####  <mark>Adaptive cost volumes </mark>



---

#### <mark>Addressing cost volume overfitting</mark>

![overview](assets/eq5.png)<!-- .element height="70%" width="60%" -->

![overview](assets/eq6.png)<!-- .element height="60%" width="60%" -->

---


#### <mark>Static cameras and start of sequences</mark>


![overview](assets/figure3.png)<!-- .element height="100%" width="100%" -->


---

#### Loss function
- ![overview](assets/eq10.png)<!-- .element height="100%" width="100%" -->

---


## Experiments

--

#### Dataset

- KITTI
- CityScapes


---

### Quantitive Comparison

![results](assets/table2.png)<!-- .element height="100%" width="100%" -->

---

![results](assets/table3.png)<!-- .element height="100%" width="100%" -->


---

### Efficiency comparison

![results](assets/figure5.png)<!-- .element height="100%" width="60%" -->

---


### Ablation experiments

![results](assets/table4.png)<!-- .element height="100%" width="100%" -->

--

![results](assets/table5.png)<!-- .element height="100%" width="100%" -->

---

### Qualitative Results

--

![overview](assets/comparison.png)<!-- .element height="100%" width="100%" -->

---

# Thank you! 

## Questions?
