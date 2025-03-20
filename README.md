# MRI-Histology framework for SWM architecture

**Cite:**

> *[Youngeun Hwang](mailto:youngeun.hwang2@mail.mcgill.ca), Raul Rodriguez-Cruces, Jordan DeKraker, Donna Gift Cabalo, Ilana R Leppert, Risavarshni Thevakumaran, Christine L. Tardif, David Rudko, Pierre-Louis Bazin, Andrea Bernasconi, Neda Bernasconi, Luis Concha, Alan C. Evans, [Boris C. Bernhardt](mailto:boris.bernhardt@mcgill.ca). (2025). A unified imaging-histology framework for superficial white matter architecture studies in the human brain. ...*

**DOI:** [TBD]().

**Keywords:** Superficial white matter, Histology, Magnetic resonance imaging (MRI), Ultra-high field MRI, 7 Tesla MRI, Quantitative MRI

## Overview
This repository contains the code and analysis notebooks for studying superficial white matter (SWM) microstructure using *post-mortem* and *in-vivo* datasets. It includes preprocessing, statistical analysis, and visualization scripts to assess intensity profiles from all datasets, gradients from quantitative MRI (qMRI), and their correlations with cortical geometry, functional and structural connectivity.
- Intensity profiles derived from each histology and qMRI data
- Statistical moments of the intensity profiles
- Constructing microstructural gradients in SWM
- Cortical geometry correlations of qMRI gradients
- Functional & Structural connectivity strength correlates of qMRI gradients

## Open Data and Software
This study was conducted using open datasets, listed below:
- BigBrain: Merker-stained *post-mortem* histological data (Amunts et al., 2013)
- Ahead brain: Multistaining *post-mortem* histological data (Alkemade et al., 2022) 
- MICA-PNI: Ultra-high field 7T MRI data (Cabalo et al., 2024)

We also utilized multiple open-source software packages, as detailed below:
- superficial-white-matter (https://doi.org/10.5281/zenodo.11510179)
- *micapipe* (http://micapipe.readthedocs.io)
- *BrainSpace* (https://brainspace.readthedocs.io/)
- surface tools (https://github.com/kwagstyl/surface_tools)

## Dataset
### Participants 
- 10 healthy controls

### Imaging Data
- BigBrain
- Ahead brain: Bielschowsky and Parvalbumin stainings
- 7T MRI: T1-weighted structural scans, T1 relaxometry (T1 map), Magnetization transfer saturation (MTsat)

## Repository content
| Directories   | Description                                                                                                                                                                                                                                                                             |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`./scripts`]()      | `bash`, and `python` scripts for processing, and perform the analysis to reproduce the findings.                                                                                                                                                        |
| [`./data`]() | Data necessary to run the code.                                                                                                                                                                                                                      |

## Abstract
The superficial white matter (SWM), immediately beneath the cortical mantle, is thought to play a major role in cortico-cortical connectivity as well as large-scale brain function. Yet, this compartment remains rarely studied due to its complex structural organization. Our objectives were to develop and disseminate  a robust computational framework to study SWM organization based on 3D histology and high-field 7T MRI. Using data from the BigBrain and Ahead histology initiatives, we first interrogated variations in cell staining intensities across different cortical regions and different SWM depths. These findings were then translated to *in-vivo* 7T quantitative myelin-sensitive MRI, including T1 relaxometry (T1 map) and magnetization transfer saturation (MTsat). As indicated by the statistical moments of the SWM intensity profiles, the first 2 mm below the cortico-subcortical boundary were characterized by high structural complexity. We quantified SWM microstructural variation using a dimensionality reduction method and examined its relationship with brain geometry, as well as structural and functional connectivity. Our results showed correlations between brain curvature and SWM microstructural gradients derived from both myelin-sensitive MRI, and between functional connectivity and SWM microstructural gradients derived from T1-maps . This study provides novel insights into the organization of SWM in the human brain and underscores the potential of SWM mapping to advance fundamental and applied neuroscience research.
