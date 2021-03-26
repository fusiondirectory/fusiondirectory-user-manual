.. _debian-repository-label:


Debian Repository
'''''''''''''''''

.. _debian-repository-stretch-label:

Debian Stretch
^^^^^^^^^^^^^^

To use the lastest published version for **stretch** put this in
your /etc/apt/sources.list

.. code-block:: shell

   #fusiondirectory repository
   deb http://repos.fusiondirectory.org/fusiondirectory-current/debian-stretch stretch main

.. code-block:: shell

   #fusiondirectory extra repository
   deb http://repos.fusiondirectory.org/fusiondirectory-extra/debian-stretch stretch main

.. _rpm-repository-label:

RPM Repository
''''''''''''''

A repository is available for Centos 7

This repository contains the stable and oldstable version of
FusionDirectory. It also contains the extra packages needed to use
FusionDirectory.

To use the lastest published version put this in your yum config :

.. _fd-rpm-repository-centos7-label:

CentOS 7 / RHEL 7
^^^^^^^^^^^^^^^^^

To use the lastest published version put this

.. code-block:: shell

   [fusiondirectory]
   name=Fusiondirectory Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-current/rhel7/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

.. code-block:: shell

   [fusiondirectory-extra]
   name=Fusiondirectory Extra Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-extra/rhel7/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

SRPMS are also available in the following repo :

.. code-block:: shell

   [fusiondirectory-src]
   name=Fusiondirectory Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-current/rhel7/SRPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Downloading the source
''''''''''''''''''''''

The source download area is here

http://repos.fusiondirectory.org/sources/
