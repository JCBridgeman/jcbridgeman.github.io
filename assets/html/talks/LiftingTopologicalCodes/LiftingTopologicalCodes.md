---
marp: true
math: mathjax
size: 16:9
title: "Lifting topological codes: Single-shot codes from topological order"
theme: JCB
footer: 
    <a href="https://jcbridgeman.github.io/" class="left">jcbridgeman.github.io</a>
    <div class="center"> Lifting topological codes </div>
    <a href="https://arxiv.org/abs/2305.06365" class="right">arXiv:2305.06365</a>
---

<!-- _class: "titleSlide" -->
<!-- _footer: "<div class='right'>EQUS — Sydney University, October 2023</div>" -->

<div class="presentationTitle"> Lifting topological codes: <br> Single-shot codes from topological order</div>

<div class="presentationAuthors"> Jacob Bridgeman, Aleks Kubica, and Mike Vasmer </div>

<a href="https://arxiv.org/abs/2305.06365" class="presentationArxiv"> arXiv:2305.06365</a>

<div style="right: 0; bottom: 1.5rem; padding: 25px; position: absolute;">
<img src="./assets/img/FWO_Logo_Negatief.png" width="150px" >
</div>

---

<!-- _header: Overview -->
<!-- _class: twocolumn -->

<div class="left">

1. Main idea

2. Subsystem codes

3. Single-shot QEC

4. Gauge color codes

5. Subsystem toric code

5. Subsystem abelian quantum double codes

7. Summary

</div>

<div class="right" style="padding-top:80px">
<img src="./assets/img/gaugeColorCodeBulk.png" style="width:475px; margin-right: 10px;"/>
</div>

---

<!-- _header: Main idea -->

- Use 2D topological codes + 3D geometry to construct 3D subsystem codes with single-shot QEC

<div align="center">


<img src="./assets/img/disjointSpheres.gif" width="400px">

</div>

---

<!-- _header: Subsystem codes -->
<!-- _class: twocolumn -->

<div class="top">

$$\mathcal{H} \simeq (\mathcal{C}\otimes\mathcal{J})\oplus \mathcal{H}^\perp$$

All stabilizer codes are subsystem codes ($\mathcal{J} = \mathbb{C}$)

Pauli subsystem codes:
</div>

<div class="left" style="border-right: 1px solid var(--theme-color,var(--theme-color-default));">

- $\mathcal{G} \leq \mathcal{P}^n$ : *Gauge* group (nonabelian)

- $\mathcal{S} \approx \mathcal{Z}(\mathcal{G})$ : Stabilizer group
- $\mathcal{C}\otimes\mathcal{J} = E_{+1}(\mathcal{S})$
</div>

<div class="right">
Examples:

- Bacon-Shor code
- Gauge color code
- Subsystem toric code
</div>

<div class="bottom">

Given a stabilizer code, add some logical pairs to $\mathcal{S}$ to get a subsystem code
</div>

---

<!-- _header: Subsystem codes | ⟦4,2,2⟧ ⟶ ⟦4,1,2⟧ -->

⟦4,2,2⟧ stabilizer code:
<div align="center">

$\mathcal{S} = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabX.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabZ.png" > $\bigg\rangle$
</div>

Two logical qubits: 

<div align="center">

$\overline{X_1}=$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/LX1.png" > &nbsp;&nbsp;$\overline{Z_1}=$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/LZ1.png" > &nbsp;&nbsp;$\overline{X_2}=$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/LX2.png" > &nbsp;&nbsp; $\overline{Z_2}=$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/LZ2.png" >
</div>


<div style="border-top:1px solid var(--theme-color,var(--theme-color-default));">

⟦4,1,2⟧ subsystem code: 
<div align="center">

$\mathcal{G} = \langle \mathcal{S}, \overline{X_2}, \overline{Z_2} \rangle = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX1.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX2.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GZ1.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GZ2.png" > $\bigg\rangle$
</div>
</div>

---
<!-- _header: Subsystem codes | Why?-->


- Lower weight check operators

- More fault-tolerant logical gates

- More general formalism &ndash; Possibility for novel codes

- **Single-shot QEC**

---

<!-- _header: Single-shot QEC -->
<!-- _class: twocolumn -->

<div class="left">

- Bombin | [arXiv:1404.5504](https://arxiv.org/abs/1404.5504)

- Single-shot QEC: correct errors in a single round of syndrome measurement

    - Even with measurement errors

</div>

<div class="right" data-marpit-fragment>
<img src="./assets/img/measurementError.png" style="width:300px;"/>
</div>

---

<!-- _header: Gauge color codes -->
<!-- _class: twocolumn -->

<div class="left">

- 3 (space) dimensional subsystem codes

- Defined on 4-colorable lattices

- Gauge operators defined on 2D faces $\mathcal{G} = \langle \otimes_{i\in\text{face} }X_{i}, \otimes_{i\in\text{face} }Z_{i}\rangle$

- Stabilizer operators associated to volumes $\mathcal{S} = \langle \otimes_{i\in\text{volume} }X_{i}, \otimes_{i\in\text{volume} }Z_{i}\rangle$
</div>

<div class="right" style="padding-top:10px">
    <img src="./assets/img/gaugeColorCodeBulk.png" style="width:475px"/>
</div>

---

<!-- _header: Gauge color codes | Gauge flux -->
<!-- _class: twocolumn -->

<div class="left">

- Non-abelian gauge group $\implies$ gauge measurement outcomes are random
- Gauge flux is the pattern of $-1$ outcomes
- Although outcomes are locally random, they are correlated
    - Product of gauge flux at a stabilizer must be $+1$
    - There may be other constraints
</div>

<div class="bottom" style="padding-top:10px">
<img src="./assets/img/gaugeColorCodeBulk.png" style="width:475px"/>
</div>

---
<!-- _header: ⟦4,1,2⟧ Code | Gauge flux -->

⟦4,1,2⟧ subsystem code: 
<div align="center">

$\mathcal{G} = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX1.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX2.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GZ1.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GZ2.png" > $\bigg\rangle$

$\mathcal{S} = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabX.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabZ.png" > $\bigg\rangle$
</div>


<div align="center">
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_A.png" data-marpit-fragment>&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_B.png" data-marpit-fragment>&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_C.png" data-marpit-fragment>
</div>

---
<!-- _header: Gauge flux | Measurement errors -->

<div align="center">

$\mathcal{G}_{X} = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX1_R.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX2_R.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX3_B.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/GX4_B.png" > $\bigg\rangle$

$\mathcal{S} = \bigg\langle$ <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabX.png" > &nbsp;,&nbsp; <img style="display:inline-block;vertical-align: middle;" width="75px" src="./assets/img/412/stabZ.png" > $\bigg\rangle$
</div>


<span align="center">
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_R_A.png" >&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_R_B.png" >
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_ME_A.png" >&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_ME_B.png" >
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_Measurement.png" >
<br><br>
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_B_A.png" >&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_B_B.png" >
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_ME_C.png" >&nbsp;&nbsp;&nbsp;
<img style="display:inline-block;vertical-align: middle;" width="150px" src="./assets/img/412/gaugeFlux_ME_D.png" >
</span>

---
<!-- _header: Gauge color codes | Observations -->
<!-- _class: twocolumn -->


<div class="left">
<img src="./assets/img/gaugeColorCodeBulk.png" style="width:400px"/>
</div>
<br>
<div  class="right">
<img src="./assets/img/2DColorCodes.png" style="width:650px; padding-bottom:0px; margin-bottom: 0px"/>
</div>

<div class="bottom">

* Each volume forms a 2D *stabilizer* color code
* Qubits are *shared* between neighboring codes
* Each stabilizer can be reconstructed in 3 ways &ndash; redundancy
* Gauge fluxes can be interpreted as anyons on the 2D color codes
* Net neutral charge on sphere $\implies$ Gauss law for gauge flux
</div>

---

<!-- _header: Subsystem toric code -->

- Introduced in [arXiv:2106.02621](https://arxiv.org/abs/2106.02621)
- More elementary than gauge color code
- Separates stabilizer constraints from topological constraints (Gauss law)
- Gauge operators associated to 2D faces and vertices

<div align="center">

<img src="./assets/img/sphereCubicLattice.png" width="350px">
<img src="./assets/img/sphereCubicLattice_triangulated.png" width="350px">
</div>

---

<!-- _header: Subsystem toric code | Stabilizers -->

<div align="center">

<img src="./assets/img/ZStabilizerBulk.png" height="200px"> <img src="./assets/img/XStabilizerBulk.png" height="200px">

</div>

- Associated to volumes of the lattice

- Each stabilizer can be reconstructed in 2 ways &ndash; from only green or only yellow gauge operators

---

<!-- _header: Subsystem abelian quantum double code -->
<!-- _class: twocolumn -->

<div class="right">
<img src="./assets/img/sphereCubicLattice_triangulated.png" width="350px">

<img src="./assets/img/abelianQDFace.png" height="200px"> <img src="./assets/img/abelianQDVertex.png" height="200px">
</div>

<div class="left">

- Instead of $\mathbb{Z}_2$ (toric code), use $\mathbb{Z}_d$

- $e$ and $m$ type anyon fusion rules dictate gauge flux Gauss law
</div>

---

<!-- _header: Subsystem abelian quantum double code | Gauge flux -->
<!-- _class: twocolumn -->


<div class="left">

1. In code space, stabilizers are $+1$, so total gauge flux (of either color) into volume must be $+1$
2) When there are physical errors, there is a net charge on a volume
    * Redundancy $\implies$ green charge = yellow charge
    * Vertices necessarily have *no* net charge, even with physical errors
3) Measurement errors can result in net charge on vertices or mismatch of charge measured at volumes
</div>

<div class="right" style="text-align:center">
<figure>
<figcaption>Physical errors only</figcaption>
  <img src="./assets/img/gaugeFlux_physical.png" height="200px">
</figure>
<figure>
    <figcaption>Physical and measurement errors</figcaption>
  <img src="./assets/img/gaugeFlux_unphysical.png" height="200px">
</div>

---

<!-- _header: Error correction -->

Error correction is a two step process:
1) Validate gauge flux to remove broken loops
    - Identify end points of broken loops and match them up

2) Correct residual errors to ensure charge on volumes is neutral
    - Identify stabilizer violations and match them up

---

<!-- _header: 'Single-shot QEC | numerical evidence' -->
<!-- _class: twocolumn -->

<div class="left">

QEC step:

1. Apply channel to each qudit

2. Compute gauge syndrome

3. Randomize each gauge outcome with probability $p$

4. Find recovery operator:
    1. Validate flux (clustering)
    2. Correct errors (clustering)

</div>

<div class="right" style="font-size:1.5rem;">

Error channel: $\mathcal{E}(\rho) := (1-p)\rho + \frac{p}{d-1} \sum_{j=1}^{d-1} Z^j \rho Z^{-1}$

<img src="assets/img/numerics_threshold.png" style="width:570px;">

</div>

---

<!-- _header: Boundaries -->
<!-- _class: twocolumn -->

<div class="left">

- Unlike topological codes, these subsystem codes require boundaries to have logical qudits

- Our perspective lets us construct boundaries from boundaries of 2D topological models

- On $\mathbb{T}^2 \times [0,1]$, macroscopic copies of the 2D code are used to define the gauge operators

</div>

<div class="right" style="padding-top:80px">
<img src="./assets/img/T2xI_top.png" style="width:400px; margin-left:30px"/>
</div>

---

<!-- _header: Boundaries | Encoded qubits -->
<!-- _class: twocolumn -->

<div class="left">

- Logical qubits associated with boundary 2D codes
- Bare logical operators are sheet-like
- Dressed logicals are boundary string operators

</div>

<div class="right">
<iframe src="./assets/html/LogicalT2xI.html" scrolling="no" frameBorder="0">
</iframe>
</div>

---

<!-- _header: Boundaries -->

When defined on a cube, we can use the boundaries of the 2D code to define the gauge operators

<iframe src="./assets/html/roughBoundary.html" scrolling="no" frameBorder="0"  style="height:365px;width:365px;"></iframe>
<iframe src="./assets/html/RoughSmoothCorner.html" scrolling="no" frameBorder="0" style="height:365px;width:365px;"></iframe>
<iframe src="./assets/html/smoothBoundary.html" scrolling="no" frameBorder="0" style="height:365px;width:365px;"></iframe>

---

<!-- _header: Summary -->

- New perspective on topological subsystem codes
    - Single-shot property arising from interplay of *2D topological order* and *3D geometry*

- This perspective provides a **natural** generalization to any abelian group/(untwisted) abelian QD anyon model
    - Includes boundaries and logical operators
    
---

<!-- _header: Summary -->

- Beyond Pauli case?
    - Currently working on semion version. Seems to need a different geometry
    - Non-abelian case?
    - General string-net models?

- Can we fit the gauge color code into this framework?
    - The split between Gauss law and stabilizers is not as clear
    - What is the correct notion of equivalence for subsystem codes?

---

<!-- _class: questionSlide --> 
<!-- _header: "" -->
<!-- _footer: "" -->

Any questions?

[arXiv:2305.06365](https://arxiv.org/abs/2305.06365)


<span> Slides available at [jcbridgeman.github.io](https://jcbridgeman.github.io) </span>

<script type="text/javascript">
var sc_project=11717036; 
var sc_invisible=1; 
var sc_security="78149843"; 
</script>
<script src="https://www.statcounter.com/counter/counter.js"
async></script>
<noscript><div class="statcounter"><a title="site stats"
href="https://statcounter.com/" target="_blank"><img
class="statcounter"
src="https://c.statcounter.com/11717036/0/78149843/1/"
alt="site stats"></a></div>
</noscript>