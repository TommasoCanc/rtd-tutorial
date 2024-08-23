biodumpy: A Comprehensive Biological Data Downloader
====================================================

.. _installation:

Overview
--------

**biodumpy** is a powerful and versatile Python package designed to simplify the process of retrieving biological information 
from several public databases. With **biodumpy**, researchers can easily download and manage data from multiple sources, 
ensuring access to the most up-to-date and comprehensive biological information available.


Key Features
------------

**biodumpy** provides dedicated modules for each supported database. Each module includes several functions tailored to 
retrieving information from its specific source. The current modules are dedicated for the following databases:

- `NCBI`_ (National Center for Biotechnology Information)
.. _NCBI: https://www.ncbi.nlm.nih.gov

- `BOLD`_ (Barcode of Life Data Systems)
.. _BOLD: https://boldsystems.org/

- `GBIF`_ (Global Biodiversity Information Facility)
.. _GBIF: https://www.gbif.org/

This list can be expanded, and suggestions and feedback are greatly appreciated.


Main functionalities and workflow
---------------------------------

Before using **biodumpy**, users need to install the package in their Python environment with the following command:

.. code-block:: console

   (.venv) $ pip install biodumpy

   
Usage
^^^^^

To simplify the use of **biodumpy**, we create a general structure common among the modules:

1) Load the package: Import **biodumpy** into your Python environment.
2) Load the desired module: Import one or more specific modules needed to retrieve the data.
3) Set up the function: Configure the **biodumpy** function with the required parameters.
4) Start the download: Execute the function to begin retrieving the data.

Here we show an example resuming the general structure. In this case we use the GBIF module.

