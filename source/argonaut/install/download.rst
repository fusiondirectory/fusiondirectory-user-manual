.. _cs_debian-repository-label:


Debian Repository
'''''''''''''''''

.. _cs_debian-repository-stretch-label:

Debian Stretch
^^^^^^^^^^^^^^

To use the lastest published version for **stretch** put this in
your /etc/apt/sources.list

.. code-block:: shell

   #fusiondirectory repository
   deb https://repos.fusiondirectory.org/argonaut-current/debian-stretch/ stretch main

.. code-block:: shell

   #fusiondirectory extra repository
   deb https://repos.fusiondirectory.org/argonaut-extra/debian-stretch/ stretch main

RPM Repository
''''''''''''''

A repository is available for Centos7

This repository contains the stable version of Argonaut. 
It also contains the extra packages needed to use Argonaut.

To use the lastest published version put this in your yum config :

.. _cs_rpm-repository-centos7-label:

CentOS 7 / RHEL 7
^^^^^^^^^^^^^^^^^

To use the lastest published version put this

.. code-block:: shell

   [argonaut]
   name=Argonaut Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/argonaut-current/rhel7/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

.. code-block:: shell

   [argonaut-extra]
   name=Argonaut Extra Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/argonaut-extra/rhel7/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

SRPMS are also available in the following repo :

.. code-block:: shell

   [argonaut-src]
   name=Argonaut Packages for RHEL / CentOS 7
   baseurl=https://repos.fusiondirectory.org/argonaut-current/rhel7/SRPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Downloading the source
''''''''''''''''''''''

The source download area is here

https://repos.fusiondirectory.org/sources/
