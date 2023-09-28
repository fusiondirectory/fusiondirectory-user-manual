fusiondirectory-schema-manager
==============================

Description
-----------

This tool will help you to manage the schemas needed by FusionDirectory into the
ldap server

Options
-------

--list-schemas
   List inserted schemas and the number off attributes and objectClass
   
--insert-schema
   Insert the given list of schemas 

--replace-schema
   Insert the given list of schemas, replacing already
   inserted versions of those schemas

--empty-schema
   Empty the given list of schemas, removing attributes and
   objectClasses from those.
   This is useful because you cannot delete a schema in openldap < 2.5

--remove-schema
   Remove the schema already inserted if LDAP version is higher or equals 2.5.

--show-schema
   Show you the content of a schema

--help
	Show you the inline manual

--verbose
   verbose output
   
Examples
--------

Insert the schema myschema (.ldif or .schema) from working directory

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema myschema.schema

Replace the existing schema by a new version of the same schema

.. code-block:: shell

   fusiondirectory-schema-manager --replace-schema myschema.schema

Empty the schema myschema

.. code-block:: shell

   fusiondirectory-schema-manager --empty-schema myschema

Show the schema

.. code-block:: shell

   fusiondirectory-schema-manager --show-schema myschema
