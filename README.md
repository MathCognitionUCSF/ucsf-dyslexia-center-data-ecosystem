# UCSF Dyslexia Center - Data Ecosystem

![images](/ucsfneuroviz_flowchart_10-18-2023-2.png)

## Overview

### Raw Data:

Sources of data include Structural MRI, Diffusion MRI, Functional MRI, and Behavioral Data.

Data is stored in various databases:
* [REDCap](https://redcap.ucsf.edu/)
* [LAVA](https://github.com/UCSFMemoryAndAging/lava/)
* [MAC Imaging-Core](https://github.com/UCSFMemoryAndAging/imaging-core)

Dyslexia Center neuroimaging data is stored in a standardized structure called [BIDS](https://bids.neuroimaging.io/) on UCSF secure drives.

### Pre-processing:

Data undergoes pre-processing using tools on the Wynton HPC. The tools used include:
* [sMRIprep](https://github.com/nipreps/smriprep) for structural MRI
* [QSIprep](https://github.com/PennLINC/qsiprep) for diffusion MRI
* [fMRIprep](https://github.com/nipreps/fmriprep) for functional MRI

### Post-processing:

Further data refinement is done on both the local machine and Wynton HPC. This includes:
* Generating statistical files using Bash scripts
* Generating contrasts using Python scripts
* [Fetching REDCap data using Python with an API](https://github.com/MathCognitionUCSF/REDCap_tools)

### Data Standardization:

* Data is standardized in specific formats like FreeSurfer metrics, interactive tractography, and CSV files
* Data is stored in a consistent and easy to follow file structure on secure UCSF drives.

### Data Analysis:

* Advanced analysis, including machine learning predictions and group comparisons, are done using [Wynton HPC](https://wynton.ucsf.edu/hpc/index.html), which is UCSF's High Performance Cluster. Less computationally intensive analysis steps may be performed on local machine.
* Encoding/Decoding models linking brain and behavior are implemented using Python tools such as [nilearn](https://github.com/nilearn/nilearn) and [nibabel](https://github.com/nipy/nibabel).

### [Ucsfneuroviz](https://github.com/MathCognitionUCSF/ucsfneuroviz) Browser:

The browser allows dynamic and interactive visualization of Structural MRI, Diffusion MRI, Functional MRI, and behavioral scores.
We will also implement a section for publication-grade visualizations of analysis results.

### Supporting Tools:

* [Python](https://www.python.org/): Used for scripting, generating Jupyter notebooks, and handling data.
* [Voilà](https://voila.readthedocs.io/en/stable/): Converts Jupyter notebooks into interactive dashboards with minimal setup.
* [Binder](https://mybinder.org/): Allows for sharing of data via Git, making the entire process reproducible without requiring local machine setup.

## Pros of this Approach

### 1. Flexible
The ecosystem is designed to easily accommodate various data types and sources.

### 2. Modular
Each step in the process is clearly defined, allowing for individual modules to be updated or replaced without disrupting the entire system.

### 3. Robust
With the use of established tools and databases, the pipeline ensures reliability and accuracy in data processing and analysis.

### 4. Ready for Multimodal & Multicenter Data
The structure is ready to handle diverse data types from various centers, ensuring a wide range of applicability.

### 5. Prepared for Data Sharing
With the use of [BIDS](https://bids.neuroimaging.io/) format, the system is already aligned with standards for data sharing in the neuroscience community.

### 6. Integrative Approach
Instead of creating new data storage tools and attempting to reinvent our entire previous system, this ecosystem smartly integrates established tools like REDCap and LAVA, ensuring best practices are followed.

### 7. Secure Platform
Tools like Voilà ensure that while data can be accessed and visualized, the raw data remains secure.
