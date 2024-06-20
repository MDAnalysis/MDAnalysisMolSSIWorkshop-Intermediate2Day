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
| 09:15-10:05   | Introduction to MDAnalysis: Atoms                        | [Lecture 1](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Lecture1_MDAnalysisBasics.ipynb), [Tutorial 1](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial1_System_Manipulation.ipynb)                                                                    |
| 10:05-11:00   | Introduction to MDAnalysis: Dynamics                     | [Lecture 2](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Lecture2_Distance_calculations.ipynb), [Tutorial 2](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial2_Distances_Trajectories.ipynb)                                                                 |
| 11:00-11:15   | Break                            	                       |   	                                                                                                                         |
| 11:15-12:05   | MDAnalysis: Analysis                     	               | [Tutorial 3](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial3_Analysis.ipynb) |
| 12:05-12:45   | MDAnalysis: Advanced Tips and Tricks            	       | [Tutorial 4](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Tutorial4_Advanced.ipynb) |
| 12:45-12:55   | Introduction to MDAKits                                  |                                                                                                                             |
| 12:55-13:05   | Group Photo                                              |                                                                                                                             |
| 13:05-14:00   | Lunch                                    	               |   	                                                                                                                         |
| 14:00-14:30   | Introduction to the Bash Shell                           | [Software Carpentry Tutorial](https://swcarpentry.github.io/shell-novice/), [MolSSI Command Line Basics Lesson](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Command_Line.md)                                                                                                                 |
| 14:30-16:00   | Python Packaging                	                       | [MolSSI Python Package Set-Up Lesson](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Python_Packaging.md)  	 |
| 16:00-16:15   | Break                            	                       |   	                                                                                                                         |
| 16:15-18:15   | Version Control                  	                       | [MolSSI git and GitHub Lessons](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Version_Control.md)  	   |

### Day 2, June 25th
| Time (MST)    | Session                                                  | Materials                                                                                                                   |
|---------------|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 08:00-09:00   | Breakfast and Check-In/Registration                      |   	                                                                                                                         |
| 09:00-10:45   | Testing and pytest               	                       | [MolSSI Testing Lessons](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Testing.md)             	                                                                                                                                                                             |
| 10:45-11:00   | Break                            	                       |   	                                                                                                                         |
| 11:00-12:30   | Documentation                              	             | [MolSSI Documentation Lessons](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/notebooks/Documentation.md) |
| 12:30-13:30   | Lunch                 	                                 |   	                                                                                                                         |
| 13:30-13:40   | Hackathon Introduction                                   |                                                                                                                             |
| 13:40-15:30   | [Hackathon](#hackathon)                    	             | [Hackathon Directory](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/tree/jun24-ws/hackathon)      |
| 15:30-15:45   | Break                            	                       |   	                                                                                                                         |
| 15:45-17:15   | [Hackathon](#hackathon)                    	             | [Hackathon Directory](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/tree/jun24-ws/hackathon)      |
| 17:15-17:45   | Hackathon Wrap-Up and Showcase             	             |   	                                                                                                                         |
| 17:45-18:00   | Closing Remarks                            	             |   	                                                                                                                         |

## Hackathon

The hackathon will be held on the second day of the workshop. We encourage you to start thinking about what you want to work on early. More information and ideas can be found in the [hackathon directory](./hackathon).

## Setting up your Python Environment *Before the Workshop*

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

## Asking Questions *Before and During the Workshop*

The primary communication channel for asking questions and having relevant discussions for this workshop will be the [MDAnalysis Discord server](https://discord.com/channels/807348386012987462/). To join the server, use the invitation link, [https://discord.gg/dMQWjNcZmh](https://discord.gg/dMQWjNcZmh). If you are new to Discord, [here are some resources](https://support.discord.com/hc/en-us/categories/115000217151) to help you get started.

Once you join the server, you will see a “ASU WORKSHOP 2024” category. Start exploring the specific channels and read their descriptions to get used to the organization. You are welcome to introduce yourself in the `#general` channel and start asking any workshop-related questions in the `#questions` forum. Unfortunately Discord is limited in its ability to collapse the post titles posted in the `#questions` and `#hackathon` forums, so a workaround is to mute these channels (a post should show again if someone updates it).

## Connecting to the Wireless Network/Wifi

* The **asu guest** wireless network is *available to all participants* but limited in capabilities.
* The **eduroam** network is available to anyone whose institution participates in [eduroam](https://eduroam.org/). If you need to set up anything, talk to your institution's IT support *before* coming to ASU.
* The **asu** network is only available to members of Arizona State University.

### "asu guest" network

Full instructions for connecting to the **asu guest** wireless network can be found in [`connecting-to-the-asu-wifi.pdf`](https://github.com/MDAnalysis/MDAnalysisMolSSIWorkshop-Intermediate2Day/blob/jun24-ws/connecting-to-the-asu-wifi.pdf). You will need a means to read email or receive text messages because as part of the registration process, a code will be sent to you.

*The "asu guest" network is bandwidth-limited. Make sure that you [install the workshop environment](INSTALL.md) before coming to ASU.*

### eduroam

Provide your institution credentials. See https://eduroam.org/ and your institution's documentation for how to set up.

## Workshop Pre-Requisites

The workshop assumes that attendees have a working knowledge of [Jupyter notebooks][1] and Python (especially the [NumPy library][2]). For a better idea of things participants should be comfortable doing in Python or to freshen up on your skills, please have a look at the MolSSI lesson, “[Python Scripting for Computational Molecular Science](https://education.molssi.org/python_scripting_cms/)”.

## Code of Conduct

All members of the MDAnalysis community and participants in MDAnalysis workshops are expected to abide by the MDAnalysis [Code of Conduct](https://www.mdanalysis.org/pages/conduct/).

## Health and Safety
We are committed to providing a safe, comfortable, and healthy environment for the workshop and have looked to local and international entities and other organizations in the open source community to develop onsite safety measures for workshop attendees.

### Testing
A limited number of rapid self-tests will be made available at check-in for those who would like to test themselves for COVID-19 during the meeting.

**Testing Positive for COVID-19**

*Individuals who are COVID-positive should not attend the workshop.* If you receive a positive COVID-19 test result during the workshop, please [notify the workshop organizing committee][workshop_email] and do not return to the event while you are still COVID-positive.

* We will treat any information about your testing status as confidential. (If you want to notify any of your contacts you may, of course, do so yourself.)
* We will announce to attendees if we are made aware of anyone testing positive for SARS-Cov-2 so that all attendees and instructors are put in a position to make choices that are right for them and their exposure risk level.

### Face Coverings
Face coverings are not required, but are welcomed. We view face coverings as a personal choice and will support attendees in their choice to wear or not to wear a face covering.

## Fire Safety
Follow the instructions given at the workshop.


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

[workshop_email]: mailto:workshops@mdanalysis.org
