fusiondirectory-configuration-manager
=====================================

Description
-----------

This tool is designed to help you configure and perform multiple checks on your
FusionDirectory instance and fix usual misconfiguration.

Extra features allow you to install FusionDirectory's plugins, and
change destinations directories.

Options
-------

--update-cache
   This option update the /var/cache/fusiondirectory/class.cache file.
   Which contain PHP classes used in FusionDirectory, and their
   location.

--update-locales
   This option update internalization, by generating a new .mo locales
   file for each language, with every .po files it found. Needs *msgcat*
   and *msgfmt* to be installed.

--check-directories
   This option perform a check on all FusionDirectory's files or
   directories.

--check-config
   This option perform a check on FusionDirectory's config file.

--check-ldap
   This option check your LDAP tree. Looking for admin account, and
   groups or people branch. If one of those don't exists, the script
   will ask you what to do.

--encrypt-passwords
   This option will encrypt the password inside your
   fusiondirectory.conf file, it need the headers module to be activated
   in your apache to work.

--show-version
   This option will parse the file variables_common.inc of
   FusionDirectory to find out which version of FusionDirectory is
   installed.

--list-vars
   This option will list the variables you can change to install
   FusionDirectory on another set of directories. This option is
   intended for people wanting to install from the sources.

--write-vars
   This option will write back the variables.inc file with the updated
   variables and is only useful with --set-VAR=variable and for people
   installing from sources.

--set-VAR=variable
   This option will change the variable for the FusionDirectory
   installation. it is only useful with --install-directories and for
   people installing from sources.

--show-config
   This option will print a dump of the FusionDirectory configuration
   LDAP node.

--set-config-VAR=value
   This option sets the value of a configuration field in the LDAP. The
   value needs to be in the correct LDAP format. You cannot set
   multivalued field with this. The var name can be provided with or
   without the fd prefix.

Examples
--------

Update FusionDirectory class cache and update localization

.. code-block:: shell
   
   fusiondirectory-setup --update-cache --update-locales

List possible vars to give to --set

.. code-block:: shell

   fusiondirectory-setup --list-vars
     locale_cache_dir [locale]
     config_file [fusiondirectory.conf]
     fd_cache [/var/cache/fusiondirectory]
     fd_smarty_dir [/usr/share/php/smarty3]
     fd_spool_dir [/var/spool/fusiondirectory]
     fai_log_dir [fai]
     tmp_dir [tmp]
     secrets_file [fusiondirectory.secrets]
     template_dir [template]
     locale_dir [locale]
     class_cache [class.cache]
     fd_config_dir [/etc/fusiondirectory]
     fd_home [/var/www/fusiondirectory]

update the class.cache name and write back the variables.inc file

.. code-block:: shell

   fusiondirectory-setup --set-class_cache=class.cache --write-vars
