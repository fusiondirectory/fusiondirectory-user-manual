.. include:: /globals.rst

Argonaut DNS settings
=====================

* Edit the server and go to the service tab by clicking on the button

  .. image:: images/argonaut-systems-service-button.png
     :alt: Picture of service button in a server

* Add the Argonaut DNS settings service

  .. image:: images/argonaut-systems-services.png
     :alt: Picture of all the services

Configuration
-------------

  .. image:: images/argonaut-service-dns.png
     :alt: Argonaut DNS Service configuration

Ldap2zone global settings
^^^^^^^^^^^^^^^^^^^^^^^^^
  * Bind directory: The directory in which the configuration file for bind will be saved
  * Bind cache directory: The directory in which the zone files will be saved
  * TTL: The time to live saved in the SOA record
  * rndc path: Path to the rndc binary.
  * Search base: LDAP base in which ldap2zone should search. Only useful if you got several nodes for the same zone.

Ldap2zone master settings
^^^^^^^^^^^^^^^^^^^^^^^^^
  * Ignore reverse zone: Do not write reverse zone
  * Notify: notify
  * Allow update: allow-update (semicolon separated and ended)
  * Allow transfer: allow-transfer (semicolon separated and ended)
  * Check names: Cause any host name for the zone to be checked for compliance with RFC 952 and RFC 1123 and take the defined action

Ldap2zone slave settings
^^^^^^^^^^^^^^^^^^^^^^^^

  * DNS slaves

    * zone: DNS zone this server should be declared as slave of
    * master: Master IP(s) for this zone
    * reverses: Whether this server should be slave of reverses zones as well

