# Probing Quantum Information Scrambling via Local Randomized Measurements
Code and data for the paper "Probing Quantum Information Scrambling via Local Randomized Measurements".

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

This repository contains the numerical simulation code and pre-calculated data to reproduce the results presented in the paper: **"Probing Quantum Information Scrambling via Local Randomized Measurements"** .

In this work, we propose a highly efficient, purity-dependent metric—the Averaged Accessible Information (AAI, $\chi_2$)—extracted via the classical shadow protocol using single-qubit randomized Pauli measurements to probe quantum information scrambling across diverse many-body paradigms.

##  Repository Structure & Reproducibility Map

To facilitate easy reproduction of our results, the code is organized into Jupyter Notebooks, each corresponding to a specific figure in the manuscript. To avoid lengthy simulation times, the raw numerical data generated from the simulations are stored in the `results/` directory and can be loaded directly by the notebooks for plotting.

### 1. Code Files (`.ipynb`)
* `Clifford_circuit.ipynb` : Simulates random Clifford sampling to extract the AAI ($\chi_2$) in the PXP model. (**Reproduces Figure 1**)
* `heat_maps.ipynb` : Generates the spatiotemporal heatmaps comparing standard Holevo information, subentropy, and our AAI across four different many-body systems. (**Reproduces Figure 2**)
* `Classical_shadow.ipynb` : Validates the classical shadow protocol estimations of AAI against exact analytical evolution in MFIM, TFIM, PXP, and MBL models. (**Reproduces Figure 3**)
* `MBL.ipynb` : Simulates the strict dynamical confinement of information within an isolated local cage in the MBL phase. (**Reproduces Figure 4**)

### 2. Data Directory (`results/`)
Contains the pre-calculated data files loaded by the notebooks:
* `AAI_using_Clifford_circuit_data/` (Used by Fig. 1)
* `scrambling_heatmaps_data/` (Used by Fig. 2)
* `dynamics_of_diverse_systems_data/` (Used by Fig. 3)
* `Analysis_of_MBL_system/` (Used by Fig. 4)

---

##  How to Run and Reproduce

### 1. Clone the repository
```bash
git clone https://github.com/ChenYanMing0207/Probing-Quantum-Information-Scrambling-via-Local-Randomized-Measurements.git
cd Probing-Quantum-Information-Scrambling-via-Local-Randomized-Measurements
```  

### 2. Install dependencies
We strongly recommend using a virtual environment (such as conda or venv). Install the required Python packages by running:
```bash
pip install -r requirements.txt
``` 

### 3. Run the Notebooks
Launch Jupyter Notebook or Jupyter Lab:
```bash
jupyter lab
```  

Open any of the .ipynb files and run the cells sequentially (or simply select Kernel -> Restart & Run All).
Each notebook is designed to be self-contained: executing the notebook will run the core numerical simulations (e.g., exact Krylov time evolution or classical shadow sampling) from scratch and directly plot the corresponding figures presented in the manuscript.
(Note: While algorithms are optimized using sparse matrix operations, some simulations—such as the full spatiotemporal heatmaps—may take a few minutes to complete depending on your hardware. Generated figures or intermediate data will be saved to the results/ directory.)

## Citation
If you find this code or our work helpful in your research, please consider citing our paper.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
