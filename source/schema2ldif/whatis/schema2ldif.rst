What is schema2ldif ?
=====================

`Schema2ldif`_ provides a
solution to the conversion and management of schema inside an `OpenLDAP`_ directory.

OpenLDAP since version 2.4 has a backend named **cn=config** where everything is stored in ldif format including schemas.

Schemas must therefore be converted from schema format to ldif format to be inserted in the directory, 
you must also be able to update, delete, add schemas during the life of your directory.

To simplify all these operations we have written two utilities that can be used by everyone, 
including those that would not use FusionDirectory.

- ldap-schema-manager: list, insert, modify, insert diagrams
- schema2ldif: which converts your schemas to ldif

.. _OpenLDAP : https://openldap.org/
.. _Schema2ldif : https://www.fusiondirectory.org/en/schema2ldif/

