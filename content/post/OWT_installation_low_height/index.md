---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "To install future supertall floating offshore wind turbines in deep sea"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2021-05-15T22:12:45+02:00
lastmod: 2021-05-15T22:12:45+02:00
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

## To install future supertall floating offshore wind turbines in deep sea

Among different renewable energy sources, wind power shows great promise due to its relatively high technological readiness level, abundant availability, and relatively low environmental footprint. Energy harvesting via conventional wind turbines is achieved by converting the kinetic energy of the wind into mechanical power through blade rotation, and then into electrical power through generators. 

Compared with onshore wind turbines, offshore wind turbines (OWTs) have many advantages, e.g., abundant wind resources, lower turbulence, substantial space for establishment, lower transmission and distribution losses, less visual impact, and less noise pollution. Given these notable advantages that guarantee reliable energy production, there has been a rapid increase in the demand of OWTs in the last two decades.

The sizes and weights of OWT structures have grown dramatically. For example, the height of the newly launched 15MW wind turbine from Vestas reaches 261 m, while the Eiffel tower is only 324 m tall. Though the benefits of extremely large structures are welcomed by industry and researchers, the trend engenders new challenges with the offshore installation process. With increasing installation heights and increasing weights of the payloads, higher and more powerful cranes are required to accomplish the specific offshore operations. For some complex projects, only a small range of vessels is capable of executing the tasks, which may limit the development of the relevant industry. It is easy to image the challenges to installation an Eiffel tower, especially the tower floats on the water and moves with waves.

<figure>
  <img src="/research/OWT_installation_low_height/Picture2.png" alt="{}" style="width:70%" >
  <figcaption>Wind turbines are becoming bigger and bigger.  </figcaption>
</figure>

A novel OWT installation concept is proposed by SFI MOVE research group from NTNU. A low-height lifting system is employed to execute the installation process. The superstructures, including tower, nacelle, and rotor, are preassembled onshore and carried to the installation site. The spar-type substructure is assumed to be pre-installed at the location. The installation is accomplished with only one lift operation, resulting in a higher installation efficiency. Besides, we do not need to build bigger and higher cranes to increasing higher OWT superstructures. A newly developed idea is to lift the preassembly using several groups of lift wires, which connects at the tower of the preassembly.

<figure>
  <img src="/research/OWT_installation_low_height/Picture3.jpg" alt="{}" style="width:70%" >
  <figcaption>Novel low-height lifting system </figcaption>
</figure>

The vessel-crane-payload-control system are fully coupled with the wind and wave conditions. “To analyze the system dynamics, we tried to use a simplified model to answer for most of the complex phenomena”, said Prof. Karl Henning Halse.

A lift wire can only provide tension when the elongation is larger than or equal to zero; otherwise, the cable is loose. Another challenge is that there are so many lift wires in the system. Such a complex system is a nightmare to control system designer.

Inspired by knowledge from localization and inverse dynamics, the research team proposed a model-free control strategy to achieve an anti-swing control which stabilizes the payload in the air at the tower bottom center and maintains the orientation such that it achieves a smooth mating operation.

<figure>
  <img src="/research/OWT_installation_low_height/Picture4.png" alt="{}" style="width:70%" >
  <figcaption>The innovative idea of the model-free control strategy </figcaption>
</figure>

The position of a node is known in three-dimensional space if the distances from the unknown node is measured to at least four landmark points with known positions. We assume that all lift wires are tight with positive tension. Hence, if a payload is lifted by at least four lift wires, on which the connecting points are closed, the position of the connecting point (pci) is easily calculated when the lengths of the lift wires (l1, · · · , l4) and the positions of their base ends (pb1, · · · , pb4) are known. Additionally, the translational motion and rotation of the entire payload are determined if the positions of two connecting points on a payload are controlled.

This idea not only works for OWT installation, but also for the other marine systems. Different from the complex theoretical deduction in many academic journal papers, the proposed control law is much friendly.

This is a promising research topic. The control strategy is robust and accurate, exactly what we need to deal with the complex lifting tasks proposed in this concept.


**Ref:** Z Ren, AS Verma, B Ataei, KH Halse, HP Hildre. Model-free anti-swing control of complex-shaped payload with offshore floating cranes and a large number of lift wires, Ocean Engineering 228, 108868
