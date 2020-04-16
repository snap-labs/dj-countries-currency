=====
Usage
=====

To use Django Countries Currency in a project, add it to your `INSTALLED_APPS`:

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
