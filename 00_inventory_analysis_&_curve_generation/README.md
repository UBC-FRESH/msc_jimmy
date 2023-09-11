
# Yield Curve Generation Project

---

Welcome to the Yield Curve Generation Project repository! This project utilizes a collection of Jupyter notebooks, each meticulously designed to provide step-by-step guidance on different stages of the yield curve generation process. By following the series, users will be equipped with a systematic understanding, ensuring clarity and precision throughout the journey.

---

## 🌲 Background 

This is the preparation repository for the forest estate modeling. Existing LCA biogenic carbon studies only used the stand-level simulation for timber supply simulation. However, the stand-level simulation faced the start-point problem when you have to consider the initial age in the existing forest. 

The point of origin for the simulation—whether from harvesting or planting—can significantly influence emission results. For instance:
- Starting the simulation from harvesting makes the model start from immediate emissions.
- Starting from planting centers on carbon sequestration. 

Consequently, simulations that begin with planting suggest a positive climate impact for the products, while those starting from harvesting indicate the opposite.

To address this, we adopted the forest landscape-level simulation model - the forest estate model. This optimization model balances the forest timber supply and forest growing stock retention. In simple terms, if we harvest all the volume growing during a coming year, we achieve timber supply while the forest tree carbon pool remains intact. The model not only finds the growing volume but also offers the flexibility to explore other harvest scenarios. The forest estate model aggregates all the stand-level simulations in the area and considers them holistically. 

For the forest estate model, we need the forest's initial inventory and the stand-level growth and yield curve. We analyzed the forest inventory with geopandas to determine similar stands in the forest and later aggregate them. The analyzed representative stands information will be used to find the yield curve from the government forest growth model. This will then be the input for the forest estate model. 

---

## 📊 Overview

This repository houses a collection of scripts and notebooks tailored for the preparation, analysis, and conversion of forest estate modeling data.

### Contents:

1. **00_data-prep.ipynb**:
   - **Purpose**: Main entry point for data preparation. Processes and prepares datasets for subsequent steps.
   - **Details**:
     - Originally designed by Gregory Paradis. Fine-tuned by Jimmy Ke.
     - Prepares datasets for landscape-level forest estate modeling in BC.
     - Imports vegetation resource inventory datasets.
     - Extracts study area dataset.
     - Stratifies features for harvesting and carbon analyses.
     - Constructs VDYP and TIPSY yield curves.

2. **01a_run-tsa.ipynb**:
   - **Purpose**: Focuses on compiling and preparing strata and yield curves.
   - **Details**:
     - Compiles strata and divides each into three AUs based on SI quantile ranges.
     - Runs the VDYP application and amalgamates its outputs into yield curves.
     - Generates files for the TIPSY application (manual run required on Windows).

3. **01b_run-tsa.ipynb**:
   - **Purpose**: Post-processes TIPSY outputs.
   - **Details**:
     - Cleans TIPSY outputs.
     - Streamlines column names and other details.
     - Handles multiple TSA output files.

4. **03_yield_curve_convert.ipynb**:
   - **Purpose**: Converter tool for TIPSY outputs.
   - **Details**:
     - Creates wood allocation curves.
     - Processes fertilized yield curves for further analysis.

### Dependencies:

- `numpy`: Numerical computations.
- `pandas`: Data manipulation and analysis.
- `geopandas`: Geoinformation analysis.

### 🚀 Getting Started:

1. **Setup**:
   - Install dependencies: `pip install numpy pandas`
   - Download required datasets and adjust paths in `00_data-prep.ipynb` as needed.

2. **Execution**:
   - Begin with `00_data-prep.ipynb`.
   - Follow the order of script/notebook prefix numbers.
   - For `01a_run-tsa.ipynb`, run TIPSY manually on a Windows machine post data generation.

3. **Output**:
   - Processed data is ready for further tasks post script execution.

---

Happy Modeling! 🌳📈
