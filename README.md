# Metpetools

After various decades of digital transition, publishing and spreading of geo-data actually is exclusively with Web and internet channels. Everybody know the effective communication and easy to access to the data and maps using web or mobile devices. The last decade of web-development and expecially web-gis technology development provided a very number of projects and libraries (OpenLayers, LeafLet etc..) for a better "production process" of geo-data publication on the web. Today especially in Opensource community we have a several front-end project that offer possibility to develop effective interface for data publishing on the web and mobile devices.

Geoscientists have a multitude of digital data across scales, across geometric types, across dataset types and more, such as Geo-graphic data, Geo-spatial data and Microscale-data.

**Metpetools** is a set of Python tools to create web-viewers of geological data provided from different type of analysis. A frist version of this project provided a multiscale web publication process for the site of Palmi shear zone  (Italy). A complex web-GIS viewer that contain different type of data at different scale: from microstructural data of thin section provided in a LIS-viewer (Litologic Information Sistem), a 3D model viewer of outcrops.
___

Actual version proposed is used in:

Di Pietro, G., D’Agostino, A., Ortolano, G., Fazio, E., Visalli, R., Musumeci, R.E., Cirrincione, R., 2024. Web publication of multiscale geological data, methodology, and processes. [DOI: 10.13140/RG.2.2.34955.50726](https://doi.org/10.13140/RG.2.2.34955.50726) (keynote available)

---

### Table of contents

1. Making a Web viewer of a "Thin section" (LIS) from data
2. Web viewer of a 3D model from KMZ file
3. Pakaging all into a web-gis framwork

---

# Making a Web viewer of a "Thin section" (LIS) from data

**We recomend use Jupyter notebook version** [shp2html.ipynb](notebook/shp2html.ipynb)

## Jump to:

- [Qgis Desktop](#1-using-on-a-qgis-desktop-as-custom-script)
- [Esri ArcGis](#2-using-inside-esri-arcgisproarcmap-applications)
- [Python/Notebook](#3-using-via-jupyter-notebook)
- [KMZ to HTML script GUI](Standalone_GUI/Readme.md)

## 1. Using on a Qgis desktop as custom script

1. Download [shp2html_qgis.py](shp2html_qgis.py) file
2. Open Qgis in your desktop
3. Go to menù Plugin -> Console Python

<div style="text-align:left"><img src="./Qgis%20processing%20script/images/1.png" width="200"></div>

4. Click on "Show editor" icon

<div style="text-align:left"><img src="./Qgis%20processing%20script/images/2.png" width="200"></div>

5. Click on "Open script icon"

<div style="text-align:left"><img src="./Qgis%20processing%20script/images/3.png" width="400"></div>

6. Select the downloaded .py file
7. Change input data in the header of file

<div style="text-align:left"><img src="./Qgis%20processing%20script/images/4.png" width="400"></div>

8. Click on "Run" (Play) icon.


## 2. Using inside ESRI (ArcGisPro/ArcMap) applications

Toolbox was developed using ArcGis Pro 3.2

1. Download [Metpetools_ArcGisPro.atbx](Metpetools_ArcGisPro.atbx)
2. Open a New or existing project
3. Go to Menù: Insert -> Toolbox -> Add Toolbox

<div style="text-align:left"><img src="./ArcGis%20toolboxes/images/1.png" width="200"></div>

4. In toolbox panel go to Metpetools and double click on shp2html

5. Set parameters, For more info please check metadata and guide editor inside toolbox
<div style="text-align:left"><img src="./ArcGis%20toolboxes/images/2.png" width="400"></div>


## 3. Using via Jupyter notebook

1. Prepare Python environment with below requirement
- Install native GDAL
    - On Debian Linux: `sudo apt-get install gdal-bin`
    - On macOS with homebrew: `brew install gdal`
- Create Python virtual environment: `virtualenv metpetools` 
- Activate virtual environment: 
    - On UnixLike system `source ./bin/activate`
- Install python dependencies: `pip install GDAL`
- Additional dependencies for Jupyter notebook: `pip install jupyter`
2. Download Jupyter notebook version [shp2html.ipynb](notebook/shp2html.ipynb)
and run
<div style="text-align:left"><img src="./notebook/input mask.png" width="500"></div>
3. Open file (pyton or Jupyter notebook) and update !!! User inputs !!! with your files and your project
4. Run It!
