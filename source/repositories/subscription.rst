.. _fd-subscription-repository-label:

Subscription Repository
=======================

When buying a subscription you will receive three files

* yourcompany-subscription-fusiondirectory.ini
* yourcompany-auth.conf
* yourcompany-fusiondirectory-subscription-centos7fixes.repo

The **yourcompany-subscription-fusiondirectory.ini** is the file to be imported into FusionDirectory to show that you have a valid subscription

The **yourcompany-auth.conf** is the file needed to access the enterprise repository with authentification for Debian

The **fusiondirectory-subscription-centos7fixes.repo** is the file need to add the enterprise repository to a centos 7 Linux Distribution

.. _fd-enterprise-debian-repository-label:

Debian Repository
'''''''''''''''''

* To authenticate to the enterprise repository copy with root access the file **yourcompany-auth.conf** to /etc/apt/auth.conf

.. code-block:: console

    root@ffusiondirectory:~# cp  yourcompany-auth.conf /etc/apt/auth.conf

.. note::   

   All url are made the same way. 
   
   if you want to install the fixes for Debian Stretch

   https://enterprise.fusiondirectory.org/debianversion-fusiondirectory-fixes

* Write the source.list

.. code-block:: console

   root@ffusiondirectory:~# cd /etc/apt/sources.list.d/
   root@ffusiondirectory:~# echo https://enterprise.fusiondirectory.org/stretch-fusiondirectory-fixes/ stretch main > stretch-fusiondirectory-fixes.list

* update your repositories to see that the enterprise repository is working

.. code-block:: console

   root@ffusiondirectory:~# apt-get update 
   Hit:1 http://security.debian.org/debian-security buster/updates InRelease
   Hit:2 http://deb.debian.org/debian buster InRelease                                                                   
   Hit:3 https://enterprise.fusiondirectory.org/buster-fusiondirectory-fixes buster InRelease

.. _fd-enterprise-centos-repository-label:

RPM Repository
''''''''''''''

* To install FusionDirectory fixes from the enterprise repository for Centos 7 

.. code-block:: console

    root@ffusiondirectory:~# cp  fusiondirectory-subscription-centos7fixes.repo /etc/yum.repos.d/
