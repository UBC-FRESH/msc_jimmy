
# Forest Estate Carbon Budget Model

This repository contains tools and notebooks for simulating and analyzing forest estate carbon emissions and sequestration.

## Contents:
1. `model_input.ipynb` - **Woodstock-style Input Compilation**
2. `model_run_seq_CBM.ipynb` - **Running the Carbon Budget Model with SIT Inputs**

---

## 1. Woodstock-style Input Compilation (`model_input.ipynb`)

### Overview:
This notebook is tailored to compile Woodstock-style input data for the `ws3` model. It primarily focuses on the stratification schema, initial inventory, yield curves, treatments, and transitions.

### Key Features:
- **Forest Estate Model Input File Generation**: Produces input files for a forest estate model. These encompass:
  - Landscape file
  - Area file
  - Growth and yield file
  - Forest action file
  - Transition rule file

- **Transition Rule File Creation**: Constructs a transition rule file, considering various fertilization options and their respective actions.

---

## 2. Running the Carbon Budget Model with SIT Inputs (`model_run_seq_CBM.ipynb`)

### Overview:
This notebook is centered around executing a forest estate model, seamlessly integrating with the Carbon Budget Model (CBM) using the Standard Import Tool (SIT) input data.

### Introduction to Forest Estate Model:
The primary objective of this notebook is to set up, run, and analyze a forest estate management model. This model is instrumental in guiding decisions on forest management, encompassing activities like harvesting, fertilization, and other interventions.

### Introduction to Forest Ecosystem Carbon Model:
The forest ecosystem carbon will react associated with the forest managements. Thus, we simulate the forest ecosystem carbon pool and emission from the carbon pool identicially with the forest management options. 


### Key Components:
1. **Setup**:
   - Initialization and updates of Git submodules.
   - Installation and loading of the `memory_profiler` extension for memory usage profiling.
   - Addition of a local submodule named `ws3` to the path.
   - Loading the `autoreload` extension for dynamic module reloading during development.

2. **Preliminary Definitions**:
   - Model parameters are defined, such as input data path, period length, max age, base year, horizon, and model name.

3. **Model Initialization**:
   - Creation of the `ForestModel` instance from the `ws3.forest` module.
   - Integration of landscape, areas, yields, actions, and transitions into the model.

4. **Action Configuration**:
   - Addition of a "null" action and flagging a specific action as a harvest action.

5. **Objective and Constraint Compilation**:
   - Definition of functions to compile model components, which include objective function coefficients and various constraints.

6. **Scenario Analysis**:
   - Compilation of scenario outputs into dataframes and visualization of results.

7. **CBM Model Buidling**:
    - Build CBM model with the forest operations

8. **Emission Analysis**:
    - The carbon sequestration and ecosytem carbon dynamic has been tracked along the way
    
9. **Harvested Wood Products Tracking**:
    - The volume of harvested wood products will be tracked for the following emission simulation

