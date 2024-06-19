# MDAnalysis/MolSSI Workshop at Arizona State University 2024
Materials for the June 24-25, 2024 [MDAnalysis/MolSSI workshop](https://www.mdanalysis.org/2024/05/14/ASUworkshop/) at [Arizona State University](https://www.asu.edu/) (ASU).

## Instructors
Irfan Alibay - [@IAlibay](https://github.com/IAlibay)  
Oliver Beckstein - [@orbeckst](https://github.com/orbeckst)    
Sam Ellis - [@sjayellis](https://github.com/sjayellis)    
Mike Henry - [@mikemhenry](https://github.com/mikemhenry)    
Ian Kenney - [@ianmkenney](https://github.com/ianmkenney)   
Fiona Naughton - [@fiona-naughton](https://github.com/fiona-naughton)   
Ashley Ringer-Macdonald - [@armcdona](https://github.com/armcdona)   
Yuxuan Zhuang - [@yuxuanzhuang](https://github.com/yuxuanzhuang)    

## Location

#### Workshop Lectures and Tutorials:

Room PSF 186, [Physical Sciences F Building](https://maps.app.goo.gl/b2kKhEBdvdvS2M3h9)  
Department of Physics  
Arizona State University  
550 E Tyler Mall, PSF 186  
Tempe, AZ 85287  
USA

## Schedule
### Day 1, June 24th
| Time (MST)    | Session                                                  | Materials                                                                                                                   |
|---------------|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 08:00-09:00   | Breakfast and Check-In/Registration                      |   	                                                                                                                         |
| 09:00-09:15   | Introduction                    	                       | [Introduction Slides](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/June%202024%20MDAnalysis-MolSSI%20Workshop%20Introduction%20Slides.pdf)                                	                                                                                                                         |
| 09:15-10:05   | Introduction to MDAnalysis: Atoms                        | [Lecture 1](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Lecture1_MDAnalysisBasics.ipynb), [Tutorial 1](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial1_System_Manipulation.ipynb)                                                                                                                            |
| 10:05-11:00   | Introduction to MDAnalysis: Dynamics                     | [Lecture 2](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Lecture2_Distance_calculations.ipynb), [Tutorial 2](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial2_Distances_Trajectories.ipynb)                                                                                                                              |
| 11:00-11:15   | Break                            	                       |   	                                                                                                                         |
| 11:15-12:05   |  MDAnalysis: Analysis                     	             | [Tutorial 3](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial3_Analysis.ipynb)                                                                                |
| 12:05-12:45   |  MDAnalysis: Advanced Tips and Tricks            	       | [Tutorial 4](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial4_Advanced.ipynb)                                                                                |
| 12:45-13:00   | Introduction to MDAKits                                  |                                                                                                                             |
| 13:00-14:00   | Lunch                 	               |   	                                                                                                                         |
| 14:00-14:30   | Introduction to the Bash Shell                           | [Software Carpentry Tutorial](https://swcarpentry.github.io/shell-novice/), [MolSSI Command Line Basics Lesson](https://education.molssi.org/python-package-best-practices/00-command-line-basics.html)                                                                                                                 |
| 14:30-15:30   | Version Control I               	                       | [MolSSI git and GitHub Lessons](https://education.molssi.org/python-package-best-practices/index.html#git-and-github)  	   |
| 15:30-15:45   | Break                            	                       |   	                                                                                                                         |
| 15:45-16:45   | Version Control II               	                       | [MolSSI git and GitHub Lessons](https://education.molssi.org/python-package-best-practices/index.html#git-and-github)  	   |
| 16:45-17:00   | Break                            	                       |   	                                                                                                                         |
| 17:00-18:30   | Python Packaging                	                       | [MolSSI Python Package Set-Up Lesson](https://education.molssi.org/python-package-best-practices/01-package-setup.html)  	 |

### Day 2, June 25th
| Time (MST)    | Session                                                  | Materials                                                                                                                   |
|---------------|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 08:00-09:00   | Breakfast and Check-In/Registration                      |   	                                                                                                                         |
| 09:00-10:45   | Testing and pytest               	                       | [MolSSI Continuous Integration, Testing, Distribution Lessons](https://education.molssi.org/python-package-best-practices/index.html#continuous-integration-testing-distribution)             	                                                                                                                         |
| 10:45-11:00   | Break                            	                       |   	                                                                                                                         |
| 11:00-12:30   | Documentation                              	             | [MolSSI Code Style and documentation Lessons](https://education.molssi.org/python-package-best-practices/index.html#code-style-and-documentation)                                                                                                                                                                                 |
| 12:30-13:30   | Lunch                 	                                 |   	                                                                                                                         |
| 13:30-13:40   | Hackathon Introduction                                   |                                                                                                                             |
| 13:40-15:30   | [Hackathon](#hackathon)                    	             | [Hackathon Directory](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/tree/jun24-ws/hackathon)      |
| 15:30-15:45   | Break                            	                       |   	                                                                                                                         |
| 15:45-17:15   | [Hackathon](#hackathon)                    	             | [Hackathon Directory](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/tree/jun24-ws/hackathon)      |
| 17:15-17:45   | Hackathon Wrap-Up and Showcase             	             |   	                                                                                                                         |
| 17:45-18:00   | Closing Remarks                            	             |   	                                                                                                                         |

## Setting up your Python environment *before the workshop*

<!--The workshop will be in a blended learning environment and hands-on. You will need a working installation of MDAnalysis and related packages including data to analyze in order to participate. The full installation may take up to about 1 GB of space (mostly for data, which you can delete after the workshop).--> 

Instructions for setting up your environment to run this workshop locally
are provided in [`INSTALL.md`](INSTALL.md).

A full list of the required Python packages can be seen inside [`environment.yml`](environment.yml).

As downloading and installing everything will take a little while, ideally you should follow these steps before the workshop starts. If you encounter any issues during installation, we can help!

**Note:** Materials may change between now and the time of the workshop, so while we ask you to install ahead of time, also make sure to `git pull` just prior to the start of the workshop.

## Google Colab

If for any reason you cannot set up a local environment with all required packages, you can use Google Colab to run all workshop notebooks directly from your browser, no installation required.                                                       
| Tutorial                                                                | Materials                                                                                                                    |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Tutorial 1:** Loading and Manipulating your Molecular Simulation Data | [![MDA Part 1](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial1_System_Manipulation.ipynb)  	                                           |
| **Tutorial 2:** Positions, Distances and Trajectories  	                | [![MDA Part 2](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial2_Distances_Trajectories.ipynb)                                           |
| **Tutorial 3:** Analysis Tools                                          | [![MDA Part 3](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial3_Analysis.ipynb)                                                         |
| **Tutorial 4:** Advanced Universe Creation and Attributes               | [![MDA Part 4](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial4_Advanced.ipynb)                                                         |

## Connecting to the Wireless Network/Wifi

* The **asu guest** wireless network is *available to all participants* but limited in capabilities.
* The **eduroam** network is available to anyone whose institution participates in [eduroam](https://eduroam.org/). If you need to set up anything, talk to your institution's IT support *before* coming to ASU.
* The **asu** network is only available to members of Arizona State University.


### "asu guest" network

Full instructions for connecting to the **asu guest** wireless network can be found in [`connecting-to-the-asu-wifi.pdf`](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/connecting-to-the-asu-wifi.pdf). You will need a means to read email or receice text messages because as part of the registration process, a code will be sent to you.

*The "asu guest" network is bandwidth-limited. Make sure that you [install the workshop environment](INSTALL.md) before coming to ASU.*


### eduroam

Provide your institution credentials. See https://eduroam.org/ and your institution's documentation for how to set up.


## Workshop pre-requisites

The workshop assumes that attendees have a working knowledge of [Jupyter notebooks][1] and Python (especially the [NumPy library][2]). For a better idea of things participants should be comfortable doing in Python or to freshen up on your skills, please have a look at the MolSSI lesson, “[Python Scripting for Computational Molecular Science](https://education.molssi.org/python_scripting_cms/)”.

## Hackathon

The hackathon will be held on the second day of the workshop. We encourage you to start thinking about what you want to work on early. More information and ideas can be found in the [hackathon directory](./hackathon).

## Code of Conduct

All members of the MDAnalysis community and participants in MDAnalysis workshops are expected to abide by the MDAnalysis [Code of Conduct](https://www.mdanalysis.org/pages/conduct/).

## License

Written materials are provided under the [CC-BY-4.0 SA license](LICENSE.md).

## Acknowledgements

Please see [`AUTHORS.md`](AUTHORS.md) for a list of contributors to the workshop materials.

We would like to give a special thanks to our partner for this workshop, the [Molecular Sciences Software Institute](https://molssi.org/) (MolSSI).

<img
src="/logos/MolSSI_Logo.png"
title="Molecular Sciences Software Institute Logo" alt="Molecular Sciences Software Institute Logo"
style="float: left; height: 5em; " />

This workshop has been made possible in part by a [grant](https://chanzuckerberg.com/eoss/proposals/mdanalysis-outreach-and-project-manager/) from the Chan Zuckerberg Initiative (CZI) DAF, a donor advised fund of Silicon Valley Community Foundation (funder DOI 10.13039/100014989). MDAnalysis also thanks NumFOCUS for its continued support as our fiscal sponsor.

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
