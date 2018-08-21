.. _debian-repository-label:

Debian Repository
'''''''''''''''''

To use the lastest published version for **stretch** put this in
your /etc/apt/sources.list

.. code-block:: shell

   #fusiondirectory repository
   deb http://repos.fusiondirectory.org/fusiondirectory-current/debian-stretch stretch main

.. code-block:: shell

   #fusiondirectory extra repository
   deb http://repos.fusiondirectory.org/fusiondirectory-extra/debian-stretch stretch main


To use the lastest published version for **jessie** put this in your
/etc/apt/sources.list

.. code-block:: shell

   #fusiondirectory repository
   deb http://repos.fusiondirectory.org/fusiondirectory-current/debian-jessie jessie main

.. code-block:: shell
  
   #fusiondirectory extra repository
   deb http://repos.fusiondirectory.org/fusiondirectory-extra/debian-jessie jessie main

!!! Wheezy is deprecated and will not be maintained anymore, the latest release is 1.2 !!!


.. _rpm-repository-label:

RPM Repository
''''''''''''''

A repository is available for CentOS 6 / Centos7

This repository contains the stable and oldstable version of
FusionDirectory. It also contains the extra packages needed to use
FusionDirectory.

To use the lastest published version put this in your yum config :

.. _rpm-repository-centos6-label:

CentOS 6 / RHEL 6
^^^^^^^^^^^^^^^^^

To use the lastest published version put this

.. code-block:: shell

   [fusiondirectory]
   name=Fusiondirectory Packages for RHEL / CentOS 6
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-current/rhel6/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

.. code-block:: shell

   [fusiondirectory-extra]
   name=Fusiondirectory Extra Packages for RHEL / CentOS 6
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-extra/rhel6/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

SRPMS are also available in the following repo :

.. code-block:: shell

   [fusiondirectory-src]
   name=Fusiondirectory Packages for RHEL / CentOS 6
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-current/rhel6/SRPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

!!! Scientific Linux is deprecated and will not be maintained anymore, you can switch the centos packages !!!

.. _rpm-repository-centos7-label:

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
