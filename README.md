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

## Project Structure
.
├── Toolbox.ipynb # Utilities and helper functions
├── dln_GREALM.ipynb # Main notebook: download, extract, and structure data
├── README.md # Project documentation (this file)
└── .gitattributes # Git configuration attributes
