.. _fd-rpm-repository-label:

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

