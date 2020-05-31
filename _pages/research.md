---
layout: splash
title: "Research"
permalink: /research/
classes: wide
---

<br/>
# Research
[//]: <> (Computational Fluid Dynamics (CFD) has become an indispensable tool for many engineering applications. Unfortunately, high-fidelity CFD simulations are often so computationally prohibitive that they cannot be used as often as needed or used only in special circumstances rather than routinely. Model order reduction (MOR) is a family of techniques for reducing the computational complexity of such large-scale computational models. This is where the core of my research lies!)
{: style="text-align: justify;"}

## 1. Integrating real-time sensor data into reduced order models (ROMs) using deep learning
In this work, we have developed an efficient state estimation methodology for dynamical systems where real-time sensor data is mapped to a reduced state space using deep neural networks. This framework will be highly useful for numerous real-time dynamical systems, where an approximate instantaneous state estimated from limited sensor data can be used to quickly predict the future behavior of the system using a ROM. Applications include flow control, adaptive and morphing structures, etc. More details about this work can be obtained[[here]](https://arxiv.org/pdf/1912.10553)
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/cse5.PNG" width="60%" />
</p></center>

## 2. Data-driven flow field estimation in unsteady aerodynamics
Instantaneous estimation of flow-field using limited sensor data will enable us to identify critical flow phenomena such as the onset of flow separation and/or stall, which will be crucial for applications such as flow control or autonomous decision making in unsteady aerodynamics. In this work, we propose to develop a novel flow-field estimation framework where we will model passively deployed torsionally hinged flaps as flow-field estimating sensors as shown below. This will be achieved by learning the mapping between the dynamics of the flaps and the flow-field using snapshot data.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/airfoil.PNG" width="60%" />
</p></center>

## 3. High performance computing
We are developing a parallel CFD solver for simulating fluid-structure interaction problems using MPI and PETSC. The algorithm consists of a fractional step method where the fluid equations are solved using fast Fourier transforms while the structural equations are solved using GMRES. The figure below displays the vorticity contours of the flow over two flat plates computed on 32 cores: one plate is horizontally fixed while the second plate, which is torsionally hinged, is oscillating about the trailing edge of the fixed plate.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/flow.gif" width="50%" />
</p></center>

## 4. Adaptive manifold-refinement for ROMs on nonlinear manifold using transfer learning
We are developing an adaptive manifold refinement strategy to guarantee convergence of ROMs on manifolds built using deep convolutional autoencoders. The refinement methodology includes splitting of the latent space and retraining of few selected weights of the decoder of the autoencoder.
{: style="text-align: justify;"}

## 5. Data-driven reduced order modeling of fluid flows
Traditional MOR approaches cannot be expected to efficiently provide good approximations in the case where the solutions are dominated by strong shocks or discontinuities whose spatial orientations and positions
are strongly parameter dependent. To tackle this problem, we have developed a novel "[transported snapshot model order reduction (TSMOR) approach](https://onlinelibrary.wiley.com/doi/full/10.1002/nme.5998)".
{: style="text-align: justify;"}

We have demonstrated the accuracy of our approach and computational efficient on many representative flow problems such as a 2D flow over a forward facing step resulting in multiple shock interactions and reflections and a multi-parametric combustion problem.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/step.png" width="60%" />
</p></center>

<center><p float="center">
  <img src="/assets/images/combustion.png" width="40%" />
</p></center>







