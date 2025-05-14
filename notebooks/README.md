# SWM analysis workflow 

## Directory file content
| File                                                                                                                                                                      | Description                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [`1-1_Intensity-Profiles_BigBrain.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/1-1_Intensity-Profiles_BigBrain.ipynb)             | [SWM mapping in the BigBrain](#1-1-swm-mapping-in-the-bigbrain)                                                      |
| [`1-2_Intensity-Profiles_AHEAD.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/1-2_Intensity-Profiles_AHEAD.ipynb)             | SWM mapping in the AHEAD brain                                                                      |
| [`1-3_Intensity-Profiles_qMRI.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/1-3_Intensity-Profiles_qMRI.ipynb) | SWM mapping using 7T qMRI                                                                      |
| [`2_NeuralContext_Cyto.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/2_NeuralContext_Cyto.ipynb)                         | Neural contextualization with cytoarchitecture                                                  |
| [`3_StatisticalMoments.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/3_StatisticalMoments.ipynb)                       | Statistical moments across GM-WM depth from histology and qMRI  |
| [`4_Microstructural-Gradients_qMRI.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/4_Microstructural-Gradients_qMRI.ipynb)                                                                       | SWM mean MPC across subjects |
| [`5_Corr_Cortical-geometry_qMRI.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/5_Corr_Cortical-geometry_qMRI.ipynb)                                                                       | Cortical geometry correlations of qMRI gradients |
| [`6-1_Corr_BrainConnectivity_qMRI.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/6-1_Corr_BrainConnectivity_qMRI.ipynb)                                                                       | Brain connectivity strength correlates of qMRI gradients |
| [`6-2_Corr_mean-BrainConnectivity.ipynb`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/6-2_Corr_mean-BrainConnectivity.ipynb)                                                                       | Mean brain connectivity strength correlates of mean qMRI gradients |

## [`1-1. SWM mapping in the BigBrain`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/1-1_Intensity-Profiles_BigBrain.ipynb)
### Process intensity profiles using the BigBrain SWM intensity data
* **Surface-based intensity smoothing and processing:** Smooth intensity profiles at each surface to reduce noise and enhance spatial continuity, then combine them into a unified profile.
* **Correcting outliers:** Identify and correct outliers in the intensity data to improve robustness.
* **Intensity visualization:** Plot the intensity profiles and their distribution for visual inspection and analysis.

## [`1-2. SWM mapping in the AHEAD brain`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/1-2_Intensity-Profiles_AHEAD.ipynb)
### Process intensity profiles using the AHEAD SWM intensity data
* **Surface-based intensity smoothing and processing:** Smooth intensity profiles at each surface to reduce noise and enhance spatial continuity, then combine them into a unified profile.
* **Intensity visualization:** Plot the intensity profiles and their distribution for visual inspection and analysis.
   
## [`1-3. SWM mapping using 7T qMRI`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/3_StatisticalMoments.ipynb)
### Process intensity profiles using the 7T MRI intensity data
* **Surface-based intensity smoothing and processing:** Smooth intensity profiles at each surface to reduce noise and enhance spatial continuity, then combine them into a unified profile.
* **Intensity visualization:** Plot the intensity profiles and their distribution for visual inspection and analysis.
   
## [`2. Neural contextualization with cytoarchitecture`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/2_NeuralContext_Cyto.ipynb)
### Cellular intensity profiles across SWM depths
* Plot smoothed profiles across SWM depths using filtered intensity maps, based on cytoarchitectonic atlases.
* Cytoarchitectonic classes used: Mesulam and Von Economo.

## [`3. Statistical moments across GM-WM depth from histology and qMRI`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/3_StatisticalMoments.ipynb) 
### Microstructural profiling of SWM
* **Combine GM-WM intensity profiles:** Stack intensity profiles from the CSF/GM boundary through the GM/WM interface and extending up to 3 mm into the SWM.
* **Statistical moments by depth:** Calculate central statistical moments (mean, standard deviation, skewness, and kurtosis) across the surface to quantify regional variation.
* **Visualization:** Plot the spatial distribution of statistical moments across the cortex and superficial white matter.

## [`4. SWM mean MPC across subjects`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/4_Microstructural-Gradients_qMRI.ipynb)
### Generate mean gradient from 7T qMRI
* **Build the mean MPC from SWM intensity profiles:** Compute the correlation matrix of SWM intensity profiles across 10 subjects.
* **Create SWM gradients from the MPC:** Apply diffusion map embedding using _BrainSpace_ to derive the gradients.

## [`5. Cortical geometry correlations of qMRI gradients`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/5_Corr_Cortical-geometry_qMRI.ipynb)
### Associations between cortical geometry and SWM gradients derived from 7T qMRI
* **Build the MPC from SWM intensity:** Compute the correlation matrix of SWM intensity profiles for each subject.
* **Gradient correlation with brain geometry:** Assess the relationship between individual SWM gradients (G1) and cortical geometry (curvature and thickness) using spin permutation testing.

## [`6-1. Brain connectivity strength correlates of qMRI gradients`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/6-1_Corr_BrainConnectivity_qMRI.ipynb)
### Associations between functional and structural connectivity and SWM gradients derived from 7T qMRI
* **Build the MPC from SWM intensity:** Compute the correlation matrix of SWM intensity profiles for each subject.
* **Correlate gradients with functional and structural connectivity:** Assess the relationship between individual SWM gradients (G1) and both functional and structural connectivity using spin permutation testing.

## [`6-2. Mean brain connectivity strength correlates of mean qMRI gradients`](https://github.com/MICA-MNI/MRI-Histology_framework_for_SWM_architecture/blob/main/notebooks/6-2_Corr_mean-BrainConnectivity.ipynb)
### Associations between functional and structural connectivity and SWM gradients across 10 subjects 
* Build the mean MPC from 7T qMRI (Step 5)
* Compute the mean functional and structural connectivity across 10 subjects.
* Correlate the mean SWM gradients with mean functional and structural connectivity across subjects.
