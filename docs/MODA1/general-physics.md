---
layout: page
title: 2 General physics
nav_order: 20
description: 2 General physics of the model equations
permalink: /MODA1/general-physics/
parent: MODA1
has_references: true

annotater:

---

# MODA for Calculations of Binding Free Energies and Potentials of Mean Force
Simulated in project SMARTNANOTOX

1. __General physics of the model equations:__
    1. __Model type and name:__<br>
        Molecular dynamics with self-adjusted bias (Metadynamics)
    2. __Model entity:__<br>
       Atoms
    3. __Model physics / chemictry equations PE's:__
        1. __Equations:__<br>
            pe_type_atomistic_molecular_dynamics<br>
            Newtons equation of motion<br>
            V-rescale thermostat<br>
            Bias potential for the surface separation distance, which is determined according to the well-tempered metadynamics equations<br>
            The PMF is computed by integration of the average force acting on the solvent at the given distance from the surface<br>
        2. __Physical quantities for each equation:__<br>
            atoms coordinates; atom velocities; biased potential
    {: .sub-start0 }
    4. __Materials relations:__
        1. __MR equations:__<br>
            Material is described by a user-specified force field<br>
            Biomolecules are described by the GAFF<br>
            Water is described by the TIP3P model
        2. __Physical quantities / descriptors for each MR:__<br>
            atoms coordinates; atom velocities; biased potential
    5. __Simulation input:__<br>
        N/A
    6. __Publication:__<br>
        G.A. Tribello, M. Bonomi, D. Branduardi, C. Camilloni, G. Bussi. PLUMED2: New feathers for an old bird, Comp. Phys. Comm. 185, 604 (2014), [doi:xxx]
{: .large-list .start2 }
