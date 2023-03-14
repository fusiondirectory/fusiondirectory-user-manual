fusiondirectory-migration-manager
=================================

Description
-----------

This tool is designed to help you configure and perform multiple checks on your
FusionDirectory instance and fix usual misconfiguration.

Extra features allow you to install FusionDirectory's plugins, and
change destinations directories.

Options
-------

--list-deprecated 
  List deprecated attributes and objectClass.

--check-deprecated
   List LDAP entries using deprecated attributes or objectClass.

--ldif-deprecated
	 Print an LDIF removing deprecated attributes.

--remove-supann-root
	 Remove Supann root establishment from FusionDirectory release < v1.4.

--check-ids
   This option check your LDAP tree for duplicated uidNumber or
   gidNumber among users and groups.

--migrate-users
   This option add FusionDirectory attributes to the people branch.

--migrate-interfaces
	 This allows migrating your system if FusionDirectory release is < v1.4.

--list-vars
   This option will list the variables you can change to install
   FusionDirectory on another set of directories. This option is
   intended for people wanting to install from the sources.

--set-VAR=variable
   This option will change the variable for the FusionDirectory
   installation. it is only useful with --install-directories and for
   people installing from sources.

Examples
--------

Migrate-users

.. code-block:: shell

   fusiondirectory-migration-manager --migrate-users
