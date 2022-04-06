---
layout: page
title: 3 Modelling metadata
nav_order: 130
description: 3 Specific computational modelling metadata
permalink: /MODA1/modelling-metadata/
parent: MODA1
has_references: true

annotater:

---

# MODA for Calculations of Binding Free Energies and Potentials of Mean Force
Simulated in project SMARTNANOTOX

1. __Specific computational modelling metadata:__
    1. __Numercial solver:__<br>
        Verlet algorithm with V-rescale thermostat<br>
        Metadynamics algorithm with collective variable determined as the surface separation distance between the sorbent molecule and surface
    2. __Software tool:__<br>
        Gromacs 2018 with Plumed 2.5
    3. __Time steps:__
        2 fs, total simulation time ~500 ns
    4. __Computational representation:__
        1. __Physics equation, material relations, material:__<br>
            Newton’s equations are discretized in a Verlet scheme. Forces are computed by summation over all atom pairs within the cut-off radius. Long-range electrostatic interactions are treated by the Particle Mesh Ewald (PME)<br>
            Metadynamics with adaptive Gaussians width
    5. __Computational boundary conditions:__<br>
        Material slab periodic in X and Y direction. Sorbent molecule located outside the slab. Water filling the rest of the simulation box. The whole system is 3D periodic
    6. __Additional solver parameters:__<br>
        thermostat relaxation time:  1 ps<br>
        real space cutoff:  1 nm<br>
        PME grip spacing:  0.1 nm<br>
        preequilibration time:  2 ns<br>
        fixed height of Gaussians:  0.001 kJ/mol<br>
        Additional potential wall for the sorbent at large distance from the surface:<br>
        _U<sub>wall</sub>(_s_)=_k_(_s_-_a_)<sup>4</sup><br>
        with the force constant _k_ = 40 kJ/(mol Å<sup>4</sup>) and _a_ = 1.5 nm.
    7. __Publication:__<br>
        E. G. Brandt and A. P. Lyubartsev "Molecular Dynamics Simulations of Adsorption of Amino Acid Side Chain Analogues and a Titanium Binding Peptide on the TiO2 (100) Surface" J. Phys. Chem. C, 119(32), 18126-18139 (2015) [DOI:10.1021/acs.jpcc.5b02670](https://doi.org/10.1021/acs.jpcc.5b02670)
{: .large-list .start3 }
