# UCSF Dyslexia Center - Data Ecosystem

## Overview

### Raw Data:

Sources of data include Structural MRI, Diffusion MRI, Functional MRI, and Behavioral Data.
Data is stored in various databases and structures such as BIDS, REDCap, LAVA, and MAC Imaging-Core.

### Pre-processing:

Data undergoes pre-processing using tools on the Wynton HPC. The tools used include sMRIprep for structural MRI, QSIprep for diffusion MRI, and fMRIprep for functional MRI.

### Post-processing:

Further data refinement is done on both the local machine and Wynton HPC. This includes generating statistical files using Bash scripts, contrasts using Python scripts, and fetching REDCap data using an API.

### Data Standardization:

Data is standardized and stored in specific formats like FreeSurfer metrics, interactive tractography, and CSV files.

### Data Analysis:

Advanced analysis, including machine learning predictions and group comparisons, are done using Wynton HPC & Local Machine.
Encoding/Decoding models using tools like nilearn and nibabel are applied.

### Ucsfneuroviz Browser:

This browser allows visualization of the Structural MRI, Diffusion MRI, Functional MRI, and Behavioral scores.

### Supporting Tools:

Python: Used for scripting, generating Jupyter notebooks, and handling data.
Voilà: Converts Jupyter notebooks into interactive dashboards.
Binder: Allows for sharing of data via Git, making the entire process reproducible without requiring local machine setup.

## Pros of this Approach

### 1. Flexibility
The ecosystem is designed to easily accommodate various data types and sources.

### 2. Modularity
Each step in the process is clearly defined, allowing for individual modules to be updated or replaced without disrupting the entire system.

### 3. Robustness
With the use of established tools and databases, the pipeline ensures reliability and accuracy in data processing and analysis.

### 4. Readiness for Multimodal & Multicenter Data
The structure is ready to handle diverse data types from various centers, ensuring a wide range of applicability.

### 5. Preparation for Data Sharing
With the use of BIDS format, the system is already aligned with standards for data sharing in the neuroscience community.

### 6. Integrative Approach
Instead of creating new data storage tools and attempting to reinvent our entire system, this ecosystem smartly integrates established tools like REDCap and LAVA, ensuring best practices are followed.

### 7. Security
Tools like Voilà ensure that while data can be accessed and visualized, the raw data remains secure.
