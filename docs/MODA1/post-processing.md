---
layout: page
title: 4 Post processing
nav_order: 40
description: 4 Post processing
permalink: /MODA1/post-processing/
parent: MODA1
has_references: true

annotater:

---

# MODA for Calculations of Binding Free Energies and Potentials of Mean Force
Simulated in project SMARTNANOTOX

1. __Post processing:__
    1. __The processed output is calculated for:__<br>
        The raw output is positions of atoms at each trajectory step (Gromacs .xtc or .trr trajectory), value of the collective variable, Gaussian height, force on the collective variable and bias potential (COLVAR , FORCES and HILLS files of Metadynamics). The processed output is the potential of mean force and binding free energy
    2. __Methodologies:__<br>
        Potential of mean force _w_(_s_) is computed by averaging of average force at the given distance of the solute from the surface (_s_):<br>
        _w_(_s_)=-∫<sub>_s_</sub><sup>_s_<sub>bulk</sub></sup>_F_(_s_)_ds_<br>
        where _s_<sub>_bulk_</sub> = 1.2 nm is the distance corresponding to bulk solvent where PMF value is accepted to be zero.<br><br>
        The binding free energy is computed by<br>
        _ΔG_<sub>_bind_</sub> = -_k_<sub>_B_</sub>_T_ ln(1/_δ_ ∫<sub>0</sub><sup>_δ_</sup> _dse_<sup>-_w_(_s_)/(_k_<sub>_B_</sub>_T_)</sup>,<br>
        where _δ_ is the adsorption layer thickness.
    3. __Margin of error:__
        2 kJ/mol
{: .large-list .start4 }
