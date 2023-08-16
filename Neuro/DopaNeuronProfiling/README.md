# Jupyter Notebook for Data Analysis Workflow

This Jupyter Notebook performs data plotting and all unsupervised and supervised analysis methods described in the scientific article. The data analysis workflow starts by data loading and feature scaling. Scaling is important for machine learning because it helps to normalize the data and ensure that each feature is on a similar scale. This can help improve the performance of machine learning algorithms by making them less sensitive to the scale of the input features.

In the next step, clustering analysis is performed. Clustering can be useful for exploring the structure of high-dimensional datasets and identifying patterns in the data that might not be immediately apparent from looking at individual features. Hierarchical clustering based on the Cosine distance between well-based phenotypic profiles showed strong differences between cell lines, but less for drug treatment.

Next to clustering, dimension reduction approaches are also a useful tool to visualize the similarities and differences of multidimensional phenotypic profiling data. Here we made use of Pairwise Controlled Manifold Approximation (PaCMAP). Similar to the previous Cosine distance-based approach also PaCMAP showed mainly differences between the two cell lines and to a lesser extend between PFE-360 or DMSO control treated wells.

To address this limitation of phenotypic profile analysis, we performed machine learning-driven supervised classification. Specifically, we used the Light gradient-boosting machine (LightGBM). LightGBM is a supervised machine learning algorithm that uses decision tree algorithms to create a model that can be used for ranking or classification. LightGBM has been designed to be faster and more efficient than traditional tree-based algorithms such as the Random forest algorithm.

We trained the algorithm with phenotypic profile data from one plate and tested the trained model on data from a second independent plate. The LightGBM model had an overall accuracy of 85% and correctly predicted the experimental category (cell line or compound) of most wells. The accuracy for cell line prediction was higher than for compound prediction, but also 60% of compound-treated wells were predicted correctly which is superior to classical unsupervised methods.

LightGBM permits to access the importances of the respective phenotypic features for classification of the four classes. Important phenotypic features that distinguish the cell lines and drug treatments are for example related to the cellular surface area or the cellular intensities of the MAP2 and TH stainings.

The obtained results illustrate the potential of phenotypic profiling to distinguish cell lines and compound treatment effects in human mDA neurons.
