# photon-noise-condensation

Code for: "Complete condensation of photon noise in nonlinear dissipative systems" by Nicholas Rivera, Jamison Sloan, Yannick Salamin, and Marin Soljacic

Contains code used to numerically validate the transient noise condensation and Fock lasing effects, as well as code to calculate statistics of Fock lasers using quantum Langevin methods.

This repository consists of three Jupyter notebooks (using Julia 1.1).

1. "Transient noise condensation.ipynb" - Performs time-evolution of master equation of 2 modes (a,d) with nonlinearity. Produces Fig. S1 of the manuscript and validates Eqs. (2-4) of the main text.

This notebook is the most resource-intensive. On my laptop, the time-evolution of the Lindblad operator took just under two hours. We have included pre-calculated data that you may load in the appropriate cell of the notebook - if you just want to see and play with the data of Fig. S1.

2. "Fock lasing in systems with sharply nonlinear loss.ipynb" - Calculates steady states of the Liouvillian of pumped two- and four-level systems (representing the gain medium) with the 2-nonlinear-modes system of Notebook (1). This shows that a pumped gain medium interacting with this nonlinear loss indeed supports extremely low-noise (heavily squeezed) states of optical radiation. This notebook produces plots for Fig. S2 of the SI and also shows how the concept extends to producing near-Fock states of up to 500 photons.

This notebook runs much quicker than (1) but will still take time to run to completion, due to large steady-state calculations, as well as a parameter-sweep.

3. "Macroscopic Fock laser statistics from quantum Langevin.ipynb" - Calculates quantum statistics of four-level gain media interacting with a resonator with nonlinear loss using the quantum Langevin approach (mean-field + linearization). Does so for an example of a solid-state gain medium coupled to a macroscopic (mm-scale) open-resonator cavity (produces plots related to Fig. 4 of the main text). 

This notebook should run almost instantly.


