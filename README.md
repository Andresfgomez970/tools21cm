# Tools21cm

[![DOI](https://joss.theoj.org/papers/10.21105/joss.02363/status.svg)](https://doi.org/10.21105/joss.02363)

A python package for analysing 21-cm signals from the Epoch of Reionization (EoR) and Cosmic Dawn (CD). Full documentation (with examples, installation instructions and complete module description) can be found at [readthedocs](https://tools21cm.readthedocs.io/).

## Package details

The package provides tools to analyse cosmological simulations of EoR and CD. It contains modules to create mock 21-cm observations for current and upcoming radio telescopes, such as LOFAR, MWA and SKA, and to construct statistical measures.

### Input

Currently, `Tools21cm` supports the following simulation codes:

* [CUBEP3M](https://github.com/jharno/cubep3m)
* [C2RAY](https://github.com/garrelt/C2-Ray3Dm)
* [GRIZZLY](https://arxiv.org/abs/1710.09397)
* [21cmFAST](https://21cmfast.readthedocs.io/en/latest/)
* [Simfast21](https://github.com/mariogrs/Simfast21)
* [sem_num](https://arxiv.org/abs/1403.0941)

### Outputs

There are various manipulation and analysis moduled in `Tools21cm`. 

* Angular coordinates: methods to convert data between physical (cMpc) coordinates and observational (angular-frequency) coordinates
* Bubble Statistics: methods to calcluate the sizes of the regions of interest and estimate the size distributions
* Cosmological calculators: various functions for calculating some cosmological stuff
* Identifying regions: methods to identify regions of interest in images
* Lightcone: methods to construct lightcones
* Power spectrum: contains functions to estimate various two point statistics
* Reading simuation outputs: methods to read simulations outputs
* Smoothing: methods to smooth or reduce resolution of the data to reduce noise
* Point statistics: contains various useful statistical methods
* Temperature: methods to estimate the brightness temperature

For detail documentation and how to use them, see [here](https://tools21cm.readthedocs.io/contents.html).

### Under Developement

* Foreground model: methods to simulate and analyse the foreground signal for 21 cm signal
* Primary beam: methods to simulate the primary beam of radio telescope
* Telescope noise: 
	* simulate the radio telescope observation strategy
	* simulate telescope noise
* Topology: methods to estimate the topology of the region of interest



## INSTALLATION

One can install a stable version of this package using pip by running the following command::

    pip install tools21cm

This package is being actively under-development, which involves addition of new modules and bug fixes. In order to use the latest version, one can clone this package.

To install the package from source, one should clone this package running the following::

    git clone https://github.com/sambit-giri/tools21cm.git

To install the package in the standard location, run the following in the root directory::

    python setup.py install

In order to install it in a separate directory::

    python setup.py install --home=directory

One can also install the latest version using pip by running the following command::

    pip install git+https://github.com/sambit-giri/tools21cm.git

The dependencies should be installed automatically during the installation process. If they fail for some reason, you can install them manually before installing tools21cm. The list of required packages can be found in the requirements.txt file present in the root directory.

### Tests

For testing, one can use [pytest](https://docs.pytest.org/en/stable/) or [nosetests](https://nose.readthedocs.io/en/latest/). Both packages can be installed using pip. To run all the test script, run the either of the following::

    python -m pytest tests
    
	nosetests -v

## CONTRIBUTING

If you find any bugs or unexpected behavior in the code, please feel free to open a [Github issue](https://github.com/sambit-giri/tools21cm/issues). The issue page is also good if you seek help or have suggestions for us. For more details, please see [here](https://tools21cm.readthedocs.io/contributing.html).
