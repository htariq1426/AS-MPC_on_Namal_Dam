# Ensemble Generation

## Overview
This subfolder contains scripts and data used for generating ensemble precipitation datasets from ERA5 reanalysis data. These datasets are then used as inputs for the SWAT model to generate corresponding hydrological outputs.

## Requirements
- **Programming Language:** Python 3
- **Data Source:** ERA5 reanalysis dataset
- **Main Scripts:**
  - `Ensemble_extractor_ERA5.ipynb` – Extracts and processes ERA5 ensemble precipitation data.
  - `ENF.ipynb` – Processes ensemble outputs into a structured dataframe.

## Installing Required Python Packages
To ensure all required dependencies are installed, run the following command in your Python environment:
```bash
pip install pandas numpy xarray netCDF4 matplotlib
```

## Data Processing Workflow
1. **Ensemble Data Extraction:**
   - `Ensemble_extractor_ERA5.ipynb` extracts ensemble precipitation data from ERA5 sources.
   - Outputs are stored in `.csv` and `.grib` formats, e.g., `1992_ensemble_pcp_sep.csv`, `1992_ensemble_pcp_jul_aug.grib`.
2. **Hydrological Model Runs:**
   - The generated precipitation datasets are used to run SWAT simulations for multiple ensemble members (`1a.csv`, `2a.csv`, ..., `10a.csv`).
3. **Dataframe Processing:**
   - `ENF.ipynb` processes the SWAT model outputs into a structured dataframe (`ENF_1.csv`, `ENF_2.csv`, ..., `ENF_10.csv`).
4. **Visualization:**
   - Various ensemble analysis plots (`Ensemble Member.jpg`, `Ensemble Streamflows Namal Sept-1992.jpg`) are generated to assess uncertainty and spread.

## Running the Scripts
1. Ensure you have Python 3 installed with the required dependencies.
2. Run `Ensemble_extractor_ERA5.ipynb` to extract ensemble precipitation data.
3. Use the generated precipitation data as input to the SWAT model using the files from the data from [Zenodo Repository](https://zenodo.org/records/14909725).
4. Run `ENF.ipynb` to process SWAT outputs into a structured dataframe.
5. Use visualization scripts to analyze ensemble spread and trends.

## Contact
For any questions or collaborations, please reach out to the repository owner.

---
This README provides clear documentation on the structure, requirements, and purpose of the `Ensemble Generation` subfolder.

