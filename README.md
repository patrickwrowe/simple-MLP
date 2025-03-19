# Supplementary Data for "Machine Learning Potentials for Complex Aqueous Systems Made Simple"

This repository contains supplementary data supporting the findings of the paper:

*"Machine Learning Potentials for Complex Aqueous Systems Made Simple"*  
Christoph Schran, Fabian L. Thiemann, Patrick Rowe, Erich A. Müller, Ondrej Marsalek, and Angelos Michaelides

## License

The content of this repository is licensed under the CC-BY-SA-4.0 license. See the file `LICENSE` for details.

## Contents

- **`models/`**:  
  Contains all parameters of the C-NNP models for the six aqueous systems studied.

- **`training-sets/`**:  
  Includes all training sets of the C-NNP models for the six aqueous systems studied.

## Scientific Background

The C-NNP models leverage neural network potentials to approximate the potential energy surface of complex aqueous systems. These models are trained on density functional theory (DFT) data, ensuring high fidelity to quantum mechanical calculations while being computationally efficient. The systems studied include:

- **BNNT-water**: Boron nitride nanotube interactions with water.
- **CNT-water**: Carbon nanotube interactions with water.
- **Fluoride-water**: Fluoride ion solvation in water.
- **MoS₂-water**: Molybdenum disulfide interactions with water.
- **SO₄-water**: Sulfate ion solvation in water.
- **TiO₂-water**: Titanium dioxide interactions with water.

These potentials are specifically designed for use within the [CP2K](https://www.cp2k.org/) simulation software.

## Using the Potentials in CP2K

To use the provided potentials in CP2K:

1. **Select the Model**:  
   Choose the appropriate model from the `models/` directory based on your system of interest (e.g., `bnnt-h2o` for boron nitride nanotube-water interactions).

2. **Prepare the Input File**:  
   Include the model parameters in your CP2K input file. Documentation for this can be found at https://manual.cp2k.org/trunk/CP2K_INPUT/FORCE_EVAL/NNP.html

Validation:
Before running large-scale simulations, validate the potential by comparing its predictions (e.g., energies, forces, and structural properties) against experimental or ab initio reference data.

Fine-Tuning (Optional):
If needed, use the training sets in training-sets to retrain or fine-tune the models for specific applications. This requires a compatible machine learning framework.

References
For further details on the methodology, training process, and validation of these potentials, please refer to the original paper:

"Machine Learning Potentials for Complex Aqueous Systems Made Simple"
Christoph Schran, Fabian L. Thiemann, Patrick Rowe, Erich A. Müller, Ondrej Marsalek, and Angelos Michaelides