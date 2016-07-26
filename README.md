#QGIS documentation

Reference for installation and initial setup of QGIS for analysis of biodiversity. This documentation was created as part of my co-op at the Academy of Natural Sciences and is intended to be a guide for installing QGIS for the first time. It is intended to be a guide to setup QGIS for the first time and begin to use it for studying biodiversity of landsnails in Jamaica as part of ongoing research at ANSP.

###Installation 
------
The most recent version of QGIS can be obtained from their website here: http://qgis.org/en/site/forusers/download.html Once you have selected the correct OS and version it will ask to download. This normally takes 5 - 10 minutes to complete. If using a Windows computer, simply click the file after the download is finished and follow the prompts to install. You may need administrator priviledges to complete this step.

When the installation is finished, you can open QGIS Desktop and begin to use the software immediately. For troubleshooting and reference, the most up to date documentation can always be found online here: http://qgis.org/en/docs/index.html 

If this is the first time you have used GIS software or are unfamiliar with the program, a beginner's guide to GIS is produced by the QGIS project and found online here: http://docs.qgis.org/2.8/en/docs/gentle_gis_introduction/

Once you are comfortable with the basics, the QGIS user guide can be found online here: http://docs.qgis.org/2.8/en/docs/index.html

###Data Preparation
------

In order to get started using QGIS, data needs to be correctly prepared to be opened in the program. Data can be opened from other GIS programs or projected from Excel.

Viewing a map or points in QGIS:

- In this respository are several datasets ready to be used in QGIS as examples. Landuse.zip, soil_erosion.zip, and soil_textures.zip can be downloaded and opened in QGIS. 

- After downloading the zip folder, open QGIS and go to Layer > Add Layer > Add Vector Layer. Browse to the downloaded zip file and click Open. 

- You should now see an image of Jamaica. The layer will probably only show one color at first. To view more information, right click the layer name in the menu, and select "Properties" from the dropdown.

- A new window will open up with settings for labels, attributes, and more. Click on "Style" on the left and you will be able to change how the layer looks in QGIS.

- To color the map based on the data, click on the dropdown at the top that says "Single Symbol". Select Catergorized instead.

- Now click on the column dropdown and select the values you want to use for coloring the map. For example, in the landuse layer you would select LU_98 from the dropdown.

- Before QGIS will change the colors, you must add these values by selecting "Classify" at the bottom of the window. This will add all the values into QGIS and show you what colors match what data. Click "OK" to view the new map colors.

------

Viewing Excel files with coorinates in QGIS:

- To open Excel files in QGIS, save the Excel file as a .csv file.

- After saving, open QGIS and go to Layer > Add Layer > Add Delimited Text Layer

- This will open a new window to open the .csv file with. Use the "Browse" button to find the correct file, and select the fields to be used for the X and Y coordinates. Once it is ready, click "OK" to open the file as points in QGIS.

- The new points will show up as a layer in QGIS like other data, and can be colored, searched, and labeled using the tools in this guide and online.

###Examples
------

Search by attributes: 

QGIS can be used to display stations based on their species or number of species. In order to do this, you will need to add a layer with columns for the number of species and which species are present at each site. Then use the built in search tools to highlight stations that match your questions. 

- An example using search to find capital cities around the world can be found here: http://www.qgistutorials.com/en/docs/working_with_attributes.html

Change labels: 

QGIS can show labels for each site designed by you. Download the weather_stations.zip file in this repository to use for a simple example on using labels.

- In QGIS, go to Layer > Add Layer > Add Vector Layer. Browse to the downloaded weather_stations.zip file and click Open. This is based on the information from the user guide, found here: http://docs.qgis.org/2.0/en/docs/training_manual/vector_classification/label_tool.html 

- Weather stations should be loaded into QGIS now.

- Go to View > Toolbars > Label and make sure it is checked. If not, check the box next to Label to activate. 

- Go to the Label toolbar and click the yellow tag. If you hover the mouse over the tag it will say "Layer Labeling Options." 

- A new window will open for Label Settings. At the top will be a small box next to "Label this layer with". Click this box to activate labels and begin to make changes to them. In the dropdown box you should select the data that will be used to make the labels. You can use site names, amount of precipitation for that month, or any other data stored in the layer.

- In this window, it is now possible to change the position of labels, make them only show if the map is zoomed in, change their background image or color, and change the text size. For more examples of making labels, use the link above.

###Data Analysis
------
While QGIS has many useful functions built it, it can be extended through programs like Python and R. QGIS has a native console for Python and can be configured to run R scripts as well. This section describes how to get started using these programs in QGIS.

To install both Python and R, it is recommended to begin using Anaconda. The most recent version of Anaconda can be found here: https://www.continuum.io/downloads This is a simple way to install Python and several packages relevant to data science and analysis. Once the correct version has been selected, it will download to the computer. Windows users can simply click the file to begin installation. This may require administrator priviledges to complete this step. 

Once Anaconda is finished installing, Python can be run directly as a program from the start menu. For help using Python with QGIS refer to here: http://docs.qgis.org/testing/en/docs/pyqgis_developer_cookbook/intro.html

R can be installed directly from https://www.r-project.org/ or by using Anaconda from above. If Anaconda has been installed on the computer, open the program "Anaconda Prompt" and type "conda install -c r r-essentials" into the terminal. This should install R and all the packages necessary for basic analysis.

Once R is installed onto the computer, it is recommended to also install the program RStudio found here: https://www.rstudio.com/products/rstudio/download/ RStudio improves the interface of R and makes it easier to use for new users.

To use Python in QGIS, simply launch the Python console while using QGIS by seleting Plugins - Python. This will launch a window within QGIS to write and execute Python scripts from.

To use R in QGIS, the best practice is to use RStudio for data analysis and preparation and then to import the results into QGIS for viewing. 

###Examples
------
Python can be run directly from the console within QGIS. There are many examples of how to use Python for GIS online and on the QGIS website. A good introduction to Python for QGIS can be found here: 
http://www.qgistutorials.com/en/docs/getting_started_with_pyqgis.html This exercise will walk you through using Python to export a list of stations with meta about those locations.

This is a similar example using the Jamaican dataset weather_stations.zip

- In QGIS, go to Layer > Add Layer > Add Vector Layer. Browse to the downloaded weather_stations.zip file and click Open.

- Weather stations should be loaded into QGIS now.

- Using the identify tool, you can select any point to see the attribute table. After selecting a point with the identify tool, a window will pop up showing all available fields for that point. Select "Feature Form" either from the window toolbar or under the Actions menu to see data for those fields.

- Now open the Python console using Plugins > Python Console

- The Python console will open a window with a prompt >>> at the bottom. To use Python in QGIS we use the "iface" variable. Here we can access the current layer and store it as a layer variable using `layer = iface.activeLayer()`

- If you get confused or want to know more about a function in Python, you can use dir() to get more information. For example, type `dir(layer)` to see the operations available for layer.

- For this example, we want to get the reference for features at each point. To do this type 

```python
for f in layer.getFeatures():
  print f
```
  
- These are two seperate lines in the console, and the second line should include the two spaces before typing. This will iterate through each feature and print them out in the console.

- Modifying the above code, we can quickly view the annual rainfall at each station. Type in 

```python
for f in layer.getFeature()
  print f['Station_Na'], ['Ann]
```
  
- The variables to print must be surrounded by quotations for Python to understand them. The names came from the attribute table we identified earlier. Try changing the variables to view the height or parish instead.

- Now that we know how to find features using Python, we can use it to find coordinates. This is done using the geometry() function and stores the values in the variable geom. Type this into the console 

```python
for f in layer.getFeatures():
  geom = f.geometry()
  print geom.asPoint()
```
  
- Using the functions we have learned so far, we can now export this information to a text file using Python. Enter into the console
 
```python
for f in layer.getFeatures():
  geom = f.geometry()
  print '%s, %s, %s' % (f['Station_Na'], f['Parish'], geom.asPoint())
```
  
- Once you have confirmed this is working as intended, we can open up a new file and export the data to there. To do this, simple replace the file path with your own and type this into the console:

```python
output_file = open('c:/Users/Vincent/Desktop/weather.txt', 'w')
for f in layer.getFeatures():
  geom = f.geometry()
  line = '%s, %s, %s\n' % (f['Station_Na'], f['Parish'], geom.asPoint())
  unicode_line = line.encode('utf-8')
  output_file.write(unicode_line)
output_file.close()
```

- You can now open the text file and view the data for the stations we just extracted using Python in QGIS.

------

RStudio can perform many complex analyses and be used to create maps viewable in QGIS. An introduction to using R for GIS and its limitations and advantages can be found here: http://www.r-bloggers.com/r-an-integrated-statistical-programming-environment-and-gis/

Another interesting example for R can be found http://spatialanalysis.co.uk/2013/04/analysis-visualisation-spatial-data/

A great beginner's guide to R I use is http://swirlstats.com/ It is downloaded as a package for R and teaches you how to use R through interactive examples.