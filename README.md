# ArcGIS_Classify
* ArcGIS_Classify is a Python-based Jupyter Notebook for ArcGIS Pro for quick and easy land-use classifications.
* This project was created as a final submission for the course "Python in QGIS and ArcGIS Pro" by Sven Harpering and Philippe Rieffel at Universität Münster.
* The authors are Jonas Starke and Kieran Galbraith. For questions, contact us at: jstarke@uni-muenster.de or k_galb01@uni-muenster.de.

## To-Do
* Installation guide: Implement an installation guide into the readme.
* Finish the "components" part of the readme.
  * The Input / Output part should maybe be moved to the installation guide.

## Installation
Download the ArcGIS Pro Project file and run it. It should open a Jupyter Notebook. Carefully read the instructions and follow the Step-by-Step Guide until you saved your own LULC. 

## Motivation
- Land use / land cover classifications have become increasingly important in geosciences in recent years.
  * Machine learning algorithms can understand non-linear relationships and make predictions.
- Often used to represent and monitor changes, such as climate change.
  * But still no simple method for laypeople with a step-by-step guide.
- Example:
  
  ![LULC Example](https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/isny_lulc_example.png)
  
  <sup>*Figure 1: Land use classification of the city of Isny im Allgäu after a model transfer with data from Versmold, NRW. Created in the course „Fernerkundung und maschinelle Lernverfahren“ by Hanna Meyer, created by Kieran Galbraith.*</sup>

## Components
This project consists of:
* A Python-based Jupyter Notebook that can be run using ArcGIS Pro.
* An intuitive UI with a user guide for quick and easy LULC.
  - Including provided example data and the possibility to use your own.
  - The example data include training data from Dortmund, an already finished model from Dortmund, and Sentinel-2 data from Münster.
      * Note that these files are only supposed to be examples; the training data from Dortmund were *not* scientifically created with groundtruthing.
* Ability to input data and fetch a PDF with the finished LULC.
  - Input:
    1. Training data.
    2. Sentinel-2 data from the area of training (AOT).
    3. Sentinel-2 data from the area of interest (AOI).
  - Output:
    1. Random forest-based model of the area of training.
    2. GeoTIFF or PDF file with the finished land-use classification of the area of interest.
* Example training data from Dortmund:

  ![Training Data Example](https://github.com/kgalb01/ArcGIS_Classify/blob/main/Examples/dortmund_data_example.png)

  <sup>*Figure 2: Screenshot of Dortmund training data as GeoJSON, visualized in geojson.io. Created as an example in the course „Geosoftware II“ by Edzer Pebesma & Christian Knoth, created by Kieran Galbraith.*</sup>
