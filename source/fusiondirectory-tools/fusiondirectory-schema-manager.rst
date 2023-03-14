fusiondirectory-schema-manager
==============================

Description
-----------

This tool will help you to manage the schemas needed by FusionDirectory into the
ldap server

Options
-------

--insert-schema
   This option insert the given list of schemas instead of the default
   list

--replace-schema
   This option insert the given list of schemas, replacing already
   inserted versions of those schemas

--empty-schema
   This option empty the given list of schemas, removing attributes and
   objectClasses from those. This is useful because you cannot delete a
   schema without restarting slapd.

--remove-schema
   This options remove the schema already inserted if LDAP version is higher or equals 2.5.

--list-schemas
   This option list inserted schemas

Examples
--------


Insert the schema myschema (.ldif or .schema) from working directory

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema myschema.schema

Convert /etc/ldap/otherschema/myschema.schema to ldif and replace the existing schema by this one 

.. code-block:: shell

   fusiondirectory-schema-manager --replace-schema /etc/ldap/otherschema/myschema.schema

Empty the schema myschema

.. code-block:: shell

   fusiondirectory-schema-manager --empty-schema myschema

Show the schema

.. code-block:: shell

   fusiondirectory-schema-manager --show-schema myschema
