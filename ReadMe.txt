#Creation Date: 2021113
#Author: Christoph Sadee
#Last Change Date: 2021115

#Software and installation
################################################
Python2: Python 2.7.17

Structure predictions using Vienna RNAfold for python: 
https://www.tbi.univie.ac.at/RNA/documentation.html 

Python packages used for RNA-MaP package:
numpy					1.16.6
scipy					0.16.0 
pandas					0.18.1 
statsmodels				0.6.1 
scikits.bootstrap 		1.0.1
matplotlib				2.0.0 
seaborn					0.7.0 
joblib					0.8.4 
lmfit					0.8.3 
Biopython				1.63 
scikit-learn			0.17.1
ipdb					0.13.2

Python packages used for post RNA-MaP analysis:
biopython                          1.63
Cython                             0.29.21
DateTime                           4.3
ipdb                               0.13.2
ipykernel                          4.10.1
ipython                            5.9.0
jupyter                            1.0.0
lmfit                              0.8.3
luigi                              2.8.13
matplotlib                         2.2.5
numpy                              1.16.6
pandas                             0.24.2
pip                                19.3.1
pipenv                             2018.11.26
scikit-learn                       0.17.1
scikits.bootstrap                  1.0.1
sciluigi                           0.9.7
scipy                              1.2.3
seaborn                            0.7.0
setuptools                         41.4.0
virtualenv                         20.4.3



#Data:
################################################
data/MasterDfs/ : Contains sample datafiles with computed affinity measures and annotation

#Folders:
#################################################
RNA-MaP package: Code to compute affinity values from RNA-MaP Raw data as describe in Methods 'Fluorescence normalization and determination of the free energy of binding', 'Single cluster fitting' and 'Determining KD'. Installation outlined in 'Jarmoskaite, Inga, et al. "A quantitative and predictive model for RNA binding by human Pumilio proteins." Molecular cell 74.5 (2019): 966-981.' and https://github.com/GreenleafLab/array_fitting_tools 

CombiningReplicates: CombineReplicates.py to combine replicates as described in Methods 'Combining replicates'

PredictingStructure: PredictingStructure.py to predicts structure using Vienna RNA fold as described in Methods 'Filtering out structured variants'

AssessingAlternativeRegisters: find_registers_UGUAUAUUA.py to find alternative registers as described in Methods 'Assessing alternative binding registers in single mutants'

data_FilteredForModel : get_single_mut_params_UGUAUAUAU_aj0_0p5strucCSCutoff.py to filter sample datafiles as described in Methods 'DataFiltering' & 'Determining relative affinities' & 'Filtering out structured variants' and prepares for use in PUF4 model

ParameterSensitivity: model_params_sensitivity_PUF4multiprocessing.py to vary each additive parameter in model and compute change in RMSE as described in Methods 'Development, testing and evaluation of PUF4 thermodynamic binding models'

PUM2Model: analyse_pum2.py code and data to apply PUM2 model without optimization to RNA-Map data as described in methods 'Development, testing and evaluation of PUF4 thermodynamic binding models'

PUM2Model_FlipsOptimized: pum2_model_flips_optimized.py code and data applying PUM2 model with flips allowed to vary / optimize on RNA-Map data as described in methods 'Development, testing and evaluation of PUF4 thermodynamic binding models'

PUF4Model_Optimization: puf4_flip_model.py code and data applying PUF4 model with all parameters except consensus sequence allowed to vary / optimize on RNA-Map data as described in methods 'Development, testing and evaluation of PUF4 thermodynamic binding models'

PUF4Model_AppliedToTranscriptome: predict_affinity_window1X_PUXX.py & sliding_window.py Code and data to subdivide yeast genome into 11nt and 13nt windows and apply PUF4, PUM2 & PUF3 model as described in 'Predicting PUF3 and PUF4 binding sites in the yeast genome', 'Predicting PUF3 and PUF4 binding sites in the yeast genome with a longer sequence motif', 

GenomeAnnotationConversion: downgrade_annotation_via_realignment.py to downgrade R64 annotation from SGS to R62 genome used in the transcriptome analysis as described in '3’UTR annotation for yeast transcriptome'





