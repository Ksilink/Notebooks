# SHANK3 screening data analysis - *Thibaudeau et al.*

Link to publication: Not yet available (add bioRxiv later)

## Purpose
The provided primary screening data and Jupyter notebook allows to explore the screening data presented in *Thibaudeau et al.* and reproduces the presented results. 

## Data structure
The provided data describes the results of the primary screen using chemical compounds whose effects were measured using microscopical imaging and image segmentation. The segmented images were then used to quantify phenotypic features. The data file contains these phenotypic feature names and additional meta data columns. The first row of the csv file contains the column headers, which describe the different data fields (phenotypic features and meta data). Each subsequent row represents a single observation. For example, the first column Plate represents the plate identifier, the second column Well represents the well identifier, and so on. The provided Jupyter notebook will make use of this data.

## Jupyter notebook
The provided Jupyter notebook will first install all required packages, import them, and load the provided data. 

Next, raw data quality control plots are generated that visualize two of the quantified phenotypic features per plate (Ratio_nuclei_hucd and Ratio_nuclei_ki67). Z-factors are calculated and plotted for the raw data per plate. During the next steps, the screen data is normalized by plate to minimize batch effects. As with the raw data, quality control plots are generated that visualize Ratio_nuclei_hucd and Ratio_nuclei_ki67 and Z-factors are calculated and plotted. Next, correlation scatter plots are generated to compare the screen performance accross the two replicates using the Ratio_nuclei_hucd and Ratio_nuclei_ki67 data.

Hit identification is performed by applying standard deviation thresholds from the DMSO median and the hits are visualized in a scatter plot showing Ratio_nuclei_hucd on the x-axis and Ratio_nuclei_ki67 on the y-axis. Finally, available pathway and target infos for hits are displayed as bar and pie charts to illustrate their frequency.

## Usage
The provided Jupyter notebook can be easily run in one click assuming that Python and Jupyter Notebook have been installed.

### You are new to this and need to install Python and Jupyter Notebook
You can download and install the latest version of Python from the official Python website (https://www.python.org/downloads/). Once you have Python installed, you can install Jupyter Notebook by running "pip install notebook" in your command prompt or terminal. Alternatively, you can install the Anaconda distribution (https://www.anaconda.com/download), which comes with both Python and Jupyter Notebook pre-installed. Follow one of the many tutorials about the use of Jupyter Notebooks and get started.

### You know how to run a Jupyter Notebook
Clone or download the entire "SHANK3screening" repository to your local machine. You can now run the provided “SHANK3_screen_analysis_notebook” Jupyter notebook. During execution all outputs will be automatically saved in newly created folders in the source directory.
