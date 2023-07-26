# Jupyter Notebook for Phenotypic Data Analysis - *Di Credico et al.*

This repository contains a Jupyter Python notebook for processing and analyzing microscopic imaging data generated from human stem cell derived dopaminergic neurons that were treated with endocrine disruptors (EDs).

## Data structure
The raw_data.fth file contains the data required for reproducing the findings reported in *Di Credico et al.*. Most columns contain continous phenotypic feature data derived from an image segmentation/analysis workflow using the PhenoLink software (https://github.com/Ksilink/PhenoLink). Additional columns contain categorical data detailing the used experimental conditions (i.e. postion on plate or chemical treatment). Each row contains the mean values per 384-well plate well derived from 16 images acquired using a 40X objective.

## Pre-processing
The data is pre-processed per biological replicate using the RobustScaler method from the scikit-learn package, which scales the data according to the interquartile range (IQR).

## Visual data exploration
Data from single phenotypic features is graphically explored using boxplots and dose-response graphs. In a next step, the notebook generates a visual representation of the neuron's phenotypic profiles using a heatmap and performs clustering using the Cosine distance metric. Additionally, profile similarity is visually explored using the two unsupervised embedding techniques UMAP and PaCMAP. 

## Machine learning classification
The notebook also includes a machine learning pipeline for classification using either the XGBoost or LightGBM classifiers. The data is split into training and testing sets, with 10% of the data being used for testing. Grid search cross-validation with 5 folds is used to find the best hyperparameters for each classifier. The pipeline is then trained on the full training set using the best hyperparameters found. Feature importances are calculated and plotted to show the most important features used by the models. 10 fold cross-validation accuracy scores are also calculated and plotted. Predictions are made on the test set, and the probabilities of each sample belonging to the “Control” class are calculated. The accuracy of the classifier on the test set is evaluated, and a confusion matrix is computed and plotted as a heatmap.

## Usage
1. Clone this repository or download both the notebook .ipynb and data .fth files into the same directory.
2. Install the required packages, if not already present.
3. Open the Jupyter notebook and run the cells to reproduce the analysis.
