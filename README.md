# HMS-Gridded-Automation
Batch collection of environmental data modeling workflow for gridded land surface models (LSMs) through DEM acquisition and HMS Restful API tailored for VELMA initialization
This code and data repository supports the manuscript entitled "Improving data acquisition and automation for gridded models and modeling workflow" under review in Environmental Modelling & Software. 
The abstract (below) provides the insight to the work that has been performed. 

Continuous observed environmental data required during model simulations for gridded land surface models (LSMs) are often difficult to obtain, making initializations challenging. In response, this study focuses on automation retrievals for digital elevation models (DEMs), climate drivers, and surface runoff across the United States, initializing the Visualizing Ecosystem and Land Management Assessment (VELMA) model. This is accomplished using the US EPA’s Hydrologic Micro Services (HMS) Representation State Transfer (REST) application programming interface (API) and Geospatial Data Abstraction Library (GDAL) with Python. DEM acquisition is retrieved from Google Earth Engine (GEE), where transformation between projected latitude and longitude coordinates are translated into grid cell indices. This acquisition workflow provides greater efficiency, minimizes initialization time, reduces manual processing errors, and facilitates a reusable methodology for other modeling studies. With this innovation, users of VELMA and other gridded LSMs will be able to initialize simulations more efficiently, improving their operational capabilities. For more information on the HMS REST API documentation please visit https://qed.epa.gov/hms/api_doc/

# Workflow Environment Deployment 
In order to recreate the development of the virtual environment with GDAL/HMS/GEE Batch Automation retrieval data, installation of an environment manager is required. However it is recommended for you to utilize miniforge which can be obtained at (https://conda-forge.org/miniforge/) : 

1) Open command line terminal
2) Run code to create the virtual environment based on the yaml (.yml) configuration file from your directory path located in the repository: conda env create -f 
e.g. conda env create -f "path\020325pygdalenvironment.yml"

3) Virtual environment developed will be named pygdal4. The environment will be placed into environment file folder with the name pygdal4. This will install all dependencies required to run the virtual environment.
4) (Start here at step 4 after initial deployment to activate the environment) To use the environment prior to jupyterlab/jupyter notebook deployment, we must activate the environment: conda activate pygdal4 
5) Change the directory/path/folder where the repository was downloaded : 
e.g. cd path\folderofchoice
6) Initialize jupyterlab to open the files from the downloaded repository: python -m jupyterlab
A browser on the internet will open with  jupyterlab to access the jupyter notebook for the workflow and the provided associated files required for running the respository after forking or downloading.  


# Viewing Notebook Render
If unable to view the notebook render due to the output stored in the jupyter notebook, please use the nbviewer link: https://nbviewer.org/github/kvenable2011/HMS-Gridded-Automation/blob/main/022025_HMS_Automation_Cleaned.ipynb
