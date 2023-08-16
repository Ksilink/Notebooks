# Jupyter Notebook for phenotypic profile analysis - *Weiss et al.*
Full article: dx.doi.org/10.3791/65570

## Introduction
This Jupyter Notebook performs data plotting and all unsupervised and supervised analysis methods described in the article. It can serve as an easy to use entry point into phenotypic profile data analysis.

## Data structure
The "Raw_mDANeuron_phenotypic_features.fth" file contains the data required for reproducing the findings reported in *Weiss et al.*. Most columns contain continous phenotypic feature data derived from an image segmentation/analysis workflow using the PhenoLink software (https://github.com/Ksilink/PhenoLink). Additional columns contain categorical data detailing the used experimental conditions (i.e. postion on plate or chemical treatment). Each row contains the mean values per 384-well plate well derived from 16 images acquired using a 40X objective.

## Data Loading and Feature Scaling
The data analysis workflow starts by data loading and feature scaling. Scaling is important for machine learning because it helps to normalize the data and ensure that each feature is on a similar scale.

## Data visualization
In the next step, data visualization of individual features and clustering is performed. Clustering can be useful for exploring the structure of high-dimensional datasets and identifying patterns in the data. Next to clustering, dimension reduction approaches are also a useful tool to visualize the similarities and differences of multidimensional phenotypic profiling data. Here we made use UMAP and PaCMAP.

## Supervised Classification
Next, machine learning-driven supervised classification is performed. Specifically, we used the Light gradient-boosting machine (LightGBM) algorithm. LightGBM is a supervised machine learning algorithm that uses decision tree algorithms to create a model that can be used for ranking or classification. In the notebook, the algorithm is trained with phenotypic profile data from one plate. The trained model is then tested on data from a second independent plate.

## Usage
1. Clone this repository or download both the notebook .ipynb, data .fth and requirements .txt files into the same directory.
2. Install the required packages, if not already present.
3. Open the Jupyter notebook and run the cells to reproduce the analysis.
