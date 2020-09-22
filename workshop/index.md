# Software Tools from Atomistics to Phase Diagrams (November 10 and 11, 2020)

## Organizers

Jan Janssen, Tilmann Hickel, Jörg Neugebauer (Max-Planck-Institut für Eisenforschung)<br>
Richard Otis (Materials Genome Foundation)<br>
Brandon Bocklund (Pennsylvania State University)

*Where*: Virtual (Zoom)<br>
*When*: 11 am - 2 pm EST (5 - 8 pm CET / 8 - 11 am PST) on November 10 and 11, 2020<br>
*Application deadline*: **October 2, 2020**<br>
*Registration fee*: No cost for accepted applications

## Overview
CALPHAD (Calculation of Phase Diagrams) is one of the most powerful techniques for Materials Genome and Integrated Computational Materials Engineering (ICME) modeling. While originally based on experimental measurements and extrapolation, the CALPHAD approach has been extended to also include results of atomistic simulation for phases and states which are not experimentally accessible. With the introduction of modern workflow management tools in the atomistic community, it is now possible to use atomistic simulations to facilitate rapid CALPHAD database development. More recently, methods and user tools have been developed that enable automated, reproducible CALPHAD parameter evaluation and uncertainty quantification.

This course will give a detailed introduction to computational thermodynamic software based on atomistic simulations – pyiron – and the CALPHAD method  – pycalphad and ESPEI. This course will feature hands-on demonstrations and practical exercises that will enable attendees to perform atomistic calculations, develop CALPHAD databases with quantified uncertainty, and to propagate uncertainty to any thermodynamic calculation.
 
### [pyiron](https://pyiron.org)

pyiron is an integrated development environment for computational materials science.
[<img class="logo_image" width="100px" src="assets/pyiron-logo.png" alt="pyiron logo">](https://pyiron.org)
Originally developed for ab initio thermodynamics in the department of Joerg Neugebauer at the Max Planck Institut für Eisenforschung, it has recently been published as an open source software package and has been extended to atomistic simulations in general.
In the scope of this workshop pyiron is used to calculate free energies using the quasi harmonic approximation combining specialized codes in one unified interface like LAMMPS for molecular dynamics, phonopy for the calculation of phonons and sqsgenerator to calculate quasi random structures.
 
### [pycalphad](https://pycalphad.org)
pycalphad is a free and open-source Python library for calculating phase diagrams, designing thermodynamic models, and investigating phase equilibria within the CALPHAD method.
[<img class="logo_image" width="100px" src="assets/pycalphad-logo-withtext.png" alt="pycalphad logo">](https://pycalphad.org)
It provides routines for reading thermodynamic databases and solving the multi-component, multi-phase Gibbs energy minimization problem.
All Gibbs energy and property models in pycalphad are described symbolically allowing the models to be customized or overridden by users at runtime without changing any of the pycalphad source code. Calculation results from pycalphad are returned as multidimensional xarray datasets that make it easy to incorporate pycalphad into any tool or workflow.
 
### [ESPEI](https://espei.org)
The Extensible Self-optimizing Phase Equilibria Infrastructure (ESPEI) package is a tool for thermodynamic database development and uncertainty quantification within the CALPHAD method.
[<img class="logo_image" width="200px" src="assets/ESPEI-logo-withtext-200px.png" alt="ESPEI logo">](https://espei.org)
It uses pycalphad for the forward calculation of thermodynamic properties to solve the inverse of parameter evaluation problem. ESPEI uses a two step method to first parameterize thermodynamic models and then optimize and determine the uncertainty of the parameters using Markov Chain Monte Carlo (MCMC).

## How to apply
Interested graduate students, postdoctoral or early-career researchers are encouraged to apply to this interactive workshop by submitting a short motivation for attending the workshop (maximum: one paragraph) and a CV to <link to apply> by **Friday, October 2, 2020**. Attendees are encouraged to introduce themselves during one of the flash poster sessions (maximum: one slide). 

Applications will be reviewed and accepted by **Friday, October 9, 2020**. There is no cost to attend the workshop.

## Agenda
All times are in Eastern Standard Time.
### Day 1 (November 10, 2020)
- 11:00 am Opening
- 11:05 Introduction to pyiron and the quasi-harmonic approximation 
- 11:20 Interactive: Creating atomistic structures with pyiron
- 11:45 Interactive: Atomistic simulations with pyiron
- 12:10pm Break
- 12:20 Interactive: Calculate Phonons and free energies with pyiron
- 12:55 Interactive: From free energies to phase diagrams 
- 1:20 Summary of the first interactive session and discussion
- 1:30 Flash poster session 1
 
### Day 2 (November 11, 2020)
- 11:00 am Opening
- 11:05 Introduction to pycalphad
- 11:15 Interactive: calculating thermodynamic properties with pycalphad
- 11:45 Introduction to ESPEI
- 12:00pm Interactive: ESPEI for CALPHAD database assessment and uncertainty quantification
- 12:30 Break
- 12:40 Interactive: uncertainty propagation with PDUQ
- 1:10 Day 2 summary and discussion
- 1:40 Flash poster session 2
- 1:55 Closing
