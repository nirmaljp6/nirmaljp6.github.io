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
[//]: <>(**Keywords**: computational fluid dynamics; deep learning; reinforcement learning; high-performance computing; reduced-order modeling)

## 1. Bio-inspired flow control using computational fluid dynamics and machine learning
Flow control is a process of manipulating the flow to achieve desirable aerodynamic performance. The flow control technique in this work is inspired from covert feathers in birds---a set of self-actuating feathers located on the suction surface of the wings. During unsteady flow separation, these feathers protrude into the flow and provide lift enhancements, for reasons that are still not understood. We study the utility of covert feathers as a both passive and active flow control technique.
{: style="text-align: justify;"}

### Passive flow control

We numerically investigated a model system in which a passively deployable, torsionally hinged flap is mounted on the suction surface of a stationary airfoil via high-fidelity nonlinear simulations as shown in the figure below. A parametric study performed by varying several flap parameters yielded lift improvements as high as 27% relative to the baseline flap-less case. A k-means clustering algorithm with carefully chosen inputs revealed two dominant flow behavioral regimes responsible for these lift improvements. Further details about this work can be found [[here]](https://arxiv.org/pdf/2203.00037.pdf) and [[here]](https://arc.aiaa.org/doi/abs/10.2514/6.2022-1968). We have also collaborated with [Prof. Aimy Wissa's group](https://mae.princeton.edu/people/faculty/wissa) to compare our numerical results with their wind-tunnel experiments.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/passivefc.png" width="30%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/maps.png" width="60%" />
</p></center>

<!---
  <img src="/assets/images/passivefc.png" width="30%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/liftimp.png" width="40%" />
-->

### Active flow control using reinforcement learning

We are currently designing an active flow control counterpart of the above-mentioned passive flow control strategy for further augmenting the airfoil lift. Using reinforcement learning, we are developing a closed-loop feedback controller for actuating the hinge stiffness as shown in the figure below. The controller is constructed to maximize reward or aerodynamic lift under unsteady gust conditions. A neural network architecture is used to construct the controller/agent which takes the flow-state of the system as the input and outputs the instantaneous value of stiffness. PPO, a policy gradient optimization algorithm is used to train the agent. The results will be updated soon.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/rl.png" width="60%" /> &nbsp; &nbsp; &nbsp; &nbsp;
</p></center>

## 2. Flow-field state estimation using deep learning
In this work, we have developed an efficient state estimation methodology for dynamical systems where real-time sensor data is mapped to a reduced state space using deep neural networks. This framework will be highly useful for numerous real-time dynamical systems, where an approximate instantaneous state estimated from limited sensor data can be used to quickly predict the future behavior of the system using a ROM. Applications include flow control, adaptive and morphing structures, etc. More details about this work can be obtained[[here]](https://arxiv.org/pdf/1912.10553)
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/se.png" width="60%" />
</p></center>

## 3. High performance computing and development of efficient algorithms
The in-house CFD code that we use to simulate fluid-structure interactions (FSI) has two crucial drawbacks: (a) it lacks the scalability required to perform large-scale simulations across several processors (CPUs), and (b) it has a severe computational bottleneck that deals with how the fluid and structural dynamics are coupled to each other, and this bottleneck has not  been  addressed  in  literature.  To  tackle  these  issues,  we have developed  a scalable   and efficient   FSI  algorithm using   PETSC/MPI that employs   a  novel precomputable fluid-structure coupling strategy  and leverages  the  parallel  computing capabilities  of  supercomputers.  Further details about this work can be found [[here]](https://www.sciencedirect.com/science/article/pii/S0021999121007920).
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/hpc.png" width="60%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/speedup.png" width="30%" />
</p></center>
<!---
We are developing a parallel CFD solver for simulating fluid-structure interaction problems using MPI and PETSC. The algorithm consists of a fractional step method where the fluid equations are solved using fast Fourier transforms while the structural equations are solved using GMRES. The figure below displays the vorticity contours of the flow over two flat plates computed on 32 cores: one plate is horizontally fixed while the second plate, which is torsionally hinged, is oscillating about the trailing edge of the fixed plate.
{: style="text-align: justify;"}
-->


## 4. Guaranteeing convergence of reduced-order models (ROM) using transfer learning
Recently, deep convolutional autoencoders have been used to construct nonlinear manifolds for model order reduction. However, attaining guaranteed convergence of these reduced-order models, specifically for future time predictions, has been a significant challenge due to the nonlinear nature of the manifold. In this project, we worked on developing an adaptive  manifold refinement strategy wherein (a) the basis (or the first fully connected layer) of the latent space of the decoder was split to form a larger subspace and (b) few selected weights of the decoder neural network were retrained efficiently. By adaptively increasing the latent space basis and the number of weights trained for transfer learning, convergence of the nonlinear ROM was expected. This approach was tested on a one-dimensional Burgers equation involving a traveling shock wave. 
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/hadap.png" width="40%" />
</p></center>


## 5. Data-driven reduced order modeling of fluid flows
Traditional ROM approaches cannot be expected to efficiently provide good approximations in the case where the solutions are dominated by strong shocks or discontinuities whose spatial orientations and positions
are strongly parameter dependent. To tackle this problem, we developed a model order reduction method where certain selected snapshots are transported in parameter space according to precomputed transport velocities and are used to construct a locally linear subspace. We demonstrated the accuracy and computational efficiency of our approach on many representative flow problems such as a supersonic two-dimensional flow over a forward facing step resulting in multiple shock interactions and reflections and a multi-parametric combustion problem. Further details about this work can be found [[here]](https://onlinelibrary.wiley.com/doi/full/10.1002/nme.5998).
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/step.png" width="50%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/combustion.png" width="33%" />
</p></center>

<br/>
# Selected Course Projects

## 1. Nonlinear modal decomposition in fluid dynamics using deep convolutional autoencoders
We developed a nonlinear modal decomposition framework for accurately representing transient fluid flows where traditional techniques perform poorly. In this approach, the flow structures identified by the manifold were analyzed by identifying the principle directions of the low-dimensional latent space. The nonlinear manifold was constructed using a deep convolutional autoencoder. The proposed framework was demonstrated to reconstruct and identify dominant and meaningful flow structures in a transient flow ensuing from an impulsive motion of a flat plate at a large angle of attack.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/cae.png" width="60%" />
</p></center>

## 2. Aeroacoustics of vortex shedding about a stalled airfoil
Ffowcs Williams-Hawkings (FWH) equation for predicting acoustic pressure was numerically solved using the Farassat Formulation 1A. This formulation has been used for predicting helicoptor rotor and propeller noise. First, the code was validated against analytical solutions consisting of stationary and moving monopoles. The validated code was then used to predict vortex shedding noise about a stalled airfoil.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/caevs.png" width="30%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/directivity.png" width="30%" />
</p></center>

## 3. Shock induced flow separation control using vortex generators
Shock induced flow separation during transonic flow conditions decreases the aerodynamic performance of the wing. In this work, passive flow control of transonic flow past an Onera M6 wing using vortex generators was studied. The CFD simulations were performed on Ansys Fluent. Velocity contours at various spanwise locations revealed delay of shock downstream, reduced flow separation and associated improvements in the lift to drag ratio, implying that the vortex generators improved the aerodynamic performance of the wing.
{: style="text-align: justify;"}
<center><p float="center">
  <img src="/assets/images/mesh.png" width="30%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/cpfluent.png" width="30%" /> &nbsp; &nbsp; &nbsp; &nbsp;
  <img src="/assets/images/ansys.png" width="70%" />
</p></center>



