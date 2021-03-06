.. include:: references.txt

.. _installation:

Installation
============

iminuit works with Python 2.7 as well as 3.4 or later.

Dependencies
------------

Like most Python packages, iminuit installation requires `setuptools`_.

The following dependencies are optional:

* numpy
* ipython
* matplotlib
* pytest, pytest-cov
* Cython
* Sphinx, sphinx-rtd


TODO: describe better where which dependency is used.


Stable version
--------------

To install the latest stable version:

.. code-block:: bash

    $ pip install iminuit


Conda
-----

Conda packages for iminuit are available via the ``astropy`` channel at https://anaconda.org/astropy/iminuit

.. code-block:: bash

    $ conda install -c astropy iminuit


Windows
-------

For Windows, Christoph Gohlke made a nice windows binary to save you all from Windows compilation nightmare:

   `http://www.lfd.uci.edu/~gohlke/pythonlibs/#iminuit <http://www.lfd.uci.edu/~gohlke/pythonlibs/#iminuit>`_


Development version
-------------------

To install the latest development version clone the
repository from `Github <https://github.com/iminuit/iminuit>`_:

.. code-block:: bash

    $ git clone https://github.com/iminuit/iminuit.git
    $ cd iminuit
    $ python setup.py install

Docs
----

You will need ``sphinx`` and ``sphinx_rtd_theme``.
They can be installed via

.. code-block:: bash

   $ pip install sphinx
   $ pip install sphinx_rtd_theme

To generate html docs locally, ``iminuit`` has to be available.
To check if that is the case, and which version you're using, you can use this command:

.. code-block:: bash

    $ python -c 'import iminuit; print(iminuit)'

One way to achieve this is to do this:

.. code-block:: bash

   $ python setup.py build_ext --inplace
   $ python setup.py develop

Another is to just install ``iminuit`` into ``site-packages``:

.. code-block:: bash

   $ python setup.py install

Once you have ``iminuit`` available, use these commands to build the docs:

.. code-block:: bash

   $ cd doc
   $ make html

The HTML output is here:

.. code-block:: bash

   $ open _build/html/index.html


Testing
-------

To run the tests you need to install `pytest`_.

To run the iminuit tests for an installed version of the package:

.. code-block:: bash

    python -m pytest --pyargs iminuit

To run the tests from the source folder (e.g. during pytest development), use this command:

.. code-block:: bash

    $ make test

To get a coverage report from the tests:

.. code-block:: bash

    $ make coverage
