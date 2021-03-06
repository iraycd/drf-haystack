==================================
Haystack for Django REST Framework
==================================

Contents:

.. toctree::
   :maxdepth: 2

   basic_usage
   advanced_usage

=====
About
=====
Small library aiming to simplify using Haystack with Django REST Framework

Features
========

Supported Python versions:

    - Python 2.6
        - Django 1.5 and 1.6
    - Python 2.7, 3.3 and 3.4
        - Django 1.5, 1.6, 1.7 and 1.8


Installation
============
It's in the cheese shop!

.. code-block:: none

    $ pip install drf-haystack


Requirements
============
    - Django
    - Django REST Framework
    - Haystack (and a supported search engine such as Solr, Elasticsearch, Whoosh, etc.)
    - (geopy and libgeos if you want to use geo spatial filtering)


Changelog
=========

v1.5.0
------
*Release date: 2015-06-29*

    - Added support for field lookups in queries, such as ``field__contains=foobar``.
      Check out `Haystack docs <http://django-haystack.readthedocs.org/en/latest/searchqueryset_api.html?highlight=field%20lookup#field-lookups>`_
      for details.
    - Added default ``permission_classes`` on ``HaystackGenericAPIView`` in order to avoid crash when
      using global permission classes on REST Framework. See :ref:`permission-classes-label` for details.

v1.4
----
*Release date: 2015-06-15*

    - Fixed issues for Geo spatial filtering on django-haystack v2.4.x with Elasticsearch.
    - A serializer class now accepts a list or tuple of ``ignore_field`` to bypass serialization.
    - Added support for Highlighting.

v1.3
----
*Release date: 2015-05-19*

    - ``HaystackGenericAPIView().get_object()`` now returns Http404 instead of an empty ``SearchQueryset``
      if no object is found. This mimics the behaviour from ``GenericAPIView().get_object()``.
    - Removed hard dependencies for ``geopy`` and ``libgeos`` (See Github :issue:`5`). This means
      that if you want to use the ``HaystackGEOSpatialFilter``, you have to install these libraries
      manually.

v1.2
----
*Release date: 2015-03-23*

    - Fixed ``MissingDependency`` error when using another search backend than Elasticsearch.
    - Fixed converting distance to D object before filtering in HaystackGEOSpatialFilter.
    - Added Python 3 classifier.

v1.1
----
*Release date: 2015-02-16*

    - Full coverage (almost) test suite
    - Documentation
    - Beta release Development classifier

v1.0
----
*Release date: 2015-02-14*

    - Initial release.


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

