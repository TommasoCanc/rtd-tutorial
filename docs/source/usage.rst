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

.. code-block:: console

   # Import biodumpy pachage
   from biodumpy import Biodumpy

   # Import GBIF module
   from biodumpy.inputs import GBIF 

   # Create a list of taxa
   taxa = ['Alytes muletensis (Sanchíz & Adrover, 1979)', 'Bufotes viridis (Laurenti, 1768)', 'Hyla meridionalis Boettger, 1874', 'Anax imperator Leach, 1815']

   # Set the Biodumpy function with the specific parameters
   bdp = Biodumpy([GBIF(bulk=False, accepted_only=True)])

   # Start the download
   bdp.start(taxa, output_path='YOUR_OUTPUT_PATH/downloads/{date}/{module}/{name}')


An important parameter common to all modules is **bulk**. This parameter controls how the information is organized and 
saved thus users can customize how the data is organized according to their needs.

- If **bulk** is set to True, the information downloaded for each taxon is merged into a single file. 
  This option may be useful if the amount of the total data is limited and for consolidating data and simplifying file management.

- If bulk is set to False, the information for each taxon is saved in a separate file. 
  This option is beneficial for detailed analysis, when individual taxon files are required or when the amount of data for
  each taxon is large.


Documentation and Support
-------------------------

For detailed documentation, tutorials, and support, please visit the **biodumpy** GitHub section Tutorial or contact 
our support team at XXX@biodumpy.com.


Contribution
------------

**biodumpy** is an open-source project, and contributions are welcome! 
If you have ideas for new features, bug fixes, or improvements, please submit an issue or pull request on our GitHub repository.


License
-------

**biodumpy** is licensed under the GNU GENERAL PUBLIC LICENSE. See the LICENSE file for more details.


Acknowlegments
--------------

The project was supported by MCIN with funding from European Union—NextGenerationEU (PRTR-C17.I1) and the Government of the Balearic Islands.

<hr>
<div style="display: flex; justify-content: center">
<img src='/www/logo_cbb.png' alt='logo_cbb' width='200'>
</div>

