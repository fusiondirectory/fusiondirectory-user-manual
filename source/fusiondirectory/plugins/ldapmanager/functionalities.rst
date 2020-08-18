.. include:: /globals.rst

Functionalities
===============

In your FusionDirectory web interface, you now have, in the Configuration section, a new item called “LDAP import/export” that you can use to manage ldif in your infrastructure : 

.. image:: images/ldapmanager-ldap-import-export.png
   :alt: Picture of LDAP import/export icon in FusionDirectory
   
When you click on this item, then you can:

    * Export ldif
    * Import ldif
    * Import CSV
   
Export LDIF
-----------

The LDIF export plugin provides methods to download a complete snapshot of the running LDAP directory as ldif. You may save these files for backup purpose or when initializing a new server. 

.. image:: images/ldapmanager-export-ldif.png
   :alt: Picture of ldif export tab in FusionDirectory
   
"Export single entry" allows you to export a single ldap record. For example, in my ldap directory, if I ask to export the sales group:


.. code-block:: bash

   cn=sales,ou=groups,dc=fusiondirectory,dc=org
   
the result is an ldif file with this content: 



.. code-block:: bash

   dn: cn=sales,ou=groups,dc=fusiondirectory,dc=org
   cn: sales
   gidNumber: 1105
   memberUid: Homer.Sympson
   memberUid: gmarquez
   objectClass: top
   objectClass: posixGroup
   
"Export complete LDIF for" allows you to export all records of your ldap directory.

Import LDIF
-----------

The LDIF import plugin provides methods to upload a set of entries to your running LDAP directory as LDIF. You may use this to add new or modify existing entries. Remember that FusionDirectory will not check your ldifs for FusionDirectory conformance. 

.. image:: images/ldapmanager-import-ldif.png
   :alt: Picture of ldif import tab in FusionDirectory 
   
Import LDIF File (Modify existing objects, keep untouched attributes)  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For example, in FusionDirectory, I have this posixgroup-test group: 

.. image:: images/ldapmanager-posix-group-test.png
   :alt: Picture of posix-group test tab in FusionDirectory 

which corresponds to this entry in my ldap directory: 


.. code-block:: bash

   dn: cn=posix-group,ou=groups,dc=fusiondirectory,dc=org
   cn: posix-group
   gidNumber: 1105
   memberUid: durieux.Bcarole
   objectClass: top
   objectClass: posixGroup
   
CSV import
----------

The CSV import plugin provides methods to generate objects (for instance user accounts) from a file containing Colon Seperated Values. You can decide which columns should be transfered to which attribute and select a template to apply.    

You can also add fixed values for fields which are missing from the CSV file for instance

.. image:: images/ldapmanager-csv-import.png
   :alt: Picture of CSV import tab in FusionDirectory    

Note that the file must not contain a header line, all lines are treated as data to import, except if they start with a #.

Multivaluated columns
^^^^^^^^^^^^^^^^^^^^^

When you need to import data to a multivalue field, like group members for instance, you need to separate your values with the character "|".

System interfaces
^^^^^^^^^^^^^^^^^

When importing systems with interfaces information, you need to represent each interface as a JSON object, with an array for the value of each field.
Interfaces still need to be separated by "|" if there are several, as for other mulitvaluated columns.

Example:

.. code-block:: bash

   server1;{"cn":["eth0"],"macAddress":["00:11:22:33:12:01"],"ipHostNumber":["192.168.12.1"]}
   server2;{"cn":["eth0"],"macAddress":["00:11:22:33:12:02"],"ipHostNumber":["192.168.12.2"]}|{"cn":["eth1"],"macAddress":["00:11:22:33:12:03"],"ipHostNumber":["192.168.12.3"]}
