# Cosmological Parameters, Predictions, and Dark Matter: A Dive into Halo Mass Function Analytics
Welcome to my summer research project at Canadian Institute for Theoretical Astrophysics (CITA) at University of Toronto. This project is about classifying and eliminating dark matter candidates based on observables including halo mass function and power spectrum. This repository provides a collection of Python notebooks that dive deep into analytics of the halo mass function with an emphasis on the effects of various cosmological parameters and performing analytical fits.
## Notebooks:
### power_spectrum.ipynb

This notebook focuses on the generation of power spectrums, illustrating the effects of varying cosmological parameters on these spectrums. 

**Key Highlights:**
- Demonstration of how different cosmological parameters influence the power spectrums.
  
**Generating GIFs:**

To visualize how the power spectrum evolves with specific parameter variations, utilize the following functions:

- **Angular Power Spectrum:**
  - `generate_gif()`: Produces a GIF highlighting changes with a single parameter variation.
  - `generate_gif_two_param()`: Produces a GIF showcasing changes with two-parameter variations.

- **Matter Power Spectrum:**
  - `generate_gif_matter_spectrum()`: Generates a GIF for matter spectrum changes with a single parameter variation.
  - `generate_gif_matter_spectrum_two_param()`: Creates a GIF illustrating matter spectrum changes with two-parameter variations.


### transfer_to_hmf.ipynb

This notebook offers a comprehensive guide on deriving the transfer function using CLASS and subsequently inputting it into `halomod` to generate the halo mass function.

**Key Features and Functions:**

- **Parameter Setup and Integration with CLASS and halomod:**
  - `run_class()`: Function to obtain the transfer function from CLASS.
  - `generate_halo_model()`: Function to input the transfer function into `halomod` and subsequently generate the halo mass function. This function sets up the necessary parameters in CLASS and seamlessly integrates them into `halomod`.

- **GIF Generation for Halo Mass Function:**
  To visualize the variations in the halo mass function based on different parameter adjustments (sourced from the transfer function in CLASS), utilize the following functions:
  - `generate_gif()`: Produces a GIF showcasing changes in the halo mass function with two-parameter variations.
  - `generate_gif_one()`: Generates a GIF illustrating the halo mass function alterations with a single parameter variation.

Use this notebook to understand the intricate relationship between CLASS-generated transfer functions and the halo mass function as visualized in `halomod`, and to visualize the influence of parameter variations on the halo mass function.

### hmf_thermal_relic.ipynb

This notebook offers an in-depth exploration of the thermal relic warm dark matter model by producing halo mass functions across varying warm dark matter masses.

**Key Features and Functions:**

- **Halo Mass Function Generator:**
  - `generate_halo_mass_function(m_ncdm_keV_values)`: 
    - **Parameters**: A list of warm dark matter masses in keV, e.g., `[0.7, 1.3, 1.7]`.
    - **Output**: A visualization saved as "dndm_top.pdf", illustrating halo mass functions for the provided warm dark matter masses.
    - **Description**: Utilizing the provided warm dark matter masses, the function calculates and displays the halo mass function for each mass, making it easy to observe and compare variations.

Utilize this notebook to gain insights into the behavior of the halo mass function under the influence of different warm dark matter masses in the context of the thermal relic model.


### hmf_sigma8.ipynb

This notebook delves into the intricate relationships of various cosmological parameters, with a particular focus on the influence of \( \sigma_8 \) on the halo mass function and transfer function. It offers insights into the effects of several parameters on the halo mass function. **Notably, in this approach, parameters are inputted directly into halomod, bypassing CLASS, providing a more direct examination.**

**Key Features and Functions:**

- **Direct Parameter Input into halomod**:
  - This approach allows for an efficient investigation by sidestepping the CLASS integration, offering a unique perspective on parameter effects.

- **Effect of \( \sigma_8 \) on Halo Mass Function and Transfer Function**:
  - `generate_gif_sigma8(base_params, sigma8_values)`:
    - **Purpose**: Demonstrates the effect of different \( \sigma_8 \) values on the halo mass function by producing a gif.
    
- **Influence of Various Parameters on Halo Mass Function**:
  - `generate_gif_ns(base_params, ns_values)`:
    - **Purpose**: Illustrates the impact of spectral index (n_s) values on the halo mass function via gif generation.

  - `plot_transfer_function_direct(base_params, param_name, param_values, ylim1, ylim2, kmax=1.0, z_pk=0.0)`:
    - **Purpose**: Visually represents how varying values of a parameter can alter the transfer function.
    
  - `generate_gif_omega_cdm(base_params, omega_cdm_values, h_values)`:
    - **Purpose**: Offers a visualization of how changing \( \Omega_{cdm} \) and the Hubble parameter affect the halo mass function, presenting the results as a gif.
    
  - `generate_gif_omega_b(base_params, omega_b_values)`:
    - **Purpose**: Depicts the influence of varying \( \Omega_b \) on the halo mass function, saving the visualizations in gif format.

Leverage this notebook to gain a comprehensive understanding of the intertwining relationships between \( \sigma_8 \), other cosmological parameters, and their respective impacts on the halo mass function and transfer function, while appreciating the efficiency of direct halomod parameter input.

### hmf_fitting.ipynb

This notebook is uniquely tailored to explore the world of dark matter through the lens of fitting techniques. By employing an arctan-based fitting approach, we strive to capture the intricacies of the halo mass function (HMF) for various dark matter models.

**Models Covered:**
- **Cold Dark Matter (CDM) Model**.
- **Thermal Relic Warm Dark Matter Model**.
- **Mixed Dark Matter Model**.

**Key Features and Functions:**
- **Arctan-Based Fitting Technique**:
  - Utilized to fit the halo mass functions of different dark matter models.
  - Employs the function `fitting_hmf_mixed`, capturing the complexity of HMFs by merging a linear term with two arctangent terms. 
  - Examples provided for each dark matter model to illustrate the efficacy and nuances of the fitting process.

Dive into this notebook for a compelling journey into the realm of dark matter, understanding its varied models and appreciating the fitting techniques that help capture their essence.

## Dependencies:
To run the notebooks, ensure you have the following Python packages installed:
1. matplotlib
2. numpy
3. os
4. scipy
5. imageio
6. astropy
7. halomod
8. hmf
9. classy
## Usage:
1. Clone the repository.
2. Ensure you have all the dependencies installed.
3. Navigate to the directory and run the desired notebook.
