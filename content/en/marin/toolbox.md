---
widget: blank
headless: true
weight: 10
title: MarIn toolbox
subtitle:
date: 2021-04-05

# Section design
design:
  # Use a 1-column layout
  columns: "1"
  # Use a dark navy background with light text.
  background:
    color: 'navy'
    text_color_light: true
---


MarIn (Marine Installation) toolbox is an open-source modularized blade installation simulation toolbox for the purpose of control design in MATLAB/Simulink. Cooperating with MSS toolbox, MarIn can simulate all sorts of offshore operations. [[Download]](https://github.com/NTNU-MCS/MarIn)

<figure>
  <img src="/research/marin/overview_marin.PNG" alt="{}" style="width:60%" >
  <figcaption>Overview of MarIn toolbox </figcaption>
</figure>

The full-version toolbox with turbulence wind box can be download at:
<https://www.dropbox.com/s/g7jxpmyrmy0pkme/Marin_blade_v1_0.zip?dl=0>.

Key Features:
- MATLAB/Simulink interface;
- Open-source & object-oriented toolbox;
- Developed for the purpose of control design;
- Compatible with MSS toolboxes;
- Floating and fixed installation vessels;
- Turbulent wind field;
- Aerodynamic coefficients from HAWC2/FAST;
- Components: wire, hook, blade, crane, wind field, etc;
- Code-to-code verification.
- Used in NTNU and a few universities

MarIn toolbox has been applied in several scenarios regarding offshore wind turbine installation.

<figure>
  <img src="/research/marin/case1.PNG" alt="{}" style="width:100%" >
  <figcaption>The application to single blade installation </figcaption>
</figure>

<figure>
  <img src="/research/marin/case2.PNG" alt="{}" style="width:100%" >
  <figcaption>The application to OWT preassembly installation using an active heave compensator </figcaption>
</figure>

<figure>
  <img src="/research/marin/case3.PNG" alt="{}" style="width:100%" >
  <figcaption>The application to OWT preassembly installation using an low-height lifting system</figcaption>
</figure>


**Please include the following reference when you use the MarIn toolbox:**

*Zhengru Ren, Zhiyu Jiang, Roger Skjetne, Zhen Gao (2018). Development and application of a simulator for Offshore Wind Turbine Blades Installation. Ocean Engineering, 166:380-395*

If you need these functions right now, please contact with <renzhengru@gmail.com>.




