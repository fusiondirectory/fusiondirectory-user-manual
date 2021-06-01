.. include:: /globals.rst

Functionalities
===============

DNS Management
--------------

Clicking the DNS entry from the main menu, you will get to the DNS management page.

On this page you can create and manage three types of objects:

DNS Zones
^^^^^^^^^

A DNS zone with all the records it contains.

  .. image:: images/dns-zone.png
     :alt: Edition of a DNS Zone object

DNS Views
^^^^^^^^^

  .. image:: images/dns-view.png
     :alt: Edition of a DNS View object

DNS ACLs
^^^^^^^^

  .. image:: images/dns-acl.png
     :alt: Edition of a DNS ACL object

Systems DNS tab
---------------

On systems, you will find a DNS tab that allows you to link a zone to this system.

  .. image:: images/dns-system-tab.png
     :alt: Main section of DNS system tab

If you add zones to this tab, you will be able to add records related to this system in the zone and FusionDirectory will keep them updated if you rename the system or change its IP. If the system matches the SOA field and has a correctly configured Argonaut client and Argonaut DNS settings service, you will also be able to trigger the zone refresh through ldap2zone from this tab. You can also trigger it from DNS management page, using the "Refresh Zone" action.
