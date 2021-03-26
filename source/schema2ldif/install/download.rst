.. _schema2ldif-debian-repository-label:


Debian Repository
'''''''''''''''''

.. _sl-debian-repository-stretch-label:

Debian Stretch
^^^^^^^^^^^^^^

To use the lastest published version for **stretch** put this in
your /etc/apt/sources.list

.. code-block:: shell

   #fusiondirectory extra repository
   deb http://repos.fusiondirectory.org/fusiondirectory-extra/debian-stretch stretch main

.. _sl-rpm-repository-label:

RPM Repository
''''''''''''''

A repository is available for Centos7

CentOS 7
^^^^^^^^

To use the lastest published version put this

.. code-block:: shell

   [fusiondirectory-extra]
   name=Fusiondirectory Extra Packages for RHEL / CentOS 7
   baseurl=http://repos.fusiondirectory.org/fusiondirectory-extra/rhel7/RPMS/
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Downloading the source
''''''''''''''''''''''

The source download area is here

https://repos.fusiondirectory.org/sources/
