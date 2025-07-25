# MDAnalysisWorkshop UCL 2024
Materials for the May 10, 2024 MDAnalysis workshop at University College London.

## Instructors

Richard Gowers - [@richardjgowers](https://github.com/richardjgowers)

Micaela Matta  - [@micaela-matta](https://github.com/micaela-matta)

Harry Lewin (Teaching Assistant)

## Location

#### Workshop Lectures and Tutorials:

G15 Public Cluster, DMS Watson Building  
University College London  
Gower Street, London, WC1E 6BT  
United Kingdom

See also [accessibility information](https://www.accessable.co.uk/ucl/access-guides/dms-watson-building-public-cluster-g15).

#### Coffee Breaks and Lunch:

Garden Room, Wilkins Building  
University College London  
Gower Street, London, WC1E 6BT  
United Kingdom

See also [accessibility information](https://www.accessable.co.uk/ucl/access-guides/wilkins-building-garden-room-meeting-room).

## Schedule

| Time (BST)    | Session                                                  | Materials                                                                                                                                                                |
|---------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 9:00-9:15     | Check-In/Registration                                    |   	                                                                                                                                                                      |
| 9:15-9:25     | Opening Remarks and Introductions	                       |   	                                                                                                                                                                      |
| 9:25-10:45    | **Session 1:** MDAnalysis Basics and System Manipulation | [Lecture 1](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1.0Day/blob/may24-ws/notebooks/Lecture1_MDAnalysisBasics.ipynb), [Tutorial 1](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1.0Day/blob/may24-ws/notebooks/Tutorial1_System_Manipulation.ipynb)                                                       	                                                                    |
| 10:45-11:10   | :coffee: break :coffee:          	                       |   	                                                                                                                                                                      |
| 11:10-12:30   | **Session 2:** Distances and Trajectories  	             | [Lecture 2](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1.0Day/blob/may24-ws/notebooks/Lecture2_Distance_calculations.ipynb), [Tutorial 2](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1.0Day/blob/may24-ws/notebooks/Tutorial2_Distances_Trajectories.ipynb)                                                                                                                         |
| 12:30-13:45   | Lunch                 	                                 |   	                                                                                                                                                                      |
| 13:45-15:05   | **Session 3:** Analysis Tools                            | [Tutorial 3](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial3_Analysis.ipynb)                                                |
| 15:05-15:30   | :coffee: break  :coffee:         	                       |   	                                                                                                                                                                      |
| 15:30-16:50   | **Session 4:**  Advanced Tips and Requests               | [Tutorial 4](https://github.com/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial4_Advanced.ipynb)                                                |
| 16:50-17:00   | Closing Remarks    	                                     |     	                                                                                                                                                                    |

## Setting up your Python environment *before the workshop*

<!--The workshop will be in a blended learning environment and hands-on. You will need a working installation of MDAnalysis and related packages including data to analyze in order to participate. The full installation may take up to about 1 GB of space (mostly for data, which you can delete after the workshop).--> 

Instructions for setting up your environment to run this workshop locally
are provided in [`INSTALL.md`](INSTALL.md).

A full list of the required Python packages can be seen inside [`environment.yml`](environment.yml).

As downloading and installing everything will take a little while, ideally you should follow these steps before the workshop starts. If you encounter any issues during installation, we can help!

**Note:** Materials may change between now and the time of the workshop, so while we ask you to install ahead of time, also make sure to `git pull` just prior to the start of the workshop.

## Google Colab

If for any reason you cannot set up a local environment with all required packages, you can use Google Colab to run all workshop notebooks directly from your browser, no installation required.

| Session                                                  | Materials                                                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Session 1:** MDAnalysis Basics and System Manipulation |[![MDA Part 1](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial1_System_Manipulation.ipynb)  	                                                                                                              |
| **Session 2:** Distances and Trajectories  	             | [![MDA Part 2](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial2_Distances_Trajectories.ipynb)                                                                                                               |
| **Session 3:** Analysis Tools                            | [![MDA Part 3](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial3_Analysis.ipynb)                                                                                                                                                                                 | 
| **Session 4:** Advanced Tips and Requests                | [![MDA Part 4](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisWorkshop-Intro1Day/blob/may24-ws/notebooks/Tutorial4_Advanced.ipynb)                                                                                                                                                                                 |

## Workshop pre-requisites

The workshop assumes that attendees have a working knowledge of [Jupyter notebooks][1], Python (especially the [NumPy library][2]), and the bash shell.

## Code of Conduct

All members of the MDAnalysis community and participants in MDAnalysis workshops are expected to abide by the MDAnalysis [Code of Conduct](https://www.mdanalysis.org/conduct/).

## License

Written materials are provided under the [CC-BY-4.0 SA license](LICENSE.md).

The MDAnalysis logo and its derivatives are licensed under the Creative Commons Attribution-NoDerivs 3.0 Unported License.

## Acknowledgements

Please see [`AUTHORS.md`](AUTHORS.md) for a list of contributors to the workshop materials.

We would like to give a special thanks to our partners for this workshop, the [Thomas Young Centre](https://thomasyoungcentre.org/), the [JCMaxwell Node of CECAM](https://uk-jcmaxwell.cecam.org/), and [CCPBioSim](https://www.ccpbiosim.ac.uk/).

<img
src="/logos/TYC_Logo.png"
title="Thomas Young Centre Logo" alt="Thomas Young Centre Logo"
style="float: left; height: 5em; " />

<img
src="/logos/CECAM_UK_JCMAXWELL.jpg"
title="JCMaxwell Node of CECAM Logo" alt="JCMaxwell Node of CECAM Logo"
style="float: left; height: 5em; " />

<img
src="/logos/CCPBioSim_Logo.jpeg"
title="CCPBioSim Logo" alt="CCPBioSim Logo"
style="float: left; height: 5em; " />

This workshop has been made possible in part by a [grant](https://chanzuckerberg.com/eoss/proposals/mdanalysis-outreach-and-project-manager/) from the Chan Zuckerberg Initiative DAF, a donor advised fund of Silicon Valley Community Foundation (funder DOI 10.13039/100014989). MDAnalysis also thanks NumFOCUS for its continued support as our fiscal sponsor.

<img
src="/logos/CZI_Logo.jpg"
title="Chan Zuckerberg Initiative Logo" alt="Chan Zuckerberg Initiative Logo"
style="float: left; height: 5em; " />

<img
src="/logos/numfocus-sponsored.png"
title="NumFOCUS Sponsored Project Logo" alt="NumFOCUS Sponsored Project Logo"
style="float: left; height: 5em; " />

##
[1]: https://jupyter-notebook.readthedocs.io/en/stable/
[2]: https://numpy.org/
