---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Sea state estimation based on vessel responses"
subtitle: ""
summary: "We introudce Bezier suface and sparse regression to wave buoy analog."
authors: []
tags: []
categories: []
date: 2021-04-06T00:26:00+02:00
lastmod: 2021-04-06T00:26:00+02:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## Sea state estimation from vessel motion responses: Smoothness and robustness using Bezier surface and L1 optimization

The complexity of the ocean environment is challenging for safe voyages and marine operations. An important consideration is thereby given to the sea states at the planning and operating stages for an offshore project. The wave spectra can be measured and detected by several measurement instruments. This paper presents nonparametric sea state estimation based on vessel motion responses (wave buoy analogy).

<figure>
  <img src="/research/sea_state_est/foundation.PNG" alt="{Foundation of wave buoy analogy}" style="width:100%">
  <figcaption>Fig 1. Foundation of wave buoy analogy </figcaption>
</figure>

Because a vessel is asymmetric, the cross spectra of 6DOF vessel motions $S_{ij}^{wave}$ are related to wave spectra S_wave. The relationship between the vessel motions and wave spectra are characterized by response amplitude operators (RAO), which are influenced by the hull geometry and can be calculated by well-known hydrodynamic formulas. After discretizing the directional spectrum concerning incoming wave direction $\beta_k$ and wave frequency $\omega_m$, respectively, a linear equation $b=Af$ is formulated according to the hydrodynamics with a tall matrix $A$; shown in Figure 2. The vector of directional wave spectrum f can be solved as an inverse problem. However, the best-fit solution in this application does not always give a practical meaning. To solve the problem, typical least square (LS) methods are adopted with additional implicit smoothness conditions existing in a spectrum. The research innovatively augments this classic setup in two aspects.

<figure>
  <img src="/research/sea_state_est/coordinate.PNG" alt="{Definition of angles and discretization of the wave field}" style="width:50%" >
  <figcaption>Fig 2. Definition of angles and discretization of the wave field </figcaption>
</figure>

First, two-dimensional smoothness is achieved using the Bézier surface. Instead of considering the constant slopes between a node and its two neighbor nodes in the wave direction and frequency, respectively, the size of the smoothness scope in the discretized network can be arbitrarily selected (see Figure 3). The new smoothness condition is a more general form, where a Bézier surface is the Cartesian product of two orthogonal Bezier curves. The classic constant-slope condition is a particular example of a Bézier curve with three nodes.

<figure>
  <img src="/research/sea_state_est/bezier_smooth.PNG" alt="{Bézier surface in the discretized network}" style="width:50%" >
  <figcaption>Fig 3. Bézier surface in the discretized network </figcaption>
</figure>

Second, the potential of sparseness in the ocean wave spectrum is realized through L1 optimization. The sparsity pattern of a wave spectrum with a threshold of 0.1 reveals the powerful components in the wave spectrum; see Figure 4. Converting from time-domain sampling, disturbances are noticed in the discretized motion cross-spectra, resulting in extra risks to the estimate results. Since L1 optimization is more robust to wildpoints, sparse regression is adopted in the inverse problem. The simulation results (e.g., in Figure 5) verify that the L1 norm $(1,1,1,1)$ has much higher robustness against the disturbances and errors in the vessel response spectrum than the LS methods $(2,2,2,2)$. The estimate given by the LS cost function $(p_1,r_1,p_2,r_2 )= (2,2,2,2)$ is risky. The estimates of L1 optimization $(p_1,r_1,p_2,r_2 )= (1,1,1,1)$ is “cleaner” showing a higher sparsity, and the energy in the estimated shows a better concentration.

<figure>
  <img src="/research/sea_state_est/sparsity.PNG" alt="{Sparsity of a directional wave spectrum with different thresholds}" style="width:70%" >
  <figcaption>Fig 4. Sparsity of a directional wave spectrum with different thresholds </figcaption>
</figure>

<figure>
  <img src="/research/sea_state_est/spectrum_est.PNG" alt="{The performance comparison of L1 optimization with classic least square methods}" style="width:150%" >
  <figcaption>Fig 5. The performance comparison of L1 optimization with classic least square methods </figcaption>
</figure>

**Ref:** *Zhengru Ren, Xu Han, Amrit Shankar Verma, and Johann Alexander Dirdal, Roger Skjetne. Sea state estimation based on vessel motion responses: improved smoothness and robustness using Bézier surface and L1 optimization. Marine Structures, 2021. In press. Available online.* [[PDF](</papers/[1.18][compressed]Sea state estimation based on vessel response improved smoothness and robustness using B´ezier surface and L1 optimization.pdf>)]

**Report**: [Norwegian SciTech News](https://norwegianscitechnews.com/2021/03/using-ships-themselves-to-monitor-and-predict-ocean-conditions/), 
[EurekAlert](https://www.eurekalert.org/pub_releases/2021-03/nuos-ust031821.php), 
[Press-News](https://press-news.org/158275-using-ships-themselves-to-monitor-and-predict-waves.html), 
[One American Northwest Arkansas](https://oanwa.com/science/using-ships-themselves-to-monitor-and-predict-waves/), 
[WorldNewsEra](https://worldnewsera.com/news/science/using-ships-themselves-to-monitor-and-predict-waves/)