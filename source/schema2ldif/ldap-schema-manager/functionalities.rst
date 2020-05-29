
Functionalities
===============

How it works
------------

List schemas already installed :

.. code-block:: shell

   ldap-schema-manager -l

Insert a new schema :
^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   ldap-schema-manager -i /path/to/your/file.schema

If a schema of the same name is already present the insertion will fail.
If the file doesnt have a .schema extension added to the name, ldap-schema-manager will add .ldif

Update a schema :
^^^^^^^^^^^^^^^^^
.. code-block:: shell

   ldap-schema-manager -m /path/to/your/file.schema

If a schema of the same name is not present the update will fail.

Empty a schema :
^^^^^^^^^^^^^^^^

.. code-block:: shell

   ldap-schema-manager -e schema_name

.. Warning::

   This will clean the schema but it stay inside your ldap server in de cn=schema,cn=config.
   It's impossible right now to remove a node from cn=schema,cn=config.
   ldap-schema-manager provide this solution to be able to remove a schema without stopping the ldap server,
   but the schema will still be listed by running -l.

.. note::

   The conversion is done by schema2ldif. 
   The only constraint is that the schema first list attributes then objectclass, which is the case in all the standard schema we saw.

.. note::
   If you want to insert again a schema emptied by -e, you should use -m and not -i.





