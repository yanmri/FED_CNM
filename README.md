# FED_CNM
Extracted peak coordinates and NIfTI-format network maps from the study:

“Network-Level Convergence of Functional and Structural Alterations in First-Episode Major Depressive Disorder.”

Files

Table 1: Coordinates (in MNI space) of significant clusters identified in resting-state activity studies.

Table 2: Coordinates (in MNI space) of significant clusters identified in gray matter volume studies.

FED-associated network probability map_functional.nii: FED-associated network probability map derived from the functional modality.

FED-associated network probability map_structural.nii: FED-associated network probability map derived from the structural modality.

FED-associated network_functional_0.5.nii: FED-associated network identified from the functional modality using a 50% probability threshold.

FED-associated network_functional_0.5_binary mask.nii: Binary mask of the FED-associated network identified from the functional modality using a 50% probability threshold. Voxels belonging to the network are assigned a value of 1, whereas all other voxels are assigned a value of 0.

FED-associated network_structural_0.5.nii: FED-associated network identified from the structural modality using a 50% probability threshold.

FED-associated network_structural_0.5_binary mask.nii: Binary mask of the FED-associated network identified from the structural modality using a 50% probability threshold. Voxels belonging to the network are assigned a value of 1, whereas all other voxels are assigned a value of 0.

Probability_map.m: Code for generating the probability maps using the binarized maps derived from all ROIs. The ROIs were defined as 6-mm-radius spheres centered on each extracted peak coordinate. For each ROI, one-sample t-tests were performed on the 1,000 ROI-to-whole-brain functional connectivity (FC) maps using an FWE-corrected threshold of p < 0.05 to identify brain regions showing significant functional connectivity with the ROI. Only positive FC was considered. The resulting t-maps containing significant clusters for each ROI were subsequently binarized. Probability_map.m uses these binarized maps to generate the corresponding network probability maps, representing the proportion of ROIs for which each voxel showed significant positive functional connectivity.
