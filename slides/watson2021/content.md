
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

- Structure from Motion (SfM)

- Self-supervised monocular depth estimation methods are trained using nearby frames as a supervision signal.

- At test time, a trained network can output a depth map from a single RGB image.

---

- However:

  * For some applications, sequence information is also available

  * The vast majority of monocular methods ingore this extra information.

  * Or use test-time refinement techniques or recurrent networks.


---

## Contributions

---

* A novel self-supervised multi-frame depth estimation model

* (For SfM) Showing moving objects and static scenes impact self-supervised multi-view matching approaches and introducing solutions

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

## Comparison with other approaches 

![overview](assets/table1.png)<!-- .element height="80%" width="80%" -->

---

## Problem setup


* Single-image depth estimation
![overview](assets/eq1.png)<!-- .element height="70%" width="60%" -->

* Multi-frmae depth estimation
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


* Synthesized I<sub>t</sub>:

![overview](assets/eq3.png)<!-- .element height="70%" width="60%" -->

* Reconstruction Loss:

![overview](assets/eq4.png)<!-- .element height="60%" width="60%" -->

---

####  multi-view cost volume

* A cost volume which measures the geometric compatibility at different depth values between pixels from frames. 

![overview](assets/overview.png)<!-- .element height="100%" width="100%" -->


---

#### How to build the cost volume

* For pixel(i,j), what is the likelihood of the correct depth being d, for each d in P?



---

#### However

* d<sub>max</sub> and d<sub>min</sub> are hyperparameters.

* One assumption: world is static 

---

####  <mark>Adaptive cost volumes </mark>


* d<sub>max</sub> and d<sub>min</sub> can be learned from D<sub>t</sub>.


---

#### <mark>Addressing cost volume overfitting</mark>

---

##### Why failed?

* untextured regions
* Moiving objects (cars) 


---

##### Soluitions

* Using a seperate network to regularize

![overview](assets/eq5.png)<!-- .element height="70%" width="60%" -->

* Identifying unreliable pixels

![overview](assets/eq6.png)<!-- .element height="60%" width="60%" -->



---

![overview](assets/figure3.png)<!-- .element height="100%" width="100%" -->

---

#### <mark>Static cameras and start of sequences</mark>


* Preceding frame does not exit

    * When training, with a probability p, set the cost volume to zero.
    * At testing, same processing

---

* Camera does not move

* With a probability q, replace I<sub>t-1</sub> with I<sub>t</sub> in a color augmented version



%#### Loss function

%- ![overview](assets/eq10.png)<!-- .element height="100%" width="100%" -->

---


## Experiments

---

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

* Mutiply-add computations(MACS)

![results](assets/figure5.png)<!-- .element height="100%" width="60%" -->

---


### Ablation experiments

![results](assets/table4.png)<!-- .element height="100%" width="100%" -->

---

![results](assets/table5.png)<!-- .element height="100%" width="100%" -->

---

### Qualitative Results

---

![overview](assets/comparison.png)<!-- .element height="100%" width="100%" -->

---

# Thank you! 

## Questions?
