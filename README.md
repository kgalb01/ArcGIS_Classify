<p>
  <img src="https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/arcgis_classify_logo.jpg" alt="Logo" width="200">
</p>

<sup>*Figure 0: Logo for the project "ArcGIS_Classify", created with Adobe Firefly*</sup>

# ArcGIS_Classify

*ArcGIS_Classify* is a Python-based Jupyter Notebook designed for quick and easy land-use classification.

This project was created as a final submission for the course "Python in QGIS and ArcGIS Pro" by Sven Harpering and Philippe Rieffel at Universität Münster.

The authors are Jonas Starke and Kieran Galbraith. For questions, contact us at: jstarke@uni-muenster.de or k_galb01@uni-muenster.de.

## Installation

* Download the .zip file containing all necessary data.
* Open the Jupyter Notebook ("arcgis_classify.ipynb") in VS Code.
  * Make sure to use the ArcGIS Pro Python Kernel! For a tutorial, visit:
  * https://resources.esri.ca/getting-technical/how-to-configure-visual-studio-code-with-arcgis-pro-s-python-environment
  * The app has only been tested on this kernel! We can't guarantee that it will work properly on other kernels.
  
  ![VS Example](https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/vs_example.jpg)

  <sup>*Figure 1: Screenshot from VS Code showing the correct kernel in use*</sup>

* Carefully read the instructions and follow the step-by-step guide until you have saved your own LULC.
* Note: As the .TIF files are too big to upload to GitHub you can follow this download link to use our example data: [Google Drive](https://drive.google.com/drive/folders/1HW2gjHiq84SYiR2ubveufqxe7iAKiQy9?usp=sharing)


## Motivation

Land use/land cover classifications have become increasingly important in geosciences in recent years.

* Machine learning algorithms can understand non-linear relationships and make predictions.
* These classifications are often used to represent and monitor changes, such as those related to climate change.
* However, there is still no simple method for laypeople that includes a step-by-step guide.

Example:

![LULC Example](https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/isny_lulc_example.png)

<sup>*Figure 2: Land use classification of the city of Isny im Allgäu after a model transfer with data from Versmold, NRW. Created in the course "Fernerkundung und maschinelle Lernverfahren" by Hanna Meyer, created by Kieran Galbraith.*</sup>

## Components

This project consists of:

* A Python-based Jupyter Notebook that can be run using VS Code.
* An intuitive UI with a user guide for quick and easy LULC.
  - Includes provided example data and the option to use your own data.
  - The example data include training data from Dortmund, an already finished model from Dortmund, and Sentinel-2 data from Münster or Stuttgart.
    * Note that these files are only intended as examples; the training data from Dortmund were *not* scientifically created with ground truthing.
* The ability to input data and generate a PDF with the finished LULC.
  - Input:
    1. Training data.
    2. Sentinel-2 data from the area of training (AOT).
    3. Sentinel-2 data from the area of interest (AOI).
  - Output:
    1. Random forest-based model of the area of training.
    2. GeoTIFF or PDF file with the finished land-use classification of the area of interest.

Example training data from Dortmund:

![Training Data Example](https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/dortmund_data_example.png)

<sup>*Figure 3: Screenshot of Dortmund training data as GeoJSON, visualized in geojson.io. Created as an example in the course "Geosoftware II" by Edzer Pebesma & Christian Knoth, created by Kieran Galbraith.*</sup>

## Conclusion
In the past few months, we have worked extensively on machine learning for spatial prediction models, mostly using R. R offers several ready-to-use packages for machine learning that are easy to apply to your data. We had a lot of fun with spatial prediction models, which motivated us to explore this field further with this project.

To summarize, some parts of the project were a lot of fun, while others took us hours or even days to figure out. For example, creating a very basic UI was enjoyable, but integrating remote sensing data into the Python environment was much more challenging than expected, especially because there is practically no way to incorporate .grd files. 

We are satisfied with the models created through the project, but for some reason, the final predictions look terrible. Interestingly, when we used our models in R, the prediction results were fine. 

In conclusion, while machine learning works well in Python and has some advantages over R, we found R to be faster and (at least for us) easier to handle at this point.

## Bugs

Here is a list of known bugs that we are actively working to fix:

* This project was initially planned as a plugin for ArcGIS Pro, but this turned out to be too complex at the moment.
  * We then planned to use the Jupyter Notebook in ArcGIS Pro, but encountered numerous issues with some modules that couldn't be installed or loaded, especially those related to the UI.
  * As a result, we are currently using VS Code, as it consistently works.
* .grd files cannot be inserted into the Jupyter Notebook.
* Some rasterdata just doesn't seem to work. We tried using Sentinel-2 Data for the Fiji Islands and we never got it working
* Clicking "Yes" on "4.2.2" for the question "Is your Area of Training (the region where your training data are located) the same as your Area of Interest?" doesn't work yet. We recommend clicking "No" and selecting the same .TIF file again if you encounter issues.

## Links

Are you interested in starting your own projects? Here are some links that helped us out, in no particular order! Please note that this list is far from complete:

* Harpering, Sven & Rieffel, Phillipe: Seminar slides. Python in QGIS and ArcGIS. SoSe 2024.
* Meyer, Hanna: Lecture slides. Fernerkundung und maschinelle Lernverfahren zur flächendeckenden Erfassung von Umweltvariablen. WiSe 2021-22.
* https://www.geeksforgeeks.org/visualizing-tiff-file-using-matplotlib-and-gdal-using-python/
* https://github.com/MasoumehVahedi/Random_Forest_LandUse_LandCover_Classification-/blob/main/Random%20Forest%20Land%20cover%20Classification.ipynb
* https://www.youtube.com/watch?v=r002WD_Ui8g
* https://matplotlib.org/stable/users/explain/colors/colormaps.html#overview
* https://github.com/rasterio/rasterio
* https://github.com/rasterio/rasterio/issues/1547
* https://scikit-learn.org/stable/
* https://stackoverflow.com/questions/24458645/label-encoding-across-multiple-columns-in-scikit-learn
* https://gist.github.com/pb111/88545fa33780928694388779af23bf58
* https://github.com/ludwig-ai/ludwig/blob/master/ludwig/utils/visualization_utils.py
* https://docs.python.org/3/library/os.path.html
* https://stackoverflow.com/questions/11328958/save-multiple-plots-in-a-single-pdf-file
* ...and *a lot* of YouTube tutorials and trial and error.
