.. include:: /globals.rst

Functionalities
===============

FusionDirectory WebService plugin exposes a REST webservice that you can use if you want to access LDAP content through FusionDirectory system.
This way, you ensure that your ldap objects are kept consistent, your are able to use the system templates and have restrictions applied by acls.

On top of that you have a nicer API than the low-level LDAP one.

The REST API is documented `here <http://rest.fusiondirectory.org>`_.

.. note::

   Note that you can allow HTTP in plugin configuration, but please avoid doing this except for testing purposes.

Plugins
-------

Systems
^^^^^^^

Systems have a special networkInterfaces attribute in the interfacesManagement tab allowing to access the interfaces of a system.

Examples:

Get interfaces:

.. code-block::

   GET /objects/server/cn=server1,ou=servers,ou=systems,dc=example,dc=com/interfacesManagement/networkInterfaces
   Response:
   [
    {
      "cn": ["eth0"],
      "macAddress": ["00:11:22:33:44:88"],
      "ipHostNumber": ["192.168.2.2"],
      "dn": "cn=eth0,cn=server1,ou=servers,ou=systems,dc=example,dc=com"
    },
    {
      "cn": ["eth1"],
      "macAddress": ["00:11:22:33:44:99"],
      "ipHostNumber": ["192.168.2.22"],
      "dn": "cn=eth1,cn=server1,ou=servers,ou=systems,dc=example,dc=com"
    }
   ]

Add an interface:

.. code-block::

   PATCH /objects/server/cn=server1,ou=servers,ou=systems,dc=example,dc=com/interfacesManagement/networkInterfaces/values [{"cn":["eth2"],"ipHostNumber":["192.168.2.3"]}]
