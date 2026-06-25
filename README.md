# Cosmological Parameter Constraints with Galaxy Cluster abundances<br>
This repository provides the code and materials supporting the educational report and video content from the CosmoEntity YouTube channel https://youtube.com/@cosmoentity?si=OBPmEBDyVTAd7g5f (In progress).

## Overview
Galaxy clusters are the most massive gravitationally bound structures in the Universe and serve as powerful probes of cosmology. Their abundance and evolution across cosmic time depend sensitively on cosmological parameters, particularly the matter density parameter $\Omega_m$ and the amplitude of matter fluctuations $\sigma_8$.

This project investigates how galaxy cluster number counts can be used to constrain cosmological parameters through a forward-modeling framework. By generating theoretical predictions and comparing them with observations using likelihood analysis, the project explores the degeneracy between $\Omega_m$ and $\sigma_8$ and demonstrates how redshift binning helps break this degeneracy.

In addition, the project studies the impact of observational uncertainties arising from mass proxies, in this project, richness and examines how these uncertainties affect cosmological parameter constraints.

<p align="center">
  <img src="Confidence Contour.png" width="500">
</p>

## Project Scope
The analysis focuses on understanding the relationship between $\Omega_m$ and $\sigma_8$ through galaxy cluster abundance modeling rather than producing state-of-the-art cosmological constraints.

The following simplifications are adopted:

- Simulated data only
- Tinker halo mass function
- Poisson likelihood
- Richness as the cluster mass proxy
- Fixed richness–mass scaling parameters
- focus only two free cosmological parameters ($\Omega_m$ and $\sigma_8$)
- Grid-search parameter exploration

The following effects are not included:

- Survey selection functions
- Halo clustering and sample variance
- Astrophysical baryonic effects
- Systematic uncertainties
- Simultaneous calibration of scaling relation parameters
- Full Bayesian sampling methods (e.g. MCMC)

## Requirements
This project was developed using:
- `pyccl` 
- `numpy`
- `scipy`
- `matplotlib`
The full analysis was tested under:
- `Ubuntu (WSL2)`
- `Python 3.12.3` 

## Getting Started
**⚠️ Important Note for Windows Users:**
`pyccl` relies on C-libraries which can be difficult to build natively on Windows. It is highly recommended to run this project using **Windows Subsystem for Linux (WSL)** or by using a **Conda environment**.

#### Option 1: Using Conda (Recommended)
The most stable way to install PyCCL and its dependencies across different operating systems is via `conda-forge`.

```bash
# Clone the repository
git clone [https://github.com/](https://github.com/)<your-username>/IS-cosmology-galaxy-cluster.git
cd IS-cosmology-galaxy-cluster

# Create the environment
conda env create -f environment.yml

# Activate the environment
conda activate cosmo-cluster
```

#### Option 2: Using pip (Linux / macOS / WSL)
If you are on a UNIX-like system (Linux, macOS, or WSL on Windows), you can install the dependencies directly using pip.

```bash
# Clone the repository
git clone [https://github.com/](https://github.com/)<your-username>/IS-cosmology-galaxy-cluster.git
cd IS-cosmology-galaxy-cluster

# Install requirements
pip install -r requirements.txt
```

### Verifying the Installation

To verify that PyCCL has been installed correctly, run:

```bash
python -c "import pyccl; print(pyccl.__version__)"
```

If the command prints the installed PyCCL version without errors, the installation was successful.

---
