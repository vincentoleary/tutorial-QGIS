#QGIS documentation

Reference for installation and initial setup of QGIS for analysis of biodiversity. This documentation was created as part of my co-op at the Academy of Natural Sciences and is intended to be a guide for installing QGIS for the first time.

Installation 

> The most recent version of QGIS can be obtained from their website here: http://qgis.org/en/site/forusers/download.html Once you have selected the correct OS and version it will ask to download. This normally takes 5 - 10 minutes to complete. If using a Windows computer, simply click the file after the download is finished and follow the prompts to install. You may need administrator priviledges to complete this step.

> When the installation is finished, you can open QGIS Desktop and begin to use the software immediately. For troubleshooting and reference, the most up to date documentation can always be found online here: http://qgis.org/en/docs/index.html 

> If this is the first time you have used GIS software or are unfamiliar with the program, a beginner's guide to GIS is produced by the QGIS project and found online here: http://docs.qgis.org/2.8/en/docs/gentle_gis_introduction/

> Once you are comfortable with the basics, the QGIS user guide can be found online here: http://docs.qgis.org/2.8/en/docs/index.html This is available as a pdf version in this repository for quick reference.

Data Preparation

> 

Data Analysis

> While QGIS has many useful functions built it, it can be extended through programs like Python and R. QGIS has a native console for Python and can be configured to run R scripts as well. This section describes how to get started using these programs in QGIS.

>> To install both Python and R, it is recommended to begin using Anaconda. The most recent version of Anaconda can be found here: https://www.continuum.io/downloads This is a simple way to install Python and several packages relevant to data science and analysis. Once the correct version has been selected, it will download to the computer. Windows users can simply click the file to begin installation. This may require administrator priviledges to complete this step. 

>> Once Anaconda is finished installing, Python can be run directly as a program from the start menu. For help using Python with QGIS, a pdf manual from QGIS is available in this repository for quick reference and cane be found online here: http://docs.qgis.org/testing/en/docs/pyqgis_developer_cookbook/intro.html

>> R can be installed directly from https://www.r-project.org/ or by using Anaconda from above. If Anaconda has been installed on the computer, open the program "Anaconda Prompt" and type "conda install -c r r-essentials" into the terminal. This should install R and all the packages necessary for basic analysis.

>> Once R is installed onto the computer, it is recommended to also install the program RStudio found here: https://www.rstudio.com/products/rstudio/download/ RStudio improves the interface of R and makes it easier to use for new users.

> To use Python in QGIS, simply launch the Python console while using QGIS by seleting Plugins - Python. This will launch a window within QGIS to write and execute Python scripts from.

> To use R in QGIS, the best practice is to use RStudio for data analysis and preparation and then to import the results into QGIS for viewing. 