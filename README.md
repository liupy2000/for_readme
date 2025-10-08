# Latent Tensor Gaussian Process

This repository contains the implementation and performance evaluation of several methods for **spatial profile analysis**. 
It provides reproducible MATLAB scripts to replicate the numerical experiments and case studies reported in the paper **"Spatial In-Profile Monitoring via Latent Tensor Gaussian Process with Mixed Effects"**.

## Methods Included
The repository implements and benchmarks the following models:
- **LTGP-ME** — Latent Tensor Gaussian Process with Mixed Effects  
- **TME** — Tensor Mixed Effects Model  
- **TR** — Tensor Regression  
- **VPCR** — Vectorized PCA Regression  


## Usage
Each of the top three folders (`1 case/`, `2 Setting1/`, `3 Setting2/`) contains a main MATLAB script corresponding to one experiment setup.

Inside each folder:
- `main_case.m` — reproduces **Figure 10** (real-world case)  
- `main_setting1.m` — reproduces **Figures 4(a)** and **5(a)** (Setting I)  
- `main_setting2.m` — reproduces **Figures 4(b)** and **5(b)** (Setting II)

All tests are executed using **MATLAB R2023b**.  


## Repository Structure
```plaintext
├── 1 case/                        # Real-world case study
│   ├── baselines/                    # Source code for TME, TR, and VPCR
│   ├── LTGP/                         # Source code for LTGP-ME
│   ├── data.mat                      # Source data from the additive manufacturing
│   └── main_case.m                   # Main script
├── 2 Setting1/                    # Numerical study-Setting (I)
│   ├── baselines/                    # Source code for TME, TR, and VPCR
│   ├── LTGP/                         # Source code for LTGP-ME
│   └── main_setting1.m               # Main script
├── 3 Setting2/                    # Numerical study-Setting (II)
│   ├── baselines/                    # Source code for TME, TR, and VPCR
│   ├── LTGP/                         # Source code for LTGP-ME
│   └── main_setting2.m               # Main script
├── bspline/                       # Packages for functional data analysis
├── tensor_toolbox-c3.5/           # Packages for tensor data analysis
├── utilities/                     # General helper functions and reusable utilities
└── README.md
```

## License
This project is licensed under the [MIT License](LICENSE).
