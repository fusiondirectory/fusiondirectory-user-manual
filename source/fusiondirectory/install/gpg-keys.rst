.. _gpg-keys-label:

Getting the official GPG keys to active package signature
---------------------------------------------------------

Our packages for Debian and Centos are signed with the official gpg
key of the project.

Getting the new official gpg key
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

    gpg --keyserver keys.gnupg.net --recv-key 0xD744D55EACDA69FF

    gpg --export -a "FusionDirectory Project Signing Key <contact@fusiondirectory.org>" > FD-archive-key

Getting the development gpg key
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   gpg --keyserver keys.gnupg.net --recv-key 0xADD3A1B88B29AE4A

   gpg --export -a "FusionDirectory Packagers <fusiondirectory-packages@lists.fusiondirectory.org>" > FD-archive-dev-key

Adding the key to apt for Debian/Ubuntu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   apt-key add FD-archive-key

Adding the key for RPM into Centos
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   cp FD-archive-key /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

   rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY
