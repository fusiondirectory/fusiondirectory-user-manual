fusiondirectory-insert-schema 
=============================

Description
-----------

This tool will help you to manage the schemas needed by FusionDirectory into the
ldap server

Options
-------

-i
   This option insert the given list of schemas instead of the default
   list

-m
   This option insert the given list of schemas, replacing already
   inserted versions of those schemas

-e
   This option empty the given list of schemas, removing attributes and
   objectClasses from those. This is useful because you cannot delete a
   schema without restarting slapd.

-l
   This option list inserted schemas

-n
   This option will make generated ldifs file to not be deleted after
   execution. Might be useful to understand errors.

-c
   This option make the program continue even if an error occur

-y
   This option answer yes to all questions. The only question right now
   is the confirmation one when you ask to empty a schema.

-o
   This option allow you to specify specifics options to give to ldap
   commands such as ldapmodify, but beware that you will not be able to
   see things like password prompts as the output of these commands is
   piped.

Examples
--------

Insert the core schemas in your LDAP directory 

.. code-block:: shell

   fusiondirectory-insert-schema 

Insert the schema /etc/ldap/otherschema/myschema.ldif 

.. code-block:: shell

   fusiondirectory-insert-schema -i /etc/ldap/otherschema/myschema.ldif 

Convert /etc/ldap/otherschema/myschema.schema to ldif and insert it

.. code-block:: shell

   fusiondirectory-insert-schema -i /etc/ldap/otherschema/myschema.schema


Insert the schema myschema.ldif from working directory

.. code-block:: shell

   fusiondirectory-insert-schema -i myschema

Convert /etc/ldap/otherschema/myschema.schema to ldif and replace the existing schema by this one 

.. code-block:: shell

   fusiondirectory-insert-schema -m /etc/ldap/otherschema/myschema.schema

Empty the schema myschema

.. code-block:: shell

   fusiondirectory-insert-schema -e myschema

Connect to another ldap server to insert the schema

.. code-block:: shell

   fusiondirectory-insert-schema -o "-H ldap://my.ldap.com -ZZ -D cn=admin,cn=config -w password -x"


