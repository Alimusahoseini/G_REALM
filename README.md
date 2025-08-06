# G-REALM Lake Altimetry Toolbox

A Python toolkit for **downloading, extracting, and structuring global lake water level time series** from the [G-REALM database](https://ipad.fas.usda.gov/cropexplorer/global_reservoir/), maintained by USDA-FAS in collaboration with NASA, CNES, ESA, and other space agencies.

---

## Overview

This repository provides scripts to:
- **Download** lake water level time series from the G-REALM database (multiple temporal resolutions available).
- **Extract** and **structure** the raw data into an analysis-ready format.
- **Visualize** the time series for each lake.

The toolkit supports rapid exploration and reproducible extraction of satellite altimetry data for global lakes, suitable for hydrological research and scientific publications.

---
<br>

## Project Structure

``` .
├── Toolbox.ipynb # Utilities and helper functions
├── dln_GREALM.ipynb # Main notebook: download, extract, and structure data
├── README.md # Project documentation (this file)
└── .gitattributes # Git configuration attributes
``` 
<br>


- `Toolbox.ipynb`: Contains utility functions for analysis and visualization.
- `dln_GREALM.ipynb`: Main pipeline: data download, extraction, and structuring.
- `lake_struct_data.pkl`: Output file — structured lake metadata and timeseries (created after running the pipeline).

---

## Installation

### Prerequisites

- Python 3.7+
- Required packages:  
  `pandas`, `matplotlib`, `requests`

You can install the requirements via:

```bash
pip install pandas matplotlib requests
``` 
Usage
1. Download & Extract G-REALM Data
Run the provided code (in notebook or as a Python script). You will be prompted to select the desired temporal resolution (e.g., 10-Day, 35-Day, etc.), and the script will automatically download and extract the files.
, etc.)

