Migrations issues
=================


* After installing FusionDirectory using an existing LDAP tree, my user accounts are not listed.

You need to add the following objectClasses to your accounts:

.. code-block:: shell

    objectClass: person
    objectClass: organizationalPerson

if you follow the fusiondirectory web setup those accounts will be migrated automatically 

