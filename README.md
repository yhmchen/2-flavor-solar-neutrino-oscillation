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

```

## Reading Electron Density (Mode 2: BP2000) 

Function: solar_electron_density()

- Density profile from John Bahcall's website (https://www.sns.ias.edu/~jnb/SNdata/sndata.html)

- Reads the standard BP2000 solar model data from a file for each point.

- Converts the read data into electron density values.

- Uses Avogadro's number (N_A) for unit conversion.

- The electron density unit here is cm⁻³.

```python
# Example usage
r_vals, Ne_vals, success = solar_electron_density(filename="BP2000_electron_density.txt", model="BP2000")

```


## PMNS Matrix and Hamiltonian

The PMNS rotation matrix:

$$
U = 
\begin{bmatrix}
\cos \theta & \sin \theta \\
-\sin \theta & \cos \theta
\end{bmatrix}
$$

The total Hamiltonian is:

$$
H_\text{total} = U \cdot H_\text{vac} \cdot U^\dagger + V_e
$$

where the vacuum Hamiltonian is:

$$
H_\text{vac} =
\begin{bmatrix}
0 & 0 \\
0 & \frac{\Delta m_{21}^2}{2E}
\end{bmatrix}
$$

and the electron potential is:

$$
V_e =
\begin{bmatrix}
\sqrt{2} G_F N_e & 0 \\
0 & 0
\end{bmatrix}
$$

with

$$
\Delta m_{21}^2 = m_2^2 - m_1^2
$$







