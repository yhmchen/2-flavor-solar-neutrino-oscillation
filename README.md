# 2-flavor-solar-neutrino-oscillation
This Python code calculates and visualizes the flavor evolution of solar neutrinos  as they travel from the Sun to Earth.  It uses a 2-flavor neutrino model with vacuum and matter effects, based on the BP2000  solar electron density model.


Main Features:
- Compute the neutrino Hamiltonian including vacuum oscillations and matter potential.
- Solve the Schrödinger equation for neutrino flavor evolution.
- Calculate flavor probabilities P(ν_e) and P(ν_μ) at user-specified distances.
- Plot the survival and transition probabilities versus distance.

Usage:
- Adjust the neutrino energy (E_nu) and evaluation points (r_eval) as needed.
- Ensure the BP2000 electron density model file is available.
- Run the script to obtain probability curves and visualize the results.
"""

# Solar Electron Density

## Reading Electron Density (Mode 1: Custom Model)

Function: custom_density_function()

- You can define your own electron density model as needed.
- You can generate evenly spaced points from the solar center to the solar surface.

```python
# Example usage
r_vals, Ne_vals, success = solar_electron_density(model="custom")

Function: custom_density_function()

Reads the standard BP2000 solar model data from a file for each point.

Converts the read data into electron density values.

Uses Avogadro's number (N_A) for unit conversion.

The electron density unit here is cm⁻³.```

## Reading Electron Density (Mode 2: BP2000)

# Example usage
```python
# Example usage
r_vals, Ne_vals, success = solar_electron_density(filename="BP2000_electron_density.txt", model="BP2000")

Function: solar_electron_density()

It will use the electron density from BP2000.txt'''






