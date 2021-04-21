.. _fd-debian-repository-label:


Debian Repository
'''''''''''''''''

.. _fd-debian-repository-stretch-label:

Debian Stretch
^^^^^^^^^^^^^^

Add a file named **fusiondirectory-release.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory repository
   deb https://public.fusiondirectory.org/stretch-fusiondirectory-release/ stretch main

Add a file named **schema2ldif-release.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #latest version of schema2ldif
   deb https://public.fusiondirectory.org/stretch-schema2ldif-release/ stretch main
