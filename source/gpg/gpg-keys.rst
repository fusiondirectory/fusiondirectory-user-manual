.. _gpg-keys-label:

Getting the official GPG keys to active package signature
---------------------------------------------------------

Our packages for Debian and Centos are signed with the official gpg
key of the project.

Getting the new official gpg key
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

    gpg --keyserver keys.gnupg.net --recv-key 0xFE0FEAE5AC483A86

    gpg --export -a "FusionDirectory Packages Signing Key <contact@fusiondirectory.org>" > FD-archive-key


Adding the key to apt for Debian/Ubuntu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   apt-key add FD-archive-key

Adding the key for RPM into Centos
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   cp FD-archive-key /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

   rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY
