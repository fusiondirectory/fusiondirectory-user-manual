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

For Centos / Redhat
'''''''''''''''''''

Authentification
^^^^^^^^^^^^^^^^

The authentification is done inside the repository files 

Install repositories
^^^^^^^^^^^^^^^^^^^^

* To add the repositories for the stable fixes version to your system copy the files ending with production.repo you get into /etc/yum.repos.d/

.. code-block:: console

   root@fusiondirectory:~# cp *production.repo /etc/yum.repos.d/

* update your repositories to see that the enterprise repository is working

.. code-block:: console

   root@fusiondirectory:~# yum update 
   Modules complémentaires chargés : fastestmirror
   Determining fastest mirrors
   epel/x86_64/metalink                                                                     |  32 kB  00:00:00     
   * base: ftp.belnet.be
   * epel: epel.mirror.wearetriple.com
   * extras: centos.mirror.fr.planethoster.net
   * remi: remi.schlundtech.de
   * remi-php72: remi.schlundtech.de
   * remi-safe: remi.schlundtech.de
   * updates: ftp.belnet.be
   base                                                                                     | 3.6 kB  00:00:00     
   epel                                                                                     | 4.7 kB  00:00:00     
   extras                                                                                   | 2.9 kB  00:00:00     
   yourcompany-fusiondirectory-centos7-fusiondirectory-production.repo                      | 2.9 kB  00:00:00     
   remi                                                                                     | 3.0 kB  00:00:00     
   remi-php72                                                                               | 3.0 kB  00:00:00     
   remi-safe                                                                                | 3.0 kB  00:00:00      
   updates                                                                                  | 2.9 kB  00:00:00     
   (1/9): epel/x86_64/group_gz                                                              |  96 kB  00:00:02     
   (2/9): epel/x86_64/updateinfo                                                            | 1.0 MB  00:00:00     
   (3/9): extras/7/x86_64/primary_db                                                        | 243 kB  00:00:00     
   (4/9): yourcompany-fusiondirectory-centos7-fusiondirectory-production.repo/primary_db    |  12 kB  00:00:00     
   (5/9): remi/primary_db                                                                   | 3.1 MB  00:00:01     
   (6/9): remi-safe/primary_db                                                              | 2.1 MB  00:00:01     
   (7/9): remi-php72/primary_db                                                             | 254 kB  00:00:01     
   (8/9): epel/x86_64/primary_db                                                            | 7.0 MB  00:00:03     

For FusionDirectory
^^^^^^^^^^^^^^^^^^^

The **yourcompany-subscription-fusiondirectory.ini** is the file to be imported into FusionDirectory to show that you have a valid subscription.

See :ref:`fd-activate-a-subscription-label`
