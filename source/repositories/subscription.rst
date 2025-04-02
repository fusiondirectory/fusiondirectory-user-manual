Subscription Repository
=======================

When buying a subscription you will receive a set of files

For Debian
''''''''''

Authentification
^^^^^^^^^^^^^^^^

* To authenticate to the enterprise repository copy with root access the file **yourcompany-auth.conf** to /etc/apt/auth.conf

.. code-block:: console

   root@fusiondirectory:~# cp  yourcompany-auth.conf /etc/apt/auth.conf

Install repositories
^^^^^^^^^^^^^^^^^^^^

.. note::

   We don't always produce a stable production version. A stable production version is a version that contains minor corrections that, we believe, will benefit all subscribers.
   If we produce one, you may configure it as outlined herein.

* To add the repositories for the stable production version to your system copy the files ending with production.list into /etc/apt/sources.list.d/

.. code-block:: console

   root@fusiondirectory:~# cp *-production.list /etc/apt/sources.list.d/

* update your repositories to see that the enterprise repository is working

.. code-block:: console

   root@ffusiondirectory:~# apt-get update 
   Hit:1 http://security.debian.org/debian-security buster/updates InRelease
   Hit:2 http://deb.debian.org/debian buster InRelease                                                                   
   Hit:3 https://enterprise.fusiondirectory.org/bullseye-fusiondirectory-production bullseye InRelease

For FusionDirectory
^^^^^^^^^^^^^^^^^^^

The **yourcompany-subscription-fusiondirectory.ini** is the file to be imported into FusionDirectory to show that you have a valid subscription.

See :ref:`fd-activate-a-subscription-label`
