# Functional Depth Methods — Code & Performance Tests

This repository contains the implementation and performance evaluation of several **functional depth methods**. Functional depth is a statistical concept used to measure how “central” or “outlying” a function is within a set of functions. It provides a way to order functional data from the most typical (deepest) to the most unusual (shallowest), enabling tasks such as **outlier detection** and **robust estimation**.

## Methods Included
- **BD** — Band Depth  
- **WBD** — Weighted Band Depth based on shape distance of original functional data
- **MBD** — Modified Band Depth  
- **WMBD** — Weighted Modified Band Depth based on shape distance of original functional data  
- **FUNTA**  - Functional Tangent Angle Pseudo-Depth
- **rFUNTA**  - Robust Functional Tangent Angle Pseudo-Depth
- **WBD (1st Order Derivative)** — Weighted Band Depth based on shape distance of first-order derivative of functional data
- **WMBD (1st Order Derivative)** — Weighted Modified Band Depth based on shape distance of first-order derivative of functional data

## Experiments
1. **Outlier Detection**
   - 15 simulated model datasets  
   - 2 real-world datasets  

2. **Robust Mean Estimation**
   - 6 simulated model datasets  

## Usage
The `test` folder contains MATLAB scripts representing different test cases.  
Each `.m` file under `test/` corresponds to one test case, which may use:
- **Simulated data** generated within the test case  
- **Real-world data** loaded from the `data/` folder (if required)  

All tests are executed using **MATLAB R2018b**.  
After each run, results are stored in the variable `whole_result` for further inspection.

**Special Note:**  
In **Outlier Detection Model 15**, the test reads simulated data from two files:
- `Y_out_situation2.txt` — Outlier curves  
- `Y_nor_situation2.txt` — Normal curves  

These datasets were generated following the parameters specified in:  
> Kuhnt, S., & Rehage, A. (2016). *An angle-based multivariate functional pseudo-depth for shape outlier detection*. Journal of Multivariate Analysis, 146, 325–340.
You can download the generated data files from [this folder](https://drive.google.com/drive/folders/1ejKdfcdb1HbNSCe9rpPAiWkkUcqqPjSX?usp=share_link) on Google drive.

## Repository Structure
```plaintext
├── data/                          # Simulated and real-world datasets
├── src/                           # Source code for functional depth methods
├── test/
│   ├── outlier_detection/         # Scripts for outlier detection experiments
│   └── robust_mean_estimation/    # Scripts for robust mean estimation experiments
├── .gitignore
└── README.md
```

## License
This project is licensed under the [MIT License](LICENSE).
