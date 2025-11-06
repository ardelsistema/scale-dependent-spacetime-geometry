# Scale-Dependent Spacetime Geometry

This repository contains the LaTeX source and Python toolkit for the paper

> **“Scale-Dependent Spacetime Geometry:  
> An Effective Field Theory Framework for Quantum-Gravity Tests Across Multiple Scales”**

**Author:**  
**Facundo Firmenich**  
Centro de Estudios del Sur (CEDESUR) — Buenos Aires / Barcelona  
ORCID: [0009-0002-6578-3811](https://orcid.org/0009-0002-6578-3811)  
Email: <f.firmenich@cedesur.org>  

**Co-authors:**  
- **Pau Firmenich**  
- **León Firmenich**  

Pau Firmenich and León Firmenich are co-authors of this work and also the sons of the main author. Their collaboration has been essential for the primary conceptualization, exhaustive cross-checking, intermediate validation and final consistency checks, as well as for the continuous creative input and refinement at all stages of the project.

---

## Overview

The project develops an effective field theory (EFT)–motivated framework to investigate **scale-dependent spacetime geometries** in static, spherically symmetric configurations, with direct applications to:

- Solar-system tests (perihelion precession, light deflection, Shapiro delay)
- Binary systems and strong-field regimes (conceptual connection to ppE)
- Simple Gaia-like astrometric forecasts for Yukawa-type deviations
- Energy-condition analysis for phenomenological ansätze

The focus is on **Yukawa-type modifications** to the Newtonian potential and on how to connect them to existing Parameterized Post-Newtonian (PPN) and parameterized post-Einsteinian (ppE) frameworks, within a consistent EFT picture.

The repository provides:

- The full LaTeX manuscript (`paper.tex`)
- A Python toolkit (`yukawa_toolkit.py`) implementing the Yukawa phenomenology and generating key figures
- Pre-generated figures:
  - `yukawa_constraints.pdf` — schematic combined constraints in the Yukawa parameter space  
  - `rho_eff_yukawa.pdf` — illustrative effective energy-density ratios for different Yukawa couplings

---

## Repository Contents

- `paper.tex`  
  Complete LaTeX source of the paper, including:
  - Metric ansätze and EFT motivation  
  - PPN / ppE mapping  
  - Multi-probe observational discussion  
  - Energy-condition analysis  
  - References (single-file setup, suitable for arXiv, GitHub, Zenodo)

- `yukawa_toolkit.py`  
  Python 3 script that provides:
  - Yukawa potential: `phi_yukawa(r, M, params)`
  - Perihelion precession correction: `perihelion_precession_yukawa(...)`
  - Light deflection: `deflection_angle_yukawa(...)`
  - Effective energy density (Poisson-like approximation): `rho_eff_yukawa_r(...)`
  - Validation tests  
  - Automatic generation of:
    - `yukawa_constraints.pdf`
    - `rho_eff_yukawa.pdf`

- `yukawa_constraints.pdf`  
  Log–log plot of schematic combined constraints on Yukawa parameters \((\lambda_Y, \alpha_Y)\), showing approximate regions associated with:
  - Cassini γ bound  
  - Mercury perihelion precession  
  - Torsion-balance experiments  
  - A Gaia-like forecast

- `rho_eff_yukawa.pdf`  
  Plot of the ratio \(\rho_{\mathrm{eff}}(r) / \rho_{\mathrm{GR}}(r)\) as a function of radius, for different values of \(\alpha_Y\), illustrating how the effective energy density responds to Yukawa-type deviations in the weak-field regime.

---

## Requirements

To run the Python toolkit you need:

- **Python 3.8+**  
- The following Python packages:
  - `numpy`
  - `scipy`
  - `matplotlib`

You can install them (for example) with:

```bash
pip install numpy scipy matplotlib
