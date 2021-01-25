# Prediction of disease-associated deleterious variants in non-coding regions through a comprehensive analysis by integrating datasets and features

In this study, we integrated well-established features and commonly used datasets, and merged them into large-scale datasets based on a random forest model, which yielded promising performance and outperformed some cutting-edge approaches. 


This directory contains all code and data necessary to reproduce the figures and tables from our manuscript.



## Directories


Classifier score across human non-coding regions/ - contains the source data used to generate Figure 12, Figure 13, Figure 13—Supp.FigureS2, and Figure 13—Supp.FigureS3.

Contribution of different feature groups/ - contains the source data used to generate Figure 11.

Contribution of individual features/ - contains the source data used to generate Figure 9, Figure 10, Figure 10—Supp.FigureS1 and Table 4.

Dataset/ - contains the feature matrix of the training set and the validation set.

Model 1 prediction results/ - contains the source data used to generate the prediction performance of Model 1 in Tabel 2.

Model 2 prediction results/ - contains the source data used to generate the prediction performance of Model 2 in Tabel 2.

Model 3 prediction results/ - contains the source data used to generate the prediction performance of Model 3 in Tabel 2.

Notebooks/ - contains Python code to generate figures and tables used in our manuscript.

Other methods score/ - contains the source data used to generate Figure 7.

Other methods score2/ - contrains the source data used to generate Figure 8.

### Description of these files

The Classifier score across human non-coding regions/ directory contains two files: dataset_8terms_score.txt and terms_score_Fea_datasets.zip. In the dataset_8terms_score.txt, each row is a variant, the first column is the chromosome number where the variant is located, the second column is the location of the variant, the third column is the reference allele, the fourth column is the alternative allele, and the fifth column is true label of the variant ('1' represents harmful, '0' represents benign), the sixth column is the prediction score, and the seventh column is the non-coding region where the variant is located. For terms_score_Fea_datasets.zip, first unzip the file and in the terms_score_Fea_datasets, the meaning of the first seven columns is the same as dataset_8terms_score.txt, then the eighth column and later are the features values of the variant.


The Contribution of different feature groups/ directory contains six files. Five feature groups were used to build the model separately, and False positive rate and True positive rate of the independent dataset are recorded in these six files, respectively. In each file, the first column is the False positive rate, and the second column is True positive rate.


Contribution of individual features/ directory contains four files: 13_impor_features.csv, 19_impor_features.csv, distribution of features importance to Model 3, and distribution of features importance to Model 1. 13_impor_features.csv records the Gini importance of the 13 most important features in five training sets to Model 3, the first column is Five-fold cross-validation, the second column is Gini importance, and the third column is feature name; 19_impor_features.csv records the Gini importance of the 19 most important features in five training sets to Model 1, the first column is Five-fold cross-validation, the second column is Gini importance, and the third column is feature name; distribution of features importance to Model 3.xlsx is the source data used to generate Figure 8A; distribution of features importance to Model 1.xlsx is the source data used to generate Figure 9—Supp.FigureS1.


Dataset/ directory contains three files: training_set.zip, validation_set.zip. For validation_set.zip and training_set.zip, first unzip the two files, the training_set and validation_set are from our study. In the training_set, the meaning of the first five columns is the same as dataset_8terms_score.txt, then the sixth column and later are the features values of the variant; in the validation_set, the meaning of each column is the same as the training_set.


Model 1 prediction results/ directory contains three files: training_predictproba, test_predictproba, GWASdb_1kgp_predictproba. In each file, the first column is the true label of the variant, and the second column is the prediction score.
 

Model 2 prediction results/ directory contains three files: training_predictproba, test_predictproba, clinvar_predictproba. In each file, the first column is the true label of the variant, and the second column is the prediction score.


Model 3 prediction results/ directory contains two files: training_predictproba, test_predictproba. In each file, the first column is the true label of the variant, and the second column is the prediction score.


Other methods score/ directory contains nine files, they are prediction score of nine methods to the independent dataset. For each file, the meaning of the first column is the true label of the variant, and the second column is the  prediction score for each variant; Besides, for validation_set_GWAVA_predict_proba, the second, the third, and the fourth column is the GWAVA (Region) prediction score, GWAVA (TSS) prediction score, GWAVA (Unmatched) prediction score for each variant, respectively.


Other methods score2/ directory contains nine files, they are prediction score of all methods to the independent dataset. For each file, the meaning of the first column is the true label of the variant, and the second column is the  prediction score for each variant; Besides, for validation_set_GWAVA_predict_proba, the second, the third, and the fourth column is the GWAVA (Region) prediction score, GWAVA (TSS) prediction score, GWAVA (Unmatched) prediction score for each variant, respectively.


Notebooks/ directory contains ten scripts, we use Python 3 and anaconda is recommended. 


The Python libraries required for these scripts are:

- numpy (1.16.5)
- pandas (0.25.1)
- scikit-learn (0.21.3)
- matplotlib (3.1.1)
- matplotlib-venn (0.11.5)
- seaborn (0.9.0)


Step1-Bar chart showing the overall AUC of the training set with varying number of trees.ipynb is the source code to generate Figure 4.

Step2-Tutorial of our study and the comparison of Model 3 with other methods.ipynb is the source code to generate Figure 7 and it needs files under two folders  (i.e. Dataset/ and Other methods score/).

Step3-Performance of different dataset modeling.ipynb is the source code to generate Table 2 and it needs files under three folders (i.e. Model 1 prediction results/, Model 2 prediction results/, and Model 3 prediction results/).

Step4-Comparison of model for removing GWASdb and other methods.ipynb is the source code to generate Figure 8 and it needs files under one folder  (i.e. Other methods score2/).

Step5-Heatmap showing the distribution of Gini importance of 13 important features in five training sets.ipynb is the source code to generate Figure 9B and it needs a file (i.e. 13_impor_features.csv).

Step6-Comparison of Model 1 and Model 3.ipynb is the source code to generate Figure 10A and this script needs two files (i.e. 13_impor_features.csv and 19_impor_features.csv).

Step7-Relative information of 6 features only found in Model 1.ipynb is the source code to generate Table 4 and it needs two files (i.e. 13_impor_features.csv and 19_impor_features.csv).

Step8-Performance of the five feature groups in Model 3.ipynb is the source code to generate Figure 11 and it needs files under one folder (i.e. Contribution of different feature groups/).

Step9-Distributions of random forest classifier scores for various noncoding regions.ipynb is the source code to generate Figure 12 and it needs a file (i.e. dataset_8terms_score.txt).

Step10-Distribution of 13 important features value in different non-coding region.ipynb is the source code to generate Figure 13, Figure 13-Supp.FigureS2, and Figure 13-Supp.FigureS3, and this script needs a file (i.e. terms_score_Fea_datasets).

