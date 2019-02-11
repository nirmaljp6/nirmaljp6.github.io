---
layout: single
title: "Research Interests"
permalink: /research/
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/step2.png
---

My research interests lie in the intersection of computational fluid dynamics and data-driven reduced order modeling particularly applied to problems in aerodynamics. 

# Data-driven methods + Computational fluid dynamics
Computational Fluid Dynamics (CFD) has become an indispensable tool for many engineering applications. Unfortunately, high-fidelity CFD simulations are often so computationally prohibitive that they cannot be used as often as needed or used only in special circumstances rather than routinely. Model order reduction (MOR) is a family of techniques for reducing the computational complexity of such large-scale computational models. This is where the core of my research lies!
{: style="text-align: justify;"}

## Data-driven flow field estimation
In many applications such as flow control or autonomous decision making in unsteady aerodynamics, it is important to identify the flow-field around a wing using only limited real-time information from sensors. Estimation of flow-field will enable us to identify critical phenomena such as the onset of flow separation and/or stall.
{: style="text-align: justify;"}

As part of my Ph.D. thesis, I will be modeling passively deployed torsionally hinged flaps as flow-field estimating sensors as shown below. This will be achieved by mapping the motion of the flaps to the known flow-field data obtained at various other flow configurations by solving an off-line optimization problem.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/airfoil.PNG" width="80%" />
</p></center>

### High performance computing
Currently, I am developing an in-house parallel CFD solver built using MPI and PETSC to collect flow-field data for different flap-parameters and flow conditions. To gain expertise on parallel programming using PETSC, I had recently built a 2D advection-diffusion solver using Krylov subspace methods and fast Fourier transforms simulating a moving Gaussian as shown below.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/1.png" width="40%" />
  <img src="/assets/images/2.png" width="40%" /> 
</p></center>

## Data-driven reduced order modeling of fluid flows
Traditional MOR approaches cannot be expected to efficiently provide good approximations in the case where the solutions are dominated by strong shocks or discontinuities whose spatial orientations and positions
are strongly parameter dependent. To tackle this problem, I have developed a novel "[Transported snapshot model order reduction approach for parametric, steady-state fluid flows containing parameter
dependent shocks](https://onlinelibrary.wiley.com/doi/full/10.1002/nme.5998)".
{: style="text-align: justify;"}

We have demonstrated the accuracy of our approach on many representative flow problems such as the one shown below. Here we accurately predict the solution of a 2D flow over a forward facing step where mutiple shock interactions and reflections can be clearly observed.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/step.png" width="90%" />
</p></center>


In the figure displayed below, we have demonstrated the computational efficiency on a multi-parametric combustion problem. For this problem we obtain a computational speedup of 2 orders of magnitude compared to the high-dimensional model.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/combustion.png" width="70%" />
</p></center>



# Computational fluid dynamics
## Passive flow control using vortex generators
I studied passive flow control using vortex generators to delay shock induced flow separation on Onera M6 wing in transonic flow regime using Ansys Fluent.






