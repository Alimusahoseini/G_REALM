Lake Altimetry Toolbox
This repository provides a Python toolbox for downloading, extracting, and visualizing global lake water level time series using the G-REALM database, derived from satellite radar altimetry.

Table of Contents
Overview

Folder Structure

Requirements

Usage

1. Download G-REALM Data

2. Parse and Visualize Lake Data

Data Description

Acknowledgments & Citation

Overview
This toolbox supports the workflow for research projects on global lake water level changes.
It includes two main Python scripts:

Download GREAL – A script for interactive downloading and extracting G-REALM data files.

Toolbox – Scripts for parsing, structuring, and plotting lake altimetry time series.

All scripts are ready for use with the G-REALM public dataset maintained by USDA-FAS, NASA, CNES, ESA, and partners.

Folder Structure
bash
Copy
Edit
.
├── Download_GREAL.py      # Script to download and extract G-REALM data
├── toolbox.py             # Toolbox: parse, structure, visualize data
├── lake_data_XXDay/       # Folder containing the extracted raw text files
├── lake_struct_data.pkl   # Pickle file with structured data
└── README.md
Requirements
Python 3.7 or higher

pandas

matplotlib

requests (for Download GREAL script)

Install all dependencies using:

bash
Copy
Edit
pip install pandas matplotlib requests
Usage
1. Download G-REALM Data
Use Download_GREAL.py to download and extract lake data files for your desired period (10-Day, 27A-Day, 27B-Day, 35-Day):

bash
Copy
Edit
python Download_GREAL.py
Follow the prompts to select your preferred data frequency.

The script downloads and extracts the relevant .tar.gz file, and prints the list of available text files.

2. Parse and Visualize Lake Data
Use toolbox.py to parse all extracted .txt files, extract metadata and time series, and save the structured data as a .pkl file.
You can also plot the water level time series for any lake:

bash
Copy
Edit
python toolbox.py
Or in a Jupyter notebook:

python
Copy
Edit
import pandas as pd
df_lakes = pd.read_pickle('lake_struct_data.pkl')
lake = df_lakes[df_lakes['lake_name'] == 'Cardiel'].iloc[0]
# Extract dates and heights for valid records
times = [row['date'] for row in lake['data'] if row['obs_height'] < 900]
heights = [row['obs_height'] for row in lake['data'] if row['obs_height'] < 900]
# Plot with matplotlib
Data Description
Each lake file provides:

Metadata: Name, ID, latitude, longitude, track.

Water level series: Dates, observed heights, reference corrections (EGM2008), satellite info, error and correction parameters, quality flags.

Source:
G-REALM (Global Reservoir and Lake Monitor) Database

Acknowledgments & Citation
If you use these scripts or G-REALM data in your research, please cite the G-REALM project and acknowledge the USDA-FAS, NASA, CNES, ESA, and all contributing agencies.


