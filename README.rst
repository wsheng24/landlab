.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.3776837.svg
   :target: https://doi.org/10.5281/zenodo.3776837

.. image:: https://readthedocs.org/projects/landlab/badge/?version=latest
    :target: https://landlab.readthedocs.org

.. image:: https://github.com/landlab/landlab/actions/workflows/test.yml/badge.svg
    :target: https://github.com/landlab/landlab/actions/workflows/test.yml

.. image:: https://github.com/landlab/landlab/actions/workflows/flake8.yml/badge.svg
    :target: https://github.com/landlab/landlab/actions/workflows/flake8.yml

.. image:: https://github.com/landlab/landlab/actions/workflows/black.yml/badge.svg
    :target: https://github.com/landlab/landlab/actions/workflows/black.yml

.. image:: https://github.com/landlab/landlab/actions/workflows/docs.yml/badge.svg
    :target: https://github.com/landlab/landlab/actions/workflows/docs.yml

.. image:: https://coveralls.io/repos/landlab/landlab/badge.png
    :target: https://coveralls.io/r/landlab/landlab

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/landlab/landlab/release?filepath=notebooks/welcome.ipynb

=======
Landlab
=======

What does Landlab do?
---------------------

Landlab is an open-source Python-language package for numerical modeling of
Earth surface dynamics. It contains

* A gridding engine which represents the model domain. Regular and irregular
  grids are supported.
* A library of process components, each of which represents a physical process
  (e.g., generation of rain, erosion by flowing water). These components have
  a common interface and can be combined based on a user's needs.
* Utilities that support general numerical methods, file input/output, and
  visualization.

In addition Landlab contains a set of Jupyter notebook tutorials providing
an introduction to core concepts and examples of use.

Landlab was designed for disciplines that quantify Earth surface dynamics such
as geomorphology, hydrology, glaciology, and stratigraphy. It can also be used
in related fields. Scientists who use this type of model often build
their own unique model from the ground up, re-coding the basic building blocks
of their landscape model rather than taking advantage of codes that have
already been written. Landlab saves practitioners from the need for this kind
of re-invention by providing standardized components that they can re-use.

Watch the webinar `Landlab Toolkit Overview <https://csdms.colorado.edu/wiki/Presenters-0407>`_
at CSDMS to learn more.

How do I install Landlab?
-------------------------

First you'll need a Python distribution and either the conda or pip package
manager. If you don't know what you want, we recommend the Anaconda Python
distribution.

Two main installation options exist for Landlab. Most people will likely want
to
`install a prepackaged binary <https://landlab.readthedocs.io/en/latest/install/index.html>`_.
We distribute through both conda-forge and pip.

Landlab 2.0
```````````

In April 2020 Landlab switched to version 2.0. Landlab dropped
support of Python 2.7 with this transition.

Supported Python Versions
`````````````````````````

Landlab supports Python versions >= 3.6. Landlab distributes pre-packaged
binaries through `conda-forge <https://anaconda.org/conda-forge/landlab>`_
and `PyPI <https://pypi.org/project/landlab/>`_ for versions 3.6 through 3.9.

Conda Environment with Pre-packaged Binary Distribution
```````````````````````````````````````````````````````

To create a conda environment that installs a pre-packaged binary and all the
dependencies necessary to run the notebooks, clone the repository, navigate to
within the top level directory and use the following command:

.. code-block:: bash

    $ conda env create --file=environment.yml

Then activate the environment and open the welcome notebook execute the
following:

.. code-block:: bash

    $ conda activate landlab_notebooks
    $ jupyter notebook notebooks/welcome.ipynb

Developer Installation
``````````````````````

Individuals interested in modifying the Landlab source code should follow the
`developer installation instructions <https://landlab.readthedocs.io/en/latest/development/install/index.html>`_
which describe cloning the source code, creating a conda environment for
development, compiling, and testing the code.

In short, clone the repository, navigate to the top level directory, and
run the following commands:

.. code-block:: bash

    $ conda create -n landlab python
    $ conda install -n landlab --file=requirements.txt
    $ conda activate landlab
    $ pip install -e .

This will install *landlab* and it's dependencies. You may want to install
some additional utilities used for developing, testing, and running *landlab*
notebooks. This can be done with the following:

.. code-block:: bash

    $ conda install --file=requirements-dev.txt
    $ conda install --file=requirements-testing.txt
    $ conda install --file=requirements-notebooks.txt


How do I verify I've installed Landlab correctly?
-------------------------------------------------

Landlab uses pytest to discover and run tests. These include docstring tests
located within the core source code (``landlab/landlab`` directory) and unit
tests located within the ``landlab/tests`` directory. Presuming you have used a
source code installation with the above conda environment, you will be able to
test your install with

.. code-block::

    $ pytest

from within the ``landlab_dev`` conda environment. Additional instructions,
including how the unit tests directory is structured can be found under the
`testing section`_ of the landlab documentation.

.. _testing section: https://landlab.readthedocs.io/en/master/development/install/test.html

What are Landlab's dependencies?
--------------------------------

The core package dependencies are specified by ``requirements.txt`` and used
by ``setup.py``. There are some additional dependencies that exist for
running the notebooks or modifying the source code and testing.

Details of how we structure our dependencies can be found under the
`dependencies section`_ of the landlab documentation.

.. _dependencies section: https://landlab.readthedocs.io/en/master/development/practices/dependencies.html

How do I learn more about Landlab?
----------------------------------

Our documentation is hosted on ReadTheDocs at https://landlab.readthedocs.io/.
This includes a User Guide and API reference.

The following paper describes the design of Landlab.

`Hobley, D. E. J. <https://www.earth-surf-dynam.net/5/21/2017/>`__, Adams,
J. M., Nudurupati, S. S., Hutton, E. W. H., Gasparini, N. M., Istanbulluoglu,
E. and Tucker, G. E., 2017, Creative computing with Landlab: an open-source
toolkit for building, coupling, and exploring two-dimensional numerical models
of Earth-surface dynamics, Earth Surface Dynamics, 5, p 21-46,
10.5194/esurf-5-21-2017.

Are there any examples of using Landlab I can look at?
------------------------------------------------------

The Landlab package contains a directory, ``landlab/notebooks``, with
Jupyter Notebooks describing core concepts and giving examples of using components.
The file ``landlab/notebooks/welcome.ipynb`` provides a table of contents to
the notebooks and is the recommended starting place.
Additionally, there are a set of notebooks curated to teach physical processes
located in the directory ``landlab/notebooks/teaching``.

Run on Binder
`````````````

To launch an instance of
Binder and `explore the notebooks click here`_.

.. _explore the notebooks click here: https://mybinder.org/v2/gh/landlab/landlab/release?filepath=notebooks/welcome.ipynb

To launch a Binder instance that goes straight to the `teaching notebooks click here`_.

.. _teaching notebooks click here: https://mybinder.org/v2/gh/landlab/landlab/release?filepath=notebooks/teaching/welcome_teaching.ipynb

Run on the CSDMS JupyterHub
```````````````````````````

The Landlab notebooks can also be run on the CSDMS JupyterHub.
To sign up for a free account,
`visit the CSDMS wiki`_ and follow the instructions there.
Then, click to explore the `example notebooks`_,
or to go straight to the `teaching notebooks`_.

.. _visit the CSDMS wiki: https://csdms.colorado.edu/wiki/JupyterHub
.. _example notebooks: https://jupyter.openearthscape.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Flandlab%2Flandlab&urlpath=tree%2Flandlab%2Fnotebooks%2Fwelcome.ipynb&branch=master
.. _teaching notebooks: https://jupyter.openearthscape.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Flandlab%2Flandlab&urlpath=tree%2Flandlab%2Fnotebooks%2Fteaching%2Fwelcome_teaching.ipynb&branch=master


What License does Landlab use?
------------------------------

MIT (see the file LICENSE.txt)

I used Landlab and want to cite it. How do I do this correctly?
---------------------------------------------------------------

The following references refer to the entire Landlab package.

`Hobley, D. E. J. <https://www.earth-surf-dynam.net/5/21/2017/>`__, Adams,
J. M., Nudurupati, S. S., Hutton, E. W. H., Gasparini, N. M., Istanbulluoglu,
E. and Tucker, G. E., 2017, Creative computing with Landlab: an open-source
toolkit for building, coupling, and exploring two-dimensional numerical models
of Earth-surface dynamics, Earth Surface Dynamics, 5, p 21-46,
10.5194/esurf-5-21-2017.

`Barnhart, K. R. <https://doi.org/10.5194/esurf-8-379-2020>`__,
Hutton, E. W. H., Tucker, G. E., Gasparini, N. M., Istanbulluoglu, E.,
Hobley, D. E. J., Lyons, N. J., Mouchene, M., Nudurupati, S. S., Adams, J. M.,
and Bandaragoda, C., 2020, Short communication: Landlab v2.0: A software package for
Earth surface dynamics, Earth Surf. Dynam. Discuss., 8, pp 379-397,
https://doi.org/10.5194/esurf-8-379-2020, in review, 2020.

BibTeX format:
::

  @article{hobley2017creative,
    title={
      Creative computing with Landlab: an open-source toolkit for building,
      coupling, and exploring two-dimensional numerical models of
      Earth-surface dynamics
    },
    author={
      Hobley, Daniel EJ and Adams, Jordan M and Nudurupati, Sai Siddhartha and
      Hutton, Eric WH and Gasparini, Nicole M and Istanbulluoglu, Erkan and
      Tucker, Gregory E
    },
    journal={Earth Surface Dynamics},
    volume={5},
    number={1},
    pages={21--46},
    year={2017},
    publisher={Copernicus GmbH},
    url={https://esurf.copernicus.org/articles/5/21/2017/},
    doi={10.5194/esurf-5-21-2017}
  }

  @article{barnhart2020landlab,
    title={Landlab v2. 0: a software package for Earth surface dynamics},
    author={
      Barnhart, Katherine R and Hutton, Eric WH and Tucker, Gregory E and
      Gasparini, Nicole M and Istanbulluoglu, Erkan and Hobley, Daniel EJ and
      Lyons, Nathan J and Mouchene, Margaux and Nudurupati, Sai Siddhartha and
      Adams, Jordan M and others
    },
    journal={Earth Surface Dynamics},
    volume={8},
    number={2},
    pages={379--397},
    year={2020},
    publisher={Copernicus GmbH}
    url = {https://esurf.copernicus.org/articles/8/379/2020/},
    doi = {10.5194/esurf-8-379-2020}
  }


In addition, depending on what parts of Landlab you use, you may need to cite
component-specific. Refer to the References section of each component and
`this page <https://landlab.readthedocs.io/en/master/citation_registry.html#cite-as>`_
which discusses the Landlab Citation Registry tool.

I think I found a bug. What should I do?
----------------------------------------

Please make an Issue describing the bug so we can address it, or work with you
to address it. Please try to provide a
`minimal, reproducible example <https://stackoverflow.com/help/minimal-reproducible-example>`_.

I found something in the documentation that isn't clear. What should I do?
--------------------------------------------------------------------------

Please make an Issue describing the what isn't clear to you. Someone will tag
the most appropriate member of the core Landlab team. We will work to clarify
your question and revise the documentation so that it is clear for the next user.

I'm interested in contributing to Landlab. Where do I get started?
------------------------------------------------------------------

Thank you for your interest! Refer to ``CONTRIBUTING.md`` and
`this <https://landlab.readthedocs.io/en/master/development/index.html#development>`_
page in the documentation that describes contribution guidelines.

How is the Landlab package structured?
--------------------------------------

The
`following page <https://landlab.readthedocs.io/en/master/development/package_organization.html>`_
in the documentation describes the package structure.

How was Landlab funded?
-----------------------

Landlab is funded by the US National Science Foundation. It has been supported
by the following grants:

* A Collaborative NSF SI2-SSE proposal to
  University of Colorado (Greg Tucker,
  `1147454 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1147454&HistoricalAwards=false>`_),
  and the University of Washington (Erkan Istanbulluoglu,
  `1148305 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1148305&HistoricalAwards=false>`_)
* A Collaborative NSF SI2-SSI proposal to
  University of Colorado (Greg Tucker and Dan Hobley,
  `1450409 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1450409&HistoricalAwards=false>`_),
  Tulane University (Nicole Gasparini,
  `1450338 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1450338&HistoricalAwards=false>`_),
  and the University of Washington (Erkan Istanbulluoglu,
  `1450412 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1450412&HistoricalAwards=false>`_).
* A NSF EAR Postdoctoral Fellowship to Katy Barnhart
  (`1725774 <https://www.nsf.gov/awardsearch/showAward?AWD_ID=1725774&HistoricalAwards=false>`_).

