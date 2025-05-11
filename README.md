# TD Garden Assault Incident Analysis

This repository contains an R script and a split dataset for analysing assault incidents in the TD Garden area of Boston between 2019 and 2022. The analysis includes temporal, spatial, and predictive modelling components.

## 📂 Repository Contents

- `FinalCode.R`:  
  A complete R script covering:
  - Data loading and preparation
  - Date and time feature engineering
  - Geographic filtering around TD Garden
  - Exploratory visualisations
  - Spatial density calculations
  - Predictive modelling (kNN, Linear, Polynomial, Decision Tree, Ensemble)
  - Map-based visualisations
  - PDF report generation

- `data/`:  
  Contains split parts of the Boston crime dataset (see below).

## 📥 Download the Dataset

The dataset has been split into five parts due to file size limitations.  
Please download **all five files** and place them in the `/data/` directory:

1. `Boston_Crime_Data_2019_2023_1.csv`
2. `Boston_Crime_Data_2019_2023_2.csv`
3. `Boston_Crime_Data_2019_2023_3.csv`
4. `Boston_Crime_Data_2019_2023_4.csv`
5. `Boston_Crime_Data_2019_2023_5.csv`

Once all files are downloaded, you can load them together in R by running:

```r
# Combine all split files into one dataframe
library(dplyr)

file_list <- list.files("data/", pattern = "Boston_Crime_Data_2019_2023_.*\\.csv$", full.names = TRUE)
full_data <- do.call(rbind, lapply(file_list, read.csv))

# Proceed with analysis using full_data
🚀 How to Run
Clone or download this repository.

Download and place all five dataset parts in the /data/ folder.

Open FinalCode.R in RStudio.

Install required R packages:

r
Copy code
install.packages(c("tidyverse", "ggmap", "googleway", "FNN", "caret", 
                   "viridis", "tree", "boot", "lubridate", "gridExtra", 
                   "grid", "RColorBrewer"))
Replace the placeholder API key in register_google() with your own valid Google Maps API Key.

Run the script interactively to process the data and generate results.

[Boston_Crime_Data_2019_2023 (1)_5.csv](https://github.com/user-attachments/files/20149782/Boston_Crime_Data_2019_2023.1._5.csv)
[Boston_Crime_Data_2019_2023 (1)_4.csv](https://github.com/user-attachments/files/20149781/Boston_Crime_Data_2019_2023.1._4.csv)
[Boston_Crime_Data_2019_2023 (1)_3.csv](https://github.com/user-attachments/files/20149780/Boston_Crime_Data_2019_2023.1._3.csv)
[Boston_Crime_Data_2019_2023 (1)_2.csv](https://github.com/user-attachments/files/20149779/Boston_Crime_Data_2019_2023.1._2.csv)
[Boston_Crime_Data_2019_2023 (1)_1.csv](https://github.com/user-attachments/files/20149778/Boston_Crime_Data_2019_2023.1._1.csv)
