.. _old-gpg-keys-label:

Getting the old official GPG keys to active package signature
-------------------------------------------------------------

.. warning::

   This key is no longer used it was changed after FusionDirectory 1.2.3
   and only usefull if you try to reinstall an old version

Getting the old official gpg key
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

    gpg --keyserver keys.gnupg.net --recv-key 0xD744D55EACDA69FF

    gpg --export -a "FusionDirectory Project Signing Key <contact@fusiondirectory.org>" > FD-archive-key

Adding the key to apt for Debian/Ubuntu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   apt-key add FD-archive-key

Adding the key for RPM into Centos
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   cp FD-archive-key /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

   rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY
