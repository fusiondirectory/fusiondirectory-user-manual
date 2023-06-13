.. _fd-ubuntu-repository-label:

Ubuntu Repository
'''''''''''''''''

First add the FusionDirectory tools and libraries repositories


Add a file named **fusiondirectory-integrator.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory integrator
   deb https://public.fusiondirectory.org/debian/fusiondirectory-integrator/ bullseye main

Add a file named **fusiondirectory-utilities.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory utilities
   deb https://public.fusiondirectory.org/debian/fusiondirectory-utilities/ bullseye main

Add a file named **fusiondirectory-external-libraries.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory libraries
   deb https://public.fusiondirectory.org/debian/fusiondirectory-external-libraries/ bullseye main


Second install the repository corresponding to your distribution 

Ubuntu Focal
^^^^^^^^^^^^

Add a file named **fusiondirectory-release.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory repository
   deb https://public.fusiondirectory.org/ubuntu/focal-fusiondirectory-release/ focal main

Ubuntu bionic      
^^^^^^^^^^^^^ 

Add a file named **fusiondirectory-release.list** in /etc/apt/sources.list.d/

.. code-block:: shell

   #fusiondirectory repository
   deb https://public.fusiondirectory.org/ubuntu/bionic-fusiondirectory-release/ bionic main



