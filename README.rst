.. image:: docs/pyswarms-header.png
        :alt: PySwarms Logo
        :align: center

------------

.. image:: https://badge.fury.io/py/pyswarms.svg
        :target: https://badge.fury.io/py/pyswarms
        :alt: PyPI Version

.. image:: https://travis-ci.org/ljvmiranda921/pyswarms.svg?branch=master
        :target: https://travis-ci.org/ljvmiranda921/pyswarms
        :alt: Build Status

.. image:: https://readthedocs.org/projects/pyswarms/badge/?version=latest
        :target: https://pyswarms.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://landscape.io/github/ljvmiranda921/pyswarms/master/landscape.svg?style=flat
        :target: https://landscape.io/github/ljvmiranda921/pyswarms/master
        :alt: Code Health

.. image:: https://pyup.io/repos/github/ljvmiranda921/pyswarms/shield.svg
        :target: https://pyup.io/repos/github/ljvmiranda921/pyswarms/
        :alt: Updates

.. image:: https://img.shields.io/badge/python-2.7%2C3.4%2C3.5%2C3.6-blue.svg
        :target: https://github.com/ljvmiranda921/pyswarms
        :alt: Python versions

.. image:: https://img.shields.io/badge/license-MIT-blue.svg   
        :target: https://raw.githubusercontent.com/ljvmiranda921/pyswarms/master/LICENSE
        :alt: License

.. image:: https://zenodo.org/badge/97002861.svg
        :target: https://zenodo.org/badge/latestdoi/97002861
        :alt: Citation

PySwarms is a an extensible research toolkit for particle swarm optimization (PSO) in Python.

* Free software: MIT license
* Documentation: https://pyswarms.readthedocs.io.


Features
--------
* High-level module for Particle Swarm Optimization. For a list of all optimizers, check this_ link.
* Test optimizers using various objective functions
* (For Devs and Researchers): Highly-extensible API for implementing your own techniques
* Easy API built on :code:`matplotlib` to create animations like these:

.. image:: docs/examples/output_3d.gif
        :target: docs/examples/output_3d.gif
        :width: 320 px
        :alt: 3d particle plot

.. image:: docs/examples/output_9_0.png
        :target: docs/examples/output_9_0.png
        :width: 320 px
        :alt: cost history plot

.. _this: https://pyswarms.readthedocs.io/en/latest/features.html

Dependencies
-------------
* numpy >= 1.13.0
* scipy >= 0.17.0
* matplotlib >= 1.3.1

Installation
-------------
To install PySwarms, run this command in your terminal:

.. code-block:: console

    $ pip install pyswarms

This is the preferred method to install PySwarms, as it will always install the most recent stable release.

In case you want to install the bleeding-edge version, clone this repo:

.. code-block:: console

    $ git clone https://github.com/ljvmiranda921/pyswarms.git

and then run

.. code-block:: console

    $ python setup.py install

Basic Usage
------------
To use PySwarms in your project,

.. code-block:: python

    import pyswarms as ps

Suppose you want to find the minima of :math:`f(x) = x^2` using global best PSO, simply import the 
built-in sphere function, :code:`pyswarms.utils.functions.sphere_func()`, and the necessary optimizer:

.. code-block:: python

    import pyswarms as ps
    from pyswarms.utils.functions import single_obj as fx

    # Set-up hyperparameters
    options = {'c1': 0.5, 'c2': 0.3, 'w':0.9}

    # Call instance of PSO
    optimizer = ps.single.GlobalBestPSO(n_particles=10, dimensions=2, options=options)

    # Perform optimization
    stats = optimizer.optimize(fx.sphere_func, iters=100)

Credits
-------
This project was inspired by the pyswarm_ module that performs PSO with constrained support.
The package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _pyswarm: https://github.com/tisimst/pyswarm
.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage

Cite us
--------
Are you using PySwarms in your project or research? Please cite us!

.. code-block:: bibtex

    @article{PySwarms2017,
        author = "Lester James V. Miranda",
        year = 2017,
        title = "PySwarms, a research-toolkit for Particle Swarm Optimization in Python",
        doi = {10.5281/zenodo.986300},
        url = {https://zenodo.org/badge/latestdoi/97002861}
    }

Others
------
Like it? Love it? Leave us a star on Github_ to show your appreciation! 

.. _Github: https://github.com/ljvmiranda921/pyswarms
