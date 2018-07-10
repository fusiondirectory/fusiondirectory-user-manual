Migrate FusionDirectory from 1.2 to 1.2.1
                                         

New Depot Configuration
^^^^^^^^^^^^^^^^^^^^^^^

    !: The repositories have been cleaned and reorganized please update
    your configuration accordingly :!:

`Downloading from Repositories <en:dl_install>`__

    !: the gpg keys for FusionDirectory and Argonaut have been renewed
    so you need to install the new keys for the packages to install
    correctly :!:

`Getting the official GPG keys to active package
signature <en:documentation:admin_get_ggp_keys>`__

Upgrade schema2ldif
^^^^^^^^^^^^^^^^^^^

For Jessie distribution add extra repository

#. fusiondirectory debian-extra repository

deb http://repos.fusiondirectory.org/fusiondirectory-extra/debian-jessie
jessie main

Update the package list and upgrade schema2ldif

``apt-get`` ``update`` ``apt-get`` ``install`` ``schema2ldif``

Upgrade FusionDirectory first
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Upgrade FusionDirectory core package before other ones to avoid
dependencies errors:

``apt-get`` ``install`` ``fusiondirectory``

Upgrade FusionDirectory schema package too.

``apt-get`` ``install`` ``fusiondirectory-schema``

Upgrade of LDAP directory
^^^^^^^^^^^^^^^^^^^^^^^^^

Upgrade core schema of FusionDirectory

``fusiondirectory-insert-schema`` ``-m``
``/etc/ldap/schema/fusiondirectory/core-fd.schema``

Enjoy :)
