=============================
Django Countries Currency
=============================

.. image:: https://badge.fury.io/py/dj-countries-currency.svg
    :target: https://badge.fury.io/py/dj-countries-currency

.. image:: https://circleci.com/gh/snap-labs/dj-countries-currency.svg?branch=master
    :target: https://circleci.com/gh/snap-labs/dj-countries-currency

.. image:: https://codecov.io/gh/snap-labs/dj-countries-currency/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/snap-labs/dj-countries-currency


    Django Countries Currency Django Package
    

Documentation
-------------

The full documentation is at https://dj-countries-currency.readthedocs.io.

Quickstart
----------

Install Django Countries Currency::

    pip install dj-countries-currency

Add it to your `INSTALLED_APPS`:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'dj_countries_currency.apps.DjCountriesCurrencyConfig',
        ...
    )

Add Django Countries Currency's URL patterns:

.. code-block:: python

    from dj_countries_currency import urls as dj_countries_currency_urls


    urlpatterns = [
        ...
        url(r'^', include(dj_countries_currency_urls)),
        ...
    ]

Features
--------

* TODO

Running Tests
-------------

Does the code actually work?

::

    source <YOURVIRTUALENV>/bin/activate
    (myenv) $ pip install tox
    (myenv) $ tox
    
Register on snapPyPI
~~~~~~~~~~~~~~~~

Once you've got at least a prototype working and tests running, it's time to register the app on snapPyPI::

    python setup.py register -r pypisnap


Releasing on snapPyPI
~~~~~~~~~~~~~~~~~

Time to release a new version? Easy!

First, use `bumpversion` to up the release number::

    $ pip install bumpversion
    $ bumpversion --current-version VERSION_NUMBER minor --config-file setup.cfg
        or
    $ bumpversion minor --config-file setup.cfg


Where `VERSION_NUMBER` is the current version, e.g. `0.1.0`.

Then run::

    $ python setup.py sdist
    $ twine upload dist/dj-countries-currency-0.1.0.tar.gz  -r pypisnap
        or
    $ twine upload --skip-existing  dist/*  -r pypisnap



It will answer with something like::

    You probably want to also tag the version now:
          git tag -a 0.1.0 -m 'version 0.1.0'
          git push --tags

Go ahead and follow those instructions.
Credits
-------

Tools used in rendering this package:

*  Cookiecutter_
*  `cookiecutter-djangopackage`_

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`cookiecutter-djangopackage`: https://github.com/pydanny/cookiecutter-djangopackage
