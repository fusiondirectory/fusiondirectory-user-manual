.. include:: /globals.rst

Functionalities
===============

FusionDirectory WebService plugin exposes a REST webservice that you can use if you want to access LDAP content through FusionDirectory system.
This way, you ensure that your ldap objects are kept consistent, your are able to use the system templates and have restrictions applied by acls.

On top of that you have a nicer API than the low-level LDAP one.

The REST API is documented `here <http://rest.fusiondirectory.org>`_.

.. note::

   Note that you can allow HTTP in plugin configuration, but please avoid doing this except for testing purposes.
