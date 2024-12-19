Prerequisites
=============

FusionDirectory is a Web application that will need:

* a webserver;
* PHP;
* an ldap server;

Web server
----------

FusionDirectory requires a web server that supports PHP, like:

* `Apache 2 (or more recent) <http://httpd.apache.org>`_;
* `Nginx <http://nginx.org/>`_;
* `Microsoft IIS <https://www.iis.net>`_.

PHP
---

As of 1.4 release, FusionDirectory requires `PHP <https://www.php.net>`_ 7.3 or 7.4.

Mandatory extensions
^^^^^^^^^^^^^^^^^^^^

Following PHP extensions are required for the app to work properly:

* ``cas``: for CAS authentication;
* ``curl``: to communicate with different types of servers and protocols
* ``filter``: to filters a variable with a specified filter;
* ``fpdf``: to export data in pdf format;
* ``gd``: to generate images;
* ``iconv`` : for the samba integration;
* ``imagick`` : to handle images;
* ``imap``: to handle imap servers management;
* ``json``: to get support for JSON data format;
* ``mbstring``:  to manage multi bytes characters;
* ``ldap``: to connect and query the ldap server;
* ``openssl``: secured communications and generation of secure tokens;
* ``session``: to get user sessions support;
* ``simplexml``;
* ``xml``.

Optional extensions
^^^^^^^^^^^^^^^^^^^

.. note::

   Even if those extensions are not mandatory, we advise you to install them anyways.

Following PHP extensions are required for some extra features of FusionDirectory :

* ``gettext`` : for an internationalized interface.
* ``mhash`` : to make use of SSHA encryption
* ``sha1`` : to make use of SSHA encryption
* ``zlib``: to handle snapshots;


Configuration
^^^^^^^^^^^^^

PHP configuration file (``php.ini``) must be adapted to reflect following variables:

.. code-block:: ini

    expose_php = Off;
    implicit_flush = Off;
    memory_limit = 512M ;      // max memory limit
    max_execution_time = 30 ;  // not mandatory but adviced
    session.auto_start = off ;

LDAP server
-----------

For FusionDirectory to work you need an ldap server.

Servers know to work are :

* `OpenLDAP`_
* `389DS`_

.. _OpenLDAP : https://www.openldap.org/
.. _389DS : https://directory.fedoraproject.org/
