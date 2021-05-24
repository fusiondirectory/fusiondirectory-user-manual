
Functionalities
===============

The ldap2zone application is used to generate DNS zone, acls, views and configuration for master and slaves

How it works
------------

Argonaut-ldap2zone read the LDAP and retrieve the information for making the files locally

The arguments are the following:

*  --verbose (be verbose)
*  --noreverse (Do not write reverse zone)
*  --norestart (Do not write reverse zone)
*  --dumpdir (Dump the zones and bind configuration to another dir for testing purposes)
*  --ldap2acls (Write the the acls needed for bind in named.conf.acls)
*  --ldap2view (Write the zones in view format when you want to do split horizon dns)
*  --slave (Write the udpated slave zones files)

Examples
--------

.. code-block:: shell

   # Write the updated zones from ldap and refresh bind
   argonaut-ldap2zone --verbose fusiondirectory.org.
   # Write the updated zones from ldap to another directory and don't refresh bind
   argonaut-ldap2zone --verbose --norestart --dumpdir dnszone/ fusiondirectory.org
   # Write the updated zones from ldap in a bind view named internal and refresh bind
   argonaut-ldap2zone --verbose --ldap2view internal
   # Write the acls from ldap into named.conf.acls
   argonaut-ldap2zone --verbose --ldap2acls
   # Write the udpated slave zones files
   argonaut-ldap2zone --verbose --slave
